#include<stdio.h>
#include<conio.h>
#include<string.h>

struct all
{
   long f1,f,tp,bal,total;
}a;

void check()
{
   if((a.bal-a.tp)>=0)
   {
       //	printf("\033[36m\nTotal Price : %ld",a.tp);

	a.bal-=a.tp;
	a.f=0;
	a.f1=1;
	a.total += a.tp;
	printf("\nBalance Amount : %ld",a.bal);
	printf("\033[32m\n\nPurchase Successfully");

   }
   else
   {
     a.f=1;
     printf("\033[33mInsufficient Amount in account\n");
     delay(2000);

   }
}
void main()
{
    int option,nop=0;

    long dep,wid,qt;
    char con[5],pass[15],cpass[15],ac[9],vbal[5],name[15];

    clrscr();

    a.bal = 100;

    rac:

    printf("\033[36m\nEnter Your A/C Number : ");
    scanf("%s",&ac);



    if(strlen(ac)<10 && strlen(ac)>8)
    {
	printf("Enter User Name : ");
	scanf("%s",&name);

	rpass:

	printf("\033[36m\n\nCreate Password : ");
	scanf("%s",&pass);

	if(strlen(pass)<8)
	{
	   // printf("Confirm Password : ");
	   // scanf("%s",&cpass);

	    if(strcmp(pass,pass)==0)
	    {

	       a.total =0;
	       printf("\033[32m\nAccount created Successfully");

	       delay(2000);
	       clrscr();

	       rcon:

	       printf("\033[36m\t\t\t\t1.Deposite\n\t\t\t\t2.Widthrawel\n\t\t\t\t3.Exit\n\nYour Choice : ");
	       scanf("%d",&option);

	       if(option==1)
	       {
		  clrscr();

		  printf("\t\t\t\tDeposite\n\nEnter amount : ");
		  scanf("%ld",&dep);

		  a.bal += dep;

		  printf("\033[32m\n\nBalance Amount = %ld",a.bal);

		  getch();
		  clrscr();

		  snacks:

		  printf("\033[36m\n\t\t\t\t1.Snacks\n\t\t\t\t2.Food\n\t\t\t\t3.Movies\n\t\t\t\t4.Exit\n\nYour Choice : ");
		  scanf("%d",&option);

		  if(option==1)
		  {
		     clrscr();

		      res:
		     printf("\n\t\t\t\t1.Dairy Milk\3 - 40.00Rs\n\t\t\t\t2.Kit Kat - 50.00Rs\n\t\t\t\t3.Munch - 5.00Rs\n\t\t\t\t4.5star - 10.00Rs\n\t\t\t\t5.Unibic - 10.00Rs\n\t\t\t\t6.Exit\n\nYour Choice : ");
		     scanf("%d",&option);

		     fs:
		     if(option==1)
		     {
			 printf("Your order is Dairy Milk\3\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 40 * qt;
			 check();
		     }

		     else if(option==2)
			{
			 printf("Your order is Kit kat\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 50 * qt;
			 check();
		     }

		     else if(option==3)
		     {
			 printf("Your order is Munch\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 5 * qt;

			 check();

		     }

		     else if(option==4)
		     {
			 printf("Your order is 5star\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp= 5 * qt;
			 check();
		     }

		     else if(option==5)
		     {
			 printf("Your order is Unibic\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 10 * qt;
			 check();
		     }
		     if(option>5)
		     {
			goto snacks;
		     }

		     if(a.f1==1)
		     {
			 printf("\nDo you wanted to continue again(yes or no): ");
			  scanf("%s",&con);

			  if(strcmp(con,"Yes")==0||strcmp(con,"yes")==0)
			  {
			     goto fs;
			   }
			   else
			   {
			      goto res;
			   }

		     }
		     if(a.f==1)
		     {
			 goto fs;
		     }
		     goto end;

		  }

		  if(option==2)
		  {
		     clrscr();

		     ref:
		     printf("\033[36m\n\t\t\t\t1.Biriyani\3 - 140.00Rs\n\t\t\t\t2.Dosai - 25.00Rs\n\t\t\t\t3.Tomato Rice - 50.00Rs\n\t\t\t\t4.KFG Chicken- 210.00Rs\n\t\t\t\t5.Barota - 20.00Rs\n\t\t\t\t6.Exit\n\nYour Choice : ");
		     scanf("%d",&option);

		     s:
		     if(option==1)
		     {
			 printf("Your order is Biriyani\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 140 * qt;
			 check();
		     }

		     else if(option==2)
		     {
			 printf("Your order is Dosai\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 25 * qt;
			 check();
		     }

		     else if(option==3)
		     {
			 printf("Your order is Tomato Rice\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 50 * qt;
			 check();
		     }

		     else if(option==4)
		     {
			 printf("Your order is KFG Chicken\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp=210 * qt;
			 check();
		     }

		     else if(option==5)
		     {
			 printf("Your order is Barota\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 20 * qt;
			 check();
		     }
		     if(option>5)
		     {
			goto snacks;
		     }

		     if(a.f==1)
		     {
			 goto s;
		     }

		     if(a.f1==1)
		     {
			 printf("\nDo you wanted to continue again(yes or no): ");
			  scanf("%s",&con);

			  if(strcmp(con,"Yes")==0||strcmp(con,"yes")==0)
			  {
			     goto s;
			   }
			   else
			   {
			      goto ref;
			   }

		     }
		     goto end;
		  }

		  if(option==3)
		  {
		     clrscr();

		     rem:
		     printf("\033[36m\n\t\t\t\t1.Raayan - 440.00Rs\n\t\t\t\t2.Leo - 150.00Rs\n\t\t\t\t3.Thunivu - 150.00Rs\n\t\t\t\t4.KGF Chapter 2- 110.00Rs\n\t\t\t\t5.Kalki - 220.00Rs\n\t\t\t\t6.Exit\n\nYour Choice : ");
		     scanf("%ld",&option);

		     m:
		     if(option==1)
		     {
			 printf("Your order is Raayan Movie\n\n");

			 printf("Quantity : ");
			 scanf("%d",&qt);

			 a.tp = 440 * qt;
			 check();
		     }

		     else if(option==2)
		     {
			 printf("Your order is Leo Movie\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 150 * qt;
			 check();
		     }

		     else if(option==3)
		     {
			 printf("Your order is Thunivu Movie\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 150 * qt;
			 check();
		     }

		     else if(option==4)
		     {
			 printf("Your order is KGK Chapter 2 Movie\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp=110 * qt;
			 check();
		     }

		     else if(option==5)
		     {
			 printf("Your order is Kalki Movie\n\n");

			 printf("Quantity : ");
			 scanf("%ld",&qt);

			 a.tp = 220 * qt;
			 check();
		     }

		     if(option>5)
		     {
			goto snacks;
		     }


		     if(a.f==1)
		     {

			 goto m;

		     }

		     if(a.f1==1)
		     {
			 printf("\nDo you wanted to continue again(yes or no): ");
			  scanf("%s",&con);

			  if(strcmp(con,"Yes")==0||strcmp(con,"yes")==0)
			  {
			     goto m;
			   }
			   else
			   {
			      goto rem;
			   }

		     }
			goto snacks;
		  }

	       }
	       else if(option == 2)
	       {
		   rp:																																																																																																																															      			   printf("\033[36mPassword :");
		   scanf("%s",&cpass);

		   if(strcmp(pass,cpass)==0)
		   {
		       clrscr();

		       printf("\033[35mWelcome %s",name);

		       rw:

		       printf("\033[36m\n\nEnter Amount : ");
		       scanf("%ld",&wid);

		       if(a.bal-wid>=0)
		       {
			   a.bal-=wid;
			   if(wid>0)
			   {
				   printf("\n\nWithdrawed successfully");
				   printf("\n\nBalance Amount : %ld",a.bal);
			   }
		       }

		       else
		       {
			  printf("\033[33m\n\nInsufficient Amount in Account");

			  delay(1000);

			  printf("\nDo you wanted to view balance(yes or no): ");
			  scanf("%s",&vbal);

			  if(strcmp(vbal,"yes")==0||strcmp(vbal,"Yes")==0)
			  {
			      printf("\033[32mBalance Amount : %ld",a.bal);
			      getch();
			  }



			  goto rw;

		       }


			printf("\nDo you wanted to continue again(yes or no): ");
			  scanf("%s",&con);

			  if(strcmp(con,"Yes")==0||strcmp(con,"yes")==0)
			  {
			     goto rw;
			   }

			   else
			   {
			      goto rcon;
			   }

		   }

		   else
		   {

		      nop++;
		      printf("\033[33mInvalid Password");

		      if(nop>3)
		      {
			 goto end;
		      }
		      delay(1000);

		      goto rp;
		   }

	       }

	    }

	}

	else
	{
	   printf("\033[33mInvalid Password\n");

	   delay(1000);

	   goto rpass;
	}

    }

    else
    {

       printf("\033[33m\nInvalid A/C No");

       delay(1000);

       goto rac;
    }

    end:

    if(a.f1==1)
    {
	 printf("\n\nTotal Price = %ld\n\n",a.total);
    }
    printf("\nDo you wanted to continue again(yes or no): ");
    scanf("%s",&con);

    if(strcmp(con,"Yes")==0||strcmp(con,"yes")==0)
    {
       goto rcon;
    }

   // getch();
}

