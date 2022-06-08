# Chaos-Engineering
WHAT IS CHAOS ENGINEERING?
Chaos Engineering is the discipline of experimenting on a system in order to build confidence in the system's capability to withstand turbulant conditions in production. In simple words, it is thoughtful planned experiments designed to reveal the weakness in systems. Basically you have to think something and you have to plan and experiment around that so that you can reveal the weakness in your system software, may be hardware or software system.
WHY DO WE NEED CHAOS ENGINEERING?
Nowadays, most of the companies moving towards the microservice architecture because it provides you flexibility. So, basically if you see these microservice architecture they are very complex and distributed and there are countless number of connections and dependencies with each other. So, it is practically very difficult to test each and every thing from traditional QA practices. So, you really want a mechanism where you can test these things pro-actively. That's why we need Chaos Engineering so that, we can find issues in the large distributed systems.
PRINCIPLES OF CHAOS ENGINEERING
1. Define steady state
2. Form your hypothesis
3. Plan and run your experiments
4. Measure and learn
How chaos engineering is different from testing?
Testing is a kind of validation where you know this is the Input, that is the Output and you validate it. But Chaos Engineering, is all about experimentation, where you make hypothesis and then you do some experimentation which nobody has done.
For Example- you have a microservice architecture and in the architecture the service A is talking to service B and service C etc, so it's your hypothesis, it's your thinking how service A affects service B, then you have to plan experiments according to prove your theory. That is how it is different from testing.
SOME OPEN SOURCE TOOLS WHICH ARE THERE IN THE MARKET
1. Chaos Monkey
2. Chaos Mesh
3. Gremlin
4. Litmus
5. Cloud Blade
COMMANDS TO INSTALL CHAOS MESH
Install Helm first
- curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
- chmod 700 get_helm.sh
- ./get_helm.sh
For Chaos Mesh Installation
1. Add chaos mesh repository
- helm repo add chaos-mesh https://charts.chaos-mesh.org
2. View the chaos mesh version
- helm search repo chaos-mesh
3. Now create Namespace
- kubectl create ns chaos-testing
4. Now use Docker to install chaos mesh(you can install it in other environments also)
- helm install chaos-mesh chaos-mesh/chaos-mesh -n=chaos-testing --version 2.1.5
5. Verify the installation
- kubectl get po -n chaos-testing
