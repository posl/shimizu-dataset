- 修正箇所
    1. src/main/java/com/github/davidmoten/rx/jdbc/QueryContext.java#19
        - this(db, 1);
    2. src/main/java/com/github/davidmoten/rx/jdbc/QueryContext.java#75
        - new QueryContext(db, batchSize);

- 開発者の修正
    1. this(db, 1, 0);
    2. new QueryContext(db, batchSize, fetchSize);
    
- 提案手法の修正
    1. this(db, 1, 0);
    2. new QueryContext(db, batchSize, batchSize);
