1. src/main/java/spark/resource/ClassPathResourceHandler.java#83
    - before
       - DirectoryTraversal.protectAgainstInClassPath(resource.getPath());
    - developer's repair
       - DirectoryTraversal.protectAgainstInClassPath(resource.getPath(), baseResource);
    - our repair 
       - DirectoryTraversal.protectAgainstInClassPath(resource.getPath(), baseResource);

2. src/main/java/spark/resource/ExternalResourceHandler.java
    - before
       - DirectoryTraversal.protectAgainstInClassPath(resource.getPath());
    - developer's repair
       - DirectoryTraversal.protectAgainstForExternal(resource.getPath(), baseResource);
    - our repair 
       - DirectoryTraversal.protectAgainstInClassPath(resource.getPath(), baseResource);
