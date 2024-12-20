# CS-370

### We were given two python files that were setting up aspects of the code and allowed us to reference parts of the code we had to write and allowed us to focus on the Agent AI to find the treasure. Those python files were the GameExperience.py and the TreasureMaze.py.

### We were responsible for writing the AI Agent. It's goal was to find the treasure before the human could.

    "   ``` 
    "    ### edited code begins
    "    for epoch in range(n_epoch):
    "        #    Agent_cell = randomly select a free cell
    "        agent_cell = np.random.randint(0, high=7, size=2)
    "    
    "        #    Reset the maze with agent set to above position
    "        qmaze.reset([0, 0])
    "        #    envstate = Environment.current_state
    "        envstate = qmaze.observe()
    "    
    "        # init
    "        loss = 0
    "        n_episodes = 0
    "    
    "        #        While state is not game over:
    "        #        previous_envstate = envstate
    "        #        Action = randomly choose action (left, right, up, down) either by exploration or by exploitation
    "    
    "        while qmaze.game_status() == 'not_over':
    "            previous_envstate = envstate
    "            valid_actions = qmaze.valid_actions()
    "            if np.random.rand() < epsilon:
    "                action = random.choice(valid_actions)
    "            else:
    "                action = np.argmax(experience.predict(envstate))
    "            
    "            #        envstate, reward, game_status = qmaze.act(action)        
    "            envstate, reward, game_status = qmaze.act(action)
    "            n_episodes += 1
    "            episode = [previous_envstate, action, reward, envstate, game_status]
    "            experience.remember(episode)
    "            
    "            inputs,targets = experience.get_data()
    "            history = model.fit(inputs, targets, epochs= 10, batch_size=12, verbose=0)
    "        
    "            loss = model.evaluate(inputs, targets)
    "        
    "            if episode [4] == \"win\":
    "                win_history.append(1)
    "                win_rate = sum(win_history) / len(win_history)
    "                break
    "                
    "            if episode [4] == 'lose':
    "                win_history.append(0)
    "                win_rate = sum(win_history) / len(win_history)
    "                break
    "                
    "            if win_rate > epsilon:
    "                print(\"win_rate is: \", win_rate)
    "    
    "    ###edited code ends
    "    ```

