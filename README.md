## START THE APPLICATION
* From project directory, start up application by running 
`docker compose up`

Or 

* running the 2 docker files seperatli and creating a shared volume between them

    Build the model training image and the prediction image:

    `docker build -t cross-train -f Dockerfile_train .`

    `docker build -t cross-predict -f Dockerfile_predict .`
    `docker build -t cross-predict -f C:\Users\User\Desktop\Data_Science\final project step 3\model\Dockerfile .`


    Run the cross-train container with a volume mounting:

    `docker run -v <absolute path to your data_predict directory>:/usr/src/app/data_predict cross-train`


    Run the cross-predict container with a volume mounting and port mapping:

    `docker run -p 5000:5000 -v C:\Users\User\Desktop\Data_Science\final project step 3\train:/usr/src/app/train cross-predict`
