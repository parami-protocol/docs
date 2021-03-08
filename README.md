# docs
Parami API Documentation.

Main pallets are `did` and `ads`.

## Parami APIs

### Did Storage

```
Did.GenesisAccount
Did.BaseQuota
Did.MinDeposit
Did.FeeToPrevious

Did.Identity
Did.IdentityOf
Did.SocialAccount
Did.Metadata

Did.AllDidCount
Did.UserKeys
Did.DidIndices
```

### Did Call

```rust
create(pubkey: Vec<u8>, address: T::AccountId, did_type: Vec<u8>, superior: T::Hash, social_account: Option<Vec<u8>>, social_superior: Option<Vec<u8>>)
update(to: T::AccountId) # transfer did ownership
transfer(to_user: T::Hash, value: T::Balance, memo: Vec<u8>)
lock(value: T::Balance, period: T::Moment)
force_lock(user: T::Hash, value: T::Balance) # by root
unlock(value: T::Balance)
add_external_address(add_type: Vec<u8>, address: Vec<u8>)
set_group_name(name: Vec<u8>)
judge(account: T::AccountId)
```

### Ads Storage

```rust
trait Store for Module<T: Trait> as AdsModule {
    pub Contract get(fn contract) config(): T::AccountId;
    pub MinDeposit get(fn min_deposit) config(): T::Balance;
    pub AdsRecords get(fn ads_records): map hasher(twox_64_concat) AdIndex => AdsMetadata<T::Balance, T::Moment>;
    pub AdsActives get(fn ads_actives): map hasher(twox_64_concat) ActiveIndex => Option<AdIndex>;
    pub AdsActiveCount get(fn ads_active_count): Option<ActiveIndex>;
    pub AdsOwner get(fn ads_owner):map hasher(twox_64_concat) AdIndex => T::Hash;
    pub AllAdsCount get(fn all_ads_count): AdIndex;
    pub OwnedAds get(fn owned_ads):map hasher(twox_64_concat) T::Hash => Vec<AdIndex>;
}
```

### Ads Call

TODO