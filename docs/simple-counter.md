# Simple Counter
폴코니 3종 체인에서 공통적으로 테스트용으로 작성하는 컨트랙트의 스펙입니다.

## State
```rust
struct State {
    /// A counting number
    count: u64,
    /// Authorized transaction submitters
    auth: Vec<String> // Unordered map would be proper as well
}
```

## Initialization
`count`와 `auth`의 초기값을 지정합니다.

## Transaction
```rust
struct Transaction {
    value: u64
}
```
`count`의 값을 `value`만큼 증가시키는 트랜잭션을 만들 수 있어야 합니다. 해당 트랜잭션의 제출자가 `auth`에 포함되어 있지 않거나 `value`의 값이 10보다 크면 트랜잭션을 실패시킵니다.

## Query
`count`와 `auth`의 값을 적절히 쿼리할 수 있어야 합니다.



