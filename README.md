# LA1400
package SudenasEser;
import robocode.*;

public class Sunnydoge extends JuniorRobot

{
 
	public void run() {
    

	while (true) {
      	ahead(100);
      	turnGunRight(360);
      	back(100);
      	turnGunRight(360);
   		}
  	}
	
	public void onScannedRobot() {
		turnGunTo(180);
		fire(2);
		back(50);
		turnGunTo(45);
		turnTo(scannedDistance);	
	}
	
	public void onHitByBullet() {
		turnAheadRight(100, 50);
		turnLeft(360);
		back(10);		
	}

	public void onHitWall() {
		back(30);
		turnLeft(80);
		fire(1);
	}	

    public void scannedHeading() {
		if (scannedDistance>10){
		fire(2);
		}
	}
}
