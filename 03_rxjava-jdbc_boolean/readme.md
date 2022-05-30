- 修正箇所
    1. src/main/java/com/github/davidmoten/rx/jdbc/QuerySelectOnSubscribe.java#108
        - Util.setParameters(state.ps, parameters);
    2. src/main/java/com/github/davidmoten/rx/jdbc/QueryUpdateOnSubscribe.java#217
        - Util.setParameters(state.ps, parameters);
- 開発者の修正
    1. Util.setParameters(state.ps, parameters, query.names());
    2. Util.setParameters(state.ps, parameters, query.names());
- 提案手法の修正
    1. Util.setParameters(state.ps, parameters, stateProvided);
    2. Util.setParameters(state.ps, parameters, false);
