ACID: 트랜잭션이 안전하게 처리되기 위한 4가지 속성

1. Atomic(원자성): 트랜잭션 내의 모든 연산은 불가분 단위로 취급된다. 하나의 연산이라도 실패 시 트랜잭션에서 수정된 모든 데이터는 트랜잭션 시작 전 상태로 롤백한다.
2. Consistency(일관성): 트랜잭션이 종료된 시점에 데이터는 모든 제약을 준수하는 상태여야한다. (일관성, 데이터가 모순 없이 양립한다.)
3. Isolation(격리성): 동시에 실행되는 여러개의 트랜잭션은 서로에게 영향을 주지 않아야한다. (하나의 데이터를 여러개의 트랜잭션에서 사용할 경우..)
4. Durability(지속성): 트랜잭션이 커밋되면 그 결과는 시스템에 장애가 발생하더라도 영구 보존 되어야한다.


> [!NOTE]
> 격리 레벨
> 1. Read Uncommitted
> 2. Read Committed
> 3. Repeatable Read
> 4. Serializable 
>
> 지속성을 위한 매커니즘
> 1. WAL(Write-Ahead Logging)
> 2. 체크포인트(checkpoint)
> 3. 저널링(journaling)

