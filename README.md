# azure-app-service-frontend-and-backend-step.-
frontend is on nodejs and backend is on java


Step for azure fronted deployment:
-----------------------------------------
    
    - git clone  <repo frontend>
    - cd <repo folder>
    Note: frontend backend sa communicate kry is k lye ap, backend k url frontend k enviroment file ma **host_url** ma dye gye..
    - npm install ---→ install package/dependencies .. it will see packages/dependenies listed in package.json create **node_mode** folder accordingly
    - npm start    --- for development    and use **npm run build: <env>** like npm run build:dev-azure for making production ready build.  And it will give you **dist/**. Is folder ma updated ouput files hogi..
    
    - go side dist/ folder. And make zip for folder available inside the dist folder. 
    - now deploy/upload this zip to azure app service from kudu …
    
    - now for frontend you also need to point your frontend code directory with path….
    
    For this go to azure app service > settings > configuration > path mapping > add virtual path 
    
    like: virtual path: /apt
            phyical path: site\wwwroot\axelerate-web 
    
    
    remember: frontend is writthen on nodejs on version 16 you can use version 18





step for backend deployment
-----------------------------------
	      
    backend java per written ha or run hota ha. Iski .jar file hoti jo
    
    java –jar <.jar file>
    
    sa run hota ha…
    
    
    
    make zip for jar file with command
    
    zip r    zipfile name   .jar file name
    
    and upload thi zip to kudu…..
    
    or postman sa isko test kr lo..
