- 修正箇所
    1. src/main/java/spark/Spark.java#283
        - routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route);
    2. src/main/java/spark/Spark.java#294
        - routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter);
    3. src/main/java/spark/route/SimpleRouteMatcher.java#228
        - addRoute(method, url, target);
    4. src/main/java/spark/webserver/MatcherFilter.java#92
        - List<RouteMatch> matchSet = routeMatcher.findTargetsForRequestedRoute(HttpMethod.before, uri);
    5. src/main/java/spark/webserver/MatcherFilter.java#118
        - match = routeMatcher.findTargetForRequestedRoute(HttpMethod.valueOf(httpMethodStr), uri);
    6. src/main/java/spark/webserver/MatcherFilter.java#125
        - bodyContent = routeMatcher.findTargetForRequestedRoute(HttpMethod.get, uri) != null ? "" : null;
    7. src/main/java/spark/webserver/MatcherFilter.java#156
        - matchSet = routeMatcher.findTargetsForRequestedRoute(HttpMethod.after, uri);
- 開発者の修正
    1. routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route.getAccessType(), route);
    2. routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter.getAccessType(), filter);
    3. addRoute(method, url, acceptType, target);
    4. List<RouteMatch> matchSet = routeMatcher.findTargetsForRequestedRoute(HttpMethod.before, uri, acceptType);
    5. match = routeMatcher.findTargetForRequestedRoute(HttpMethod.valueOf(httpMethodStr), uri, acceptType);
    6. bodyContent = routeMatcher.findTargetForRequestedRoute(HttpMethod.get, uri, acceptType) != null ? "" : null;
    7. matchSet = routeMatcher.findTargetsForRequestedRoute(HttpMethod.after, uri, acceptType);
    
- 提案手法の修正
    12. truststorePassword, keystorePassword, ipAddress , keystoreFile, truststoreFile, staticFileFolder , externalStaticFileFolder
    3. 
    4567.
