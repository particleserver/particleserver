# Particle

Particle is a small, fast and very light framework for Eclipse MicroProfile™-deployments.

## Why?

This project is at this moment purely a learning exercise for all involved contributors. Our goal is to build a server that can be used to
run MicroProfile-compliant microservices and do so in a _frameworky_ manner. That means nothing to install besides Java and stuffi; the only
thing we do is to dump our applications there.

We are aware there is Helidon, Liberty, KumuluzEE and many others but we want nothing but support the latest Java with the latest
MicroProfile-specification and no other fuss so we take out the leg-work for others that do the tedious work of pushing all sorts of libs
into a Tomcat-container to get a _sort of_ EE/MP-container.

## Goals

Our goals are simple but hopefully clear enough to get a MVP:

* Should pass TCK for the latest MicroProfile-spec (5.0 at this moment).
* Runs on the latest Java LTS (17 at the time of writing).
* Fast boot (time to first response) without resorting to trickery like GraalVM.
* Nothing custom, we will to the extent possible use Reference Implementations for all specs.
* Fast as in high throughput.
* To the extent possible allow users to use Jakarta EE-specs like JPA, JTA or perhaps even EJB Lite (soft goal, some of the specs might be
  quite difficult to support).
* Only support UberJAR deployments ( we know that this really is an "anti-goal" as we should educate people that the UberJAR is wasteful, but
  we know that most people don't care and anyway just build an UberJAR ;) )

## Suggested third-party libs

* Jetty 11 for HTTP/Servlet 4.x
* SmallRye
* Weld
* RESTEasy or Jersey for JAX-RS

## License

Copyright 2022 Daniel Pfeifer & Core Contributors

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
