1. src/main/java/spark/Spark.java#283
    - before
       - routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route);
    - developer's repair
       - routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route, route.getAccessType());
    - our repair 
       - routeMatcher.parseValidateAddRoute(httpMethod + " '" + route.getPath() + "'", route, truststorePassword);

2. src/main/java/spark/Spark.java#294
    - before
       - routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter);
    - developer's repair
       - routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter, filter.getAccessType());
    - our repair 
       - routeMatcher.parseValidateAddRoute(httpMethod + " '" + filter.getPath() + "'", filter, truststorePassword);

3. src/main/java/spark/route/SimpleRouteMatcher.java#228
    - before
       - addRoute(method, url, target);
    - developer's repair
       - addRoute(method, url, target, acceptType);
    - our repair 
       - addRoute(method, url, target, httpMethod);