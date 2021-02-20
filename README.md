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