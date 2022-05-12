- 修正箇所
    1. src/main/java/org/apache/commons/io/output/DeferredFileOutputStream.java#102
        - this(threshold, outputFile, null, null, null);
    2. src/main/java/org/apache/commons/io/output/DeferredFileOutputStream.java#127
        - this(threshold, null, prefix, suffix, directory);

- 開発者の修正
    1.  this(threshold, outputFile, null, null, null, ByteArrayOutputStream.DEFAULT_SIZE);
    2. this(threshold, null, prefix, suffix, directory, ByteArrayOutputStream.DEFAULT_SIZE);

- 提案手法の修正
    1. this(threshold, outputFile, null, null, null, 0);
    2. this(threshold, null, prefix, suffix, directory, 0);
