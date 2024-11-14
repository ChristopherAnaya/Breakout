# Breakout 
    #Initialize game
    Initialize game grid (15x30)
    Initialize score = 0

    #Start game loop
    While Running:
        Display current score and level
        Spawn 150 blocks
        Spawn player
        Spawn ball
        Block health = level divided by 5 no remainder + 1
        ball speed = level divided by 3 no remainder + 1
        Move ball down
        
        When user clicks:
            change center x coordinate of player to mouse x
        
        When ball hits player:
            reverse the balls y speed
        
        When ball hits block:
            specific block health - 1
            if specific block health is equal to 0:
                destroy that block
                score += 1
                spawn power up if user gets lucky
                powerup down speed set to 1
        
        If no blocks left:
            level + 1
            restart code with increase level and score
        
        If user hits powerup:
            if powerup is big:
                user size X2 for 15 seconds
            if powerup is freeze:
                freeze ball for 5 seconds
            if powerup is speedup:
                increase speed * 3 for 15 seconds
            if powerup is slowdown:
                decrease speed / 3 for 15 seconds
            if powerup is double:
                spawn another ball
        
        If ball goes below map:
            destroy ball
        
        If no balls left:
            end game