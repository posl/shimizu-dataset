1. src/main/java/com/github/davidmoten/rx/jdbc/QuerySelectOnSubscribe.java#108
    - before
       - Util.setParameters(state.ps, parameters);
    - developer's repair
       - Util.setParameters(state.ps, parameters, query.names());
    - our repair 
       - Util.setParameters(state.ps, parameters, stateProvided);

2. src/main/java/com/github/davidmoten/rx/jdbc/QueryUpdateOnSubscribe.java#217
    - before
       - Util.setParameters(state.ps, parameters);
    - developer's repair
       - Util.setParameters(state.ps, parameters, query.names());
    - our repair 
       - Util.setParameters(state.ps, parameters, false);