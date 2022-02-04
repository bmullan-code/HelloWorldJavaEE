# HelloWorldJavaEE (J2EE Tomcat app) with TAP Workload


1. Add the buildpack
```
kp clusterstore add default -b gcr.io/paketo-buildpacks/apache-tomcat
```
2. Create the workload 
```
tanzu apps workload create hello-world-java-ee -n dev \
--git-repo https://github.com/bmullan-pivotal/HelloWorldJavaEE \
--git-branch main --type web  
```
3. Retrieve the url
```
tanzu apps workload get hello-world-java-ee -n dev
```
