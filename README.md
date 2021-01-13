import java.util.Scanner;

public class CovidTransmission {
    public static void main(String[] args){

Scanner sc = new Scanner(System.in); 

int firstDay = sc.nextInt(); 
int firstHour = sc.nextInt(); 
int firstMinute = sc.nextInt();
int secondDay = sc.nextInt();
int secondHour = sc.nextInt();
int secondMinute = sc.nextInt();

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

                
