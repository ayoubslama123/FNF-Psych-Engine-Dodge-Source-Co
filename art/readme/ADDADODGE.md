# Open Playstate.hx in source 

# And Find This :

function dodge(ableToDodge:Bool = false)

# And Type in This Code 

if(curSong.toLowerCase() == 'your-song'){
			if(ableToDodge){
				FlxG.sound.play(Paths.sound('dodge1'));
				FlxG.cameras.flash(FlxColor.RED, 0.5);
				FlxG.cameras.shake(0.05, 0.5);
			new FlxTimer().start(0.09, function(tmr:FlxTimer){
				if (!dodging){
					FlxG.sound.play(Paths.sound('dodge1'));
					health -= 10069;
				}
			});
			}
			else{
				FlxG.sound.play(Paths.sound('dodge1'));
			}
			}
 
 # After That Find This 
 
 super.update(elapsed);
 # And Type After The Code This :
 
 
 if (curSong.toLowerCase() == "your-song"){
	        if(FlxG.keys.justPressed.SPACE && !dodging && ableToDodge){
		        dodging = true;
		        boyfriend.playAnim('dodge');
		        boyfriend.debugMode = true;
		        boyfriend.holdTimer = 0.7;
	        new FlxTimer().start(dodgeTimer, function(tmr:FlxTimer)
		    {
		        dodging = false;
		        boyfriend.dance();
		    });
	        new FlxTimer().start(0.7, function(tmr:FlxTimer)
		    {
		        boyfriend.debugMode = false;
		    });
	        new FlxTimer().start(dodgeCooldown, function(tmr:FlxTimer) 
		    {
			    ableToDodge = true;
		    });
	    }
      
 # Find This :
 
 callOnLuas('onStepHit', []);
 
 # And Type This :
 
 if (curSong.toLowerCase() == "pico"){
			switch (curStep){
				case The-Time:
					add(alert);
					dodgeWarn(true);
				case The-Time+5:
					dodgeWarn(true);
				case The-Time+10:
					dodge(true);
			}
