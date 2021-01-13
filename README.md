import java.util.Scanner;
public class CovidTransmission {
    public static void main(String[] args){

Scanner Covid = new Scanner(System.in); 

int firstDay = Covid.nextInt(); 
int firstHour = Covid.nextInt(); 
int firstMinute = Covid.nextInt();
int secondDay = Covid.nextInt();
int secondHour = Covid.nextInt();
int secondMinute = Covid.nextInt();

int finalDay = (secondDay - firstDay) * 24 * 60;
int finalHour = (secondHour - firstHour) * 60;
int finalMinute = (secondMinute - firstMinute);

int finalContact = finalDay + finalHour + finalMinute;
    if(finalContact <= 60 && finalContact > 0) {
        System.out.println(finalContact + " low");
    }
    else if(finalContact >= 60 && finalContact <= 180 ) {
        System.out.println(finalContact + " medium");
    }
    else if(finalContact > 180 && finalContact <= 360) {
        System.out.println(finalContact + " high");
    }
    else if(finalContact > 360) {
        System.out.println(finalContact + " HIGH");
    }
    else {
        System.out.println("-1 -1");
    }
}
}

                
