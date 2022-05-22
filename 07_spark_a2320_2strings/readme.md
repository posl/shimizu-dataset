- 修正箇所
    1. src/main/java/spark/resource/ClassPathResourceHandler.java#83
        - DirectoryTraversal.protectAgainstInClassPath(resource.getPath());
    2. src/main/java/spark/resource/ExternalResourceHandler.java
        - DirectoryTraversal.protectAgainstForExternal(resource.getPath());
        
- 開発者の修正
    1. DirectoryTraversal.protectAgainstInClassPath(resource.getPath(), baseResource);
    2. DirectoryTraversal.protectAgainstForExternal(resource.getPath(), baseResource);

- 提案手法の修正
    1. DirectoryTraversal.protectAgainstInClassPath(resource.getPath(), baseResource);
    2. DirectoryTraversal.protectAgainstForExternal(resource.getPath(), baseResource);
