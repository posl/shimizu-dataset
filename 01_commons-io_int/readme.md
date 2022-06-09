1. src/main/java/org/apache/commons/io/output/DeferredFileOutputStream.java#102
   - before
      - this(threshold, outputFile, null, null, null);
   - developer's repair
      - this(threshold, outputFile, null, null, null, ByteArrayOutputStream.DEFAULT_SIZE);
   - our repair 
      - this(threshold, outputFile, null, null, null, 0);

2. src/main/java/org/apache/commons/io/output/DeferredFileOutputStream.java#127
   - before
      - this(threshold, null, prefix, suffix, directory);
   - developer's repair
      - this(threshold, null, prefix, suffix, directory, ByteArrayOutputStream.DEFAULT_SIZE);
   - our repair 
      - this(threshold, null, prefix, suffix, directory, 0);