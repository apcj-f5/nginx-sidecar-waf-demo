# sidecarwaf

Run the following command to get it running 

 
kubectl apply -f nginx-configmap.yml

kubectl apply -f hackazon-waf.yml

kubectl expose pod hackazon-with-sidecar-waf --type=NodePort --port=80 --target-port=81 

Simple test for modsec in operation 

curl -H "User-Agent: Nikto" http://<app-ip-address>
 
curl http://<app-ip-address>?testparam=modsectest 
 
