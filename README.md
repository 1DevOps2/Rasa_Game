### Dockerized_Rasa_Game (rock, paper & scissors)

#### Clone this Repo
    git clone https://github.com/1DevOps2/Rasa_Game.git

#### Create network
    docker network create mynet
    
#### Train the model
    docker run -it --rm --user 1001 --network mynet -p5055:5055 -v $(pwd):/app rasa/rasa:3.0.0 shell 
    
#### Run Actions
    docker run -it --rm --user 1001 --name actions --network mynet -v $(pwd):/app rasa/rasa:3.0.0 run actions 

#### Run the Rasa Shell
    docker run -it --rm --user 1001 --network mynet -p5055:5055 -v $(pwd):/app rasa/rasa:3.0.0 shell 
