- 修正箇所
    1. src/main/java/spark/Spark.java#283
        - routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route);
    2. src/main/java/spark/Spark.java#294
        - routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter);
    3. src/main/java/spark/route/SimpleRouteMatcher.java#228
        - addRoute(method, url, target);

- 開発者の修正
    1. routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route.getAccessType(), route);
    2. routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter.getAccessType(), filter);
    3. addRoute(method, url, acceptType, target);

- 提案手法の修正