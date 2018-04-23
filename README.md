#### openshift-s2i-java Builder image
Openshift Java S2I Builder image. Based on Alpine. Suitable for java (fatjar) types of applications.

Builder can be used to use generate Java S2I builds for fat-jar packaged applications.

Only binary build is supported.

##### How to use

##### Start development

Create new binary build from local directory 

	oc new-build "openshift-s2i-java:latest" --name=myapp --binary=true
	

Start build

	oc start-build myapp --from-file=myfatjar.jar --follow=true --wait=true
