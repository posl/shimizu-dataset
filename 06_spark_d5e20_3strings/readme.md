- 修正箇所
    1. src/main/java/spark/Spark.java#283
        - routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route);
    2. src/main/java/spark/Spark.java#294
        - routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter);
    3. src/main/java/spark/route/SimpleRouteMatcher.java#228
        - addRoute(method, url, target);

- 開発者の修正
    1. routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route, route.getAccessType());
    2. routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter, filter.getAccessType());
    3. addRoute(method, url, target, acceptType);

- 提案手法の修正
    1. routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route, truststorePassword);
    2. routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter, truststorePassword);
    3. addRoute(method, url, target, httpMethod);
