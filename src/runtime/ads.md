# The ADs

## Ads Storage

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

## Ads Call

TODO
