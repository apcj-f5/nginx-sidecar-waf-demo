# sidecarwaf

Run the following command to get it running 

 
kubectl apply -f nginx-configmap.yml
Kubectl apply -f hackazon-waf.yml
kubectl expose pod hackazon-with-sidecar-waf --type=NodePort --port=80 --target-port=81 

Simple test for modsec in operation 

curl -H "User-Agent: Nikto" http://10.108.94.59
 
curl http://10.108.94.59?testparam=modsectest 
 
