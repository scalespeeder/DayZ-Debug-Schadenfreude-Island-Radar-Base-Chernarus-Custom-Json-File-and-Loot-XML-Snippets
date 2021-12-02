DayZ Chernarus "Debug / Schadenfreude Island" Radar Base For Console and PC xml json Mod Instructions & Terms Of Use

Limited Testing on PC Chernarus Local Server DAYZ Version 1.15 Dec 2021.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

Many Thanks To Inclement Dab for his amazing DayZ Editor that makes this all possible: https://steamcommunity.com/sharedfiles/filedetails/?id=2250764298

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "debug-island-radar-base.json" from the extracted files to inside the "custom" folder of the mission directory on your server. This file places the structures on your map.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "objectSpawnersArr" line.

This file tells your server to access your custom file.

Edit it to look like this: 

	"objectSpawnersArr": ["custom/debug-island-radar-base.json"]
	
If you already are calling custom jsons to spawn items, seperate the files like this:

	"objectSpawnersArr": ["custom/debug-island-radar-base.json","custom/differentfile.json"]
	
Save your changes & upload if you need to.
	
Next we add loot to the structures by adding the following code snippet to the top of your mapgrouppos.xml file, after <map> 

	<!--Debug Island Radar Base-->
	<group name="Land_Airfield_Radar_Tall" pos="23944.982422 36.738117 -1.097624" rpy="0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Tisy_RadarB_Antenna" pos="23990.599609 14.268700 5.345870" rpy="0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Container_1Mo" pos="23905.900391 6.367820 -40.507301" rpy="0.000000 0.000000 -71.665298" a="161.665"/>
	<group name="Land_Boathouse" pos="24001.576172 -1.643426 78.536201" rpy="0.000000 0.000000 179.077042" a="-89.077"/>
	<group name="Land_Lighthouse" pos="23846.148438 17.277359 -0.816868" rpy="0.000000 0.000000 -172.874039" a="-97.126"/>
	<group name="Land_Tower_TC3_Red" pos="23908.900391 11.533900 -0.497612" rpy="0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Boat_Small5" pos="24030.960938 1.837780 54.190998" rpy="25.339096 -6.374843 -39.326687" a="129.327"/>
	<group name="Land_Boat_Small4" pos="24018.777344 2.069895 61.015694" rpy="22.813478 10.211865 -84.697754" a="174.698"/>
	<group name="Land_Boat_Small1" pos="23989.761719 1.036187 68.526665" rpy="-10.128533 -20.004414 19.404274" a="70.5957"/>
	<group name="Land_Boat_Small2" pos="23984.236328 1.277480 67.466133" rpy="20.429209 -11.208196 -67.214813" a="157.215"/>
	<group name="Land_Boat_Small1" pos="24039.542969 0.927003 47.991688" rpy="15.519989 -18.589903 0.000000" a="90"/>
	<group name="Land_Boat_Small6" pos="24068.806641 4.066626 -22.301147" rpy="16.240669 13.896249 0.000000" a="90"/>
	<group name="Land_Boat_Small1" pos="24021.632813 0.834649 -56.755760" rpy="10.033657 19.707825 0.000000" a="90"/>
	<group name="Land_Boat_Small2" pos="24016.277344 1.747393 -56.990101" rpy="-21.247856 -11.810697 -142.915421" a="-127.085"/>
	<group name="Land_Boat_Small4" pos="23916.679688 1.335447 -53.692497" rpy="4.104912 -17.374340 176.799713" a="-86.7997"/>
	<group name="Land_Mil_Radar_Mobile1" pos="23893.800781 5.253440 -51.385899" rpy="0.000000 0.000000 16.001202" a="73.9988"/>
	<group name="Land_Tisy_RadarPlatform_Top" pos="23897.476563 -2.008708 -52.604149" rpy="0.000000 0.000000 -162.536316" a="-107.464"/>
	<group name="Land_Pier_Crane_A" pos="23927.496094 3.935210 -58.155338" rpy="0.000000 0.000000 13.000895" a="76.9991"/>
	<group name="Land_Pier_Crane_B" pos="23928.699219 16.979601 -63.183899" rpy="0.000000 0.000000 69.499992" a="20.5"/>
	<group name="Land_Mil_Radar_Mobile1" pos="23954.306641 6.413409 -62.642120" rpy="0.000000 -0.000000 9.001192" a="80.9988"/>
	<group name="Land_Tisy_RadarPlatform_Top" pos="23957.982422 -0.848739 -63.860371" rpy="0.000000 -0.000000 -169.536057" a="-100.464"/>
	<group name="Land_Mil_Radar_Mobile1" pos="24011.103516 6.259100 -67.487938" rpy="0.000000 0.000000 -28.789881" a="118.79"/>
	<group name="Land_Tisy_RadarPlatform_Top" pos="24014.578125 -1.003048 -65.793503" rpy="0.000000 0.000000 152.672623" a="-62.6726"/>
	<group name="Land_Pier_Crane_A" pos="24039.937500 4.940869 -48.802418" rpy="0.000000 0.000000 -31.790270" a="121.79"/>
	<group name="Land_Pier_Crane_B" pos="24044.322266 17.985260 -51.551075" rpy="0.000000 0.000000 24.709503" a="65.2905"/>
	<group name="Land_Mil_Radar_Mobile1" pos="24062.269531 7.419067 -33.287239" rpy="0.000000 -0.000000 -35.789886" a="125.79"/>
	<group name="Land_Tisy_RadarPlatform_Top" pos="24065.755859 0.156920 -31.593611" rpy="0.000000 -0.000000 145.673004" a="-55.673"/>
	<group name="Land_Container_1Mo" pos="23904.835938 6.385160 -43.649391" rpy="0.000000 0.000000 -71.665298" a="161.665"/>
	<group name="Land_Guardhouse" pos="23897.099609 6.372880 -34.795700" rpy="0.000000 0.000000 18.000000" a="72"/>
	<group name="Land_Mil_Barracks_Round" pos="23967.900391 7.333180 -53.118599" rpy="0.000000 0.000000 10.099999" a="79.9"/>
	<group name="Land_Container_1Mo" pos="24015.968750 7.384741 -51.964275" rpy="-0.000000 -0.000000 59.638702" a="30.3613"/>
	<group name="Land_Container_1Mo" pos="24014.400391 7.394660 -48.563202" rpy="0.000000 0.000000 60.499989" a="29.5"/>
	<group name="Land_Container_1Mo" pos="24014.128906 9.805468 -51.340492" rpy="-0.000000 -0.000000 152.879822" a="-62.8798"/>
	<group name="Land_Container_1Moh" pos="24016.992188 9.891673 -49.366779" rpy="-0.000000 -0.000000 -23.004637" a="113.005"/>
	<group name="Land_Mil_Barracks_Round" pos="24061.607422 8.642440 -15.762491" rpy="0.000000 0.000000 54.416199" a="35.5838"/>
	<group name="Land_Container_1Mo" pos="23938.900391 0.226610 -60.309601" rpy="-2.728400 21.354498 0.000000" a="90"/>
	<group name="Land_Boathouse" pos="23846.414063 -1.939742 53.144539" rpy="-0.000000 -0.000000 -178.918747" a="-91.0813"/>
	<group name="Land_Boat_Small1" pos="23831.509766 1.537132 42.024757" rpy="-6.829530 9.440339 131.023560" a="-41.0236"/>
	<group name="Land_Boat_Small1" pos="23826.728516 1.703855 39.685673" rpy="-10.641398 5.345831 93.449409" a="-3.44941"/>
	<group name="Land_Boat_Small1" pos="23813.054688 1.253070 31.527020" rpy="8.642005 -10.999508 -86.550407" a="176.55"/>
	<group name="Land_Boat_Small6" pos="23865.652344 1.362425 50.956673" rpy="-0.629651 -13.206900 0.000000" a="90"/>
	<group name="Land_Ruin_House_1W05" pos="23868.667969 10.416043 -1.116286" rpy="-9.550150 -1.288836 -82.502144" a="172.502"/>
	<group name="Land_Ruin_House_1W12" pos="23842.041016 7.127908 20.448538" rpy="6.637724 -7.858255 -55.164616" a="145.165"/>
	<group name="Land_Misc_Toilet_Mobile" pos="23964.802734 7.570514 -47.839127" rpy="-0.000000 -0.000000 7.674180" a="82.3258"/>
	<group name="Land_Misc_Toilet_Mobile" pos="24067.400391 8.683760 -16.878599" rpy="0.000000 0.000000 58.899982" a="31.1"/>
	<group name="Land_Pier_Crane_A" pos="23941.582031 3.577277 67.376572" rpy="0.000000 0.000000 177.783661" a="-87.7837"/>
	<group name="Land_Pier_Crane_B" pos="23939.125000 16.621670 71.930893" rpy="0.000000 0.000000 -125.715744" a="-144.284"/>
	<group name="Land_Tisy_RadarPlatform_Top" pos="23911.300781 -1.206670 57.351002" rpy="0.000000 0.000000 -20.253099" a="110.253"/>
	<group name="Land_Misc_Well_Pump_Blue" pos="23986.892578 24.077950 -0.779106" rpy="-0.000000 -0.000000 0.000000" a="90"/>
	<group name="Land_Mil_ATC_Small" pos="23913.699219 15.950300 50.721298" rpy="0.000000 0.000000 -111.583000" a="-158.417"/>
	
Save your changes & upload if you need to.

Restart your server and the new structures will appear immediatly, and then they will slowly stock with loot.

Thanks, Rob.
