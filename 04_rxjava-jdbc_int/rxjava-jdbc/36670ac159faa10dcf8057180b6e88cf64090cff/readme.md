1. src/main/java/com/github/davidmoten/rx/jdbc/QueryContext.java#19
    - before
       - this(db, 1);
    - developer's repair
       - this(db, 1, 0);
    - our repair 
       - this(db, 1, 0);

2. src/main/java/com/github/davidmoten/rx/jdbc/QueryContext.java#75
    - before
       - new QueryContext(db, batchSize);
    - developer's repair
       - new QueryContext(db, batchSize, fetchSize);
    - our repair 
       - new QueryContext(db, batchSize, fetchSize);
