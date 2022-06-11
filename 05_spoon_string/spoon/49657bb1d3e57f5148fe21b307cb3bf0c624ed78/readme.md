1. src/main/java/spoon/support/compiler/SnippetCompilationHelper.java#122
    - before
       - new JDTSnippetCompiler(f);
    - developer's repair
       - new JDTSnippetCompiler(f, contents);
    - our repair 
       - new JDTSnippetCompiler(f, contents);
