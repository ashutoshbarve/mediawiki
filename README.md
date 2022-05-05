# mediawiki"# mediawiki" 
"# mediawiki" 

This projeck consist of 3 main yaml files which are as follows:
1. Chart.yaml which basicaly have dummy values for the projeck.
2. values.yaml which is empty.
3. deploy.yml which will have our deployment logic.

chart.yaml, values.yml and charts (diractory), template (directory) will be created by default if you run "helm create <namespace>"
  
 This projeckt has been deployed on azure kuberneties cluster.
  Steps I have followed are mentioned below.
  
    1. Log in into the azure subscription (if have any).
  ![image](https://user-images.githubusercontent.com/26390486/166945059-8987ebb4-39d6-4838-adb9-ac63b8bef787.png)
  
    2. To deploy "helm install mediawik mediawiki/ --create-namespace test"
       Note: Make sure the namespace you are using in unique or else it will fail.
       Note: [If you face any issue] To debug you can add --debug tag, which will provide you with proper logs.
  ![image](https://user-images.githubusercontent.com/26390486/166946287-998b5095-4c14-4bbd-8f05-b6358ce57a8c.png)
  
    3. To conferm the deployment run "kubectl get deployment -n test"
  ![image](https://user-images.githubusercontent.com/26390486/166946863-1b86bc69-084c-4fd9-bd55-0b7979e9f0cb.png)

    4. To confetm pods are up and running run "kubectl get pots -n test"
  ![image](https://user-images.githubusercontent.com/26390486/166947462-e2cef2a2-3301-43b5-a074-c96a5deb1930.png)
 
To check if the site is up and running:
   1. Get ip address of the pod "run kubectl get pods -n test -o wide"
  ![image](https://user-images.githubusercontent.com/26390486/166948138-aa2509b7-742f-4ed5-88da-7c0c9f95fefb.png)
  
  2. To Conferm the site is up and running go to your browser enter the "ip:port"
  ![image](https://user-images.githubusercontent.com/26390486/166948519-e79aaf8d-ddcb-49c1-a518-b8ec5271f728.png)



    
