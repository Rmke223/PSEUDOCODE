/Pseudocode for David Blaines ascension Altimiter/

Functionality-This ALitimiter will read the current altitude and rate of ascent/decent and will also display important prompts thoughout the flight. 

David starts his ascent
watch will measure altitiude and rate ascent/descent
Watch will prompt David to put on his parachute at 8,000 feet
watch will tell David to apply breathing apparatus at 15,000 feet
Watch will tell david to detach at 25,000 feet
watch will tell david to open his parachute at 7,000 alt

Objects-
Watch- houses all components
Power button- turns watch on and off
Proccessor- internal processor that read ALT and Converts Delta ALT/(Delta TIME*60)
Alt/Rate screen - displays the current altitude and rate of acent/descent
Message screen- displays important messsages
Internal altimiter- measures alititude
Battery- powers watch

Variables-
POWER="ON or OFF"
ALT="altitude"
RATE="DELTA Alt/(Delta Time*60)"  ft/minute
Time="Time"

START Program
Power button is ON

Battery supplies power to all components

//Proccesor sending ALT and RATE to screen continuously while turned on//

While Power is ON
Proccessor GET ALT from Altimiter
Proccessor COMPUTE RATE
Proccessor Display ALT and RATE on Alt/Rate Screen
End WHILE

// conditions for message screen//

While Power is on
IF RATE is > 0 and ALT is between 8,000 ft and 9,000 ft
    DISPLAY on message screen "Put on Parachute"

ELSE IF RATE is > 0 and ALT is beteen 15,000 and 25,000 ft
    DISPLAY on message screen "Use breathing aparatus"

ELSE IF RATE is > 0 and ALT is > 25,000 ft
    DISPLAY on message screen "Release from balloons"

ELSE IF RATE is < 0 and ALT is < 7,000 ft 
    DISPLAY on message screen "Deploy Parachute" 
ELSE
    DISPLAY Nothing
end WHILE

Power Button OFF
END program