import java.util.Random;
import java.util.Scanner;

public class loopAndSwitch {
	public static void main(String[] args){
		int loopCounter =1;
		Random rand = new Random();
		int randNum = rand.nextInt(5)+1;
		Scanner input = new Scanner(System.in);
		double ua, ub, uc, ud;
		
		//Getting user-values from user
		System.out.print("What is your score for ua?");
		ua = input.nextInt();
		System.out.print("What is your score for ub?");
		ub = input.nextInt();
		System.out.print("What is your score for uc?");
		uc = input.nextInt();
		System.out.print("What is your score for ud?");
		ud = input.nextInt();
		
		//Assigning user-values to user-array
		double user[] = {ua, ub, uc, ud};
		
		double tempUser[] = {0, 0, 0, 0};
		
		
		//given score of goods
		int score;
		double car[] = {3, 3, 3, 3};
		double purse[] = {3, 3, 3, 3};
		double computer[] = {3, 3, 3, 3};
		double flower[] = {3, 3, 3, 3};
		double game[] = {3, 3, 3, 3};
		double good[] = {0, 0, 0, 0};
		
		while(loopCounter<=3){
			switch(randNum){
			case 1:
				System.out.println("case 1");
				System.out.println("On a scale of 1 to 5 how much do you like cars?");
				score = input.nextInt();
				for (int i = 0; i < car.length; i++) {
		            good[i] = car[i];
		        }
				switch(score){
				case 1:
					for (int counter=0; counter<user.length; counter++){
							if(user[counter] >= good[counter]){
							tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
							good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
						}
						else{
							tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
							
							good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
							
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				case 2:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
				
						System.out.println("User's scores: ");
						for(int counter=0; counter<user.length; counter++){
							System.out.print(user[counter]+ ", ");
						}
						System.out.println("\nGood's scores: ");
						for(int counter=0; counter<good.length; counter++){
							System.out.print(good[counter]+ ", ");
						}
					
					break;
				
				case 3:
					
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 4:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
					System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 5:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				}
				//assigns placeholder good-array values to car array
				for (int i = 0; i < good.length; i++) {
		            car[i] = good[i];
		        }
				loopCounter++;
				randNum = rand.nextInt(5)+1;
				break;
			case 2:
				System.out.println("case 2");
				System.out.println("On a scale of 1 to 5 how much do you like purses?");
				score = input.nextInt();
				for (int i = 0; i < purse.length; i++) {
		            good[i] = purse[i];
		        }
				switch(score){
				case 1:
					for (int counter=0; counter<user.length; counter++){
							if(user[counter] >= good[counter]){
							tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
							good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
						}
						else{
							tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
							
							good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
							
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				case 2:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
				
						System.out.println("User's scores: ");
						for(int counter=0; counter<user.length; counter++){
							System.out.print(user[counter]+ ", ");
						}
						System.out.println("\nGood's scores: ");
						for(int counter=0; counter<good.length; counter++){
							System.out.print(good[counter]+ ", ");
						}
					
					break;
				
				case 3:
					
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 4:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
					System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 5:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				}
				//assigns placeholder good-array values to car array
				for (int i = 0; i < good.length; i++) {
		            purse[i] = good[i];
		        }
				loopCounter++;
				randNum = rand.nextInt(5)+1;
				break;
				
			case 3:
				System.out.println("case 3");
				System.out.println("On a scale of 1 to 5 how much do you like computers?");
				score = input.nextInt();
				for (int i = 0; i < computer.length; i++) {
		            good[i] = computer[i];
		        }
				switch(score){
				case 1:
					for (int counter=0; counter<user.length; counter++){
							if(user[counter] >= good[counter]){
							tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
							good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
						}
						else{
							tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
							
							good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
							
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				case 2:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
				
						System.out.println("User's scores: ");
						for(int counter=0; counter<user.length; counter++){
							System.out.print(user[counter]+ ", ");
						}
						System.out.println("\nGood's scores: ");
						for(int counter=0; counter<good.length; counter++){
							System.out.print(good[counter]+ ", ");
						}
					
					break;
				
				case 3:
					
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 4:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
					System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 5:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				}
				//assigns placeholder good-array values to car array
				for (int i = 0; i < good.length; i++) {
		            computer[i] = good[i];
		        }
				loopCounter++;
				randNum = rand.nextInt(5)+1;
				break;
				
			case 4:
				System.out.println("case 4");
				System.out.println("On a scale of 1 to 5 how much do you like flowers?");
				score = input.nextInt();
				for (int i = 0; i < flower.length; i++) {
		            good[i] = flower[i];
		        }
				switch(score){
				case 1:
					for (int counter=0; counter<user.length; counter++){
							if(user[counter] >= good[counter]){
							tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
							good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
						}
						else{
							tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
							
							good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
							
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				case 2:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
				
						System.out.println("User's scores: ");
						for(int counter=0; counter<user.length; counter++){
							System.out.print(user[counter]+ ", ");
						}
						System.out.println("\nGood's scores: ");
						for(int counter=0; counter<good.length; counter++){
							System.out.print(good[counter]+ ", ");
						}
					
					break;
				
				case 3:
					
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 4:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
					System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 5:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				}
				//assigns placeholder good-array values to car array
				for (int i = 0; i < good.length; i++) {
		            flower[i] = good[i];
		        }
				loopCounter++;
				randNum = rand.nextInt(5)+1;
				break;
				
			case 5:
				System.out.println("case 5");
				System.out.println("On a scale of 1 to 5 how much do you like games?");
				score = input.nextInt();
				for (int i = 0; i < purse.length; i++) {
		            good[i] = game[i];
		        }
				switch(score){
				case 1:
					for (int counter=0; counter<user.length; counter++){
							if(user[counter] >= good[counter]){
							tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
							good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
						}
						else{
							tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
							
							good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
							user[counter] = tempUser[counter];
							
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				case 2:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
				
						System.out.println("User's scores: ");
						for(int counter=0; counter<user.length; counter++){
							System.out.print(user[counter]+ ", ");
						}
						System.out.println("\nGood's scores: ");
						for(int counter=0; counter<good.length; counter++){
							System.out.print(good[counter]+ ", ");
						}
					
					break;
				
				case 3:
					
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 4:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/4;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
						else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/4;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/4;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
					System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				
				case 5:
					for (int counter=0; counter<user.length; counter++){
						if(user[counter] >= good[counter]){
						tempUser[counter] = user[counter] - Math.abs(user[counter]-good[counter])/2;
					
						good[counter] = good[counter] + Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					else{
						tempUser[counter] = user[counter] + Math.abs(user[counter]-good[counter])/2;
						
						good[counter] = good[counter] - Math.abs(user[counter]-good[counter])/2;
						user[counter] = tempUser[counter];
						}
					}
					System.out.println("User's scores: ");
					for(int counter=0; counter<user.length; counter++){
						System.out.print(user[counter]+ ", ");
					}
					System.out.println("\nGood's scores: ");
					for(int counter=0; counter<good.length; counter++){
						System.out.print(good[counter]+ ", ");
					}
					break;
				}
				//assigns placeholder good-array values to car array
				for (int i = 0; i < good.length; i++) {
		            game[i] = good[i];
		        }
				loopCounter++;
				randNum = rand.nextInt(5)+1;
				break;
			default:
				System.out.println("default case");
				loopCounter++;
				randNum = rand.nextInt(5)+1;
				break;
			
			}
			
		}
		
		System.out.println("\nWhile Loop Exited");
		
	}

}
