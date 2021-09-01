# c-Labs-Yoobee
Beginners programming.  
//CS120-Lab 4: A game site wants to selebrae the top players whose scores are calculated out of 10.000 points.//

#include <iostream>
#include <ctime>
#include <cstdlib>
using namespace std;
int main(){
    //Declaring variables and Arrays //
    float smallestscore = 0, largestscore=0, average,total=0,s_temp=0;
    string names[10]={};
    float scores[10]={};
    int a1_temp;
    string a2_temp;
    
    for(int i=0;i<10;i++){                   // Taking name and scores of the player as input from the user //
        cout<<"Enter the name of the player "<<i+1<<":";
        cin>>names[i];
        cout<<"Enter the score of the player (Scores 5000 or less will be ignored) : ";
        cin>>scores[i];
        if(scores[i] > 5000.00){              //Storing score greater than 5000//
         total+= scores[i];
            
        }
            else{
                scores[i]=scores[i];
            }
    }
    cout<<endl;
    cout<<"*****************************"<<endl;
    cout<<names[0]<<":"<<scores[0]<<endl;                // Displaying names and scores//
    cout<<names[1]<<":"<<scores[1]<<endl;
    cout<<names[2]<<":"<<scores[2]<<endl;
    cout<<names[3]<<":"<<scores[3]<<endl;
    cout<<names[4]<<":"<<scores[4]<<endl;
    cout<<names[5]<<":"<<scores[5]<<endl;
    cout<<names[6]<<":"<<scores[6]<<endl;
    cout<<names[7]<<":"<<scores[7]<<endl;
    cout<<names[8]<<":"<<scores[8]<<endl;
    cout<<names[9]<<":"<<scores[9]<<endl;
    cout<<endl<<endl;
    cout<<"Average,Minimun and Maximun scores."<<endl;
    cout<<"*************************************"<<endl;
    
    smallestscore=scores[0];                                     //Comparing the largest against the smallest score //
    largestscore=scores[0];
    string smallestname,largestname,n_temp;
    smallestname=names[0];largestname=names[0];
    for(int i=0;i<10;i++)
    {
        s_temp= scores[i];
        n_temp=names[i];
        if(s_temp<smallestscore)
            smallestscore = s_temp;
        if(n_temp<smallestname)
            smallestname = n_temp;
        if(s_temp >largestscore)
           largestscore = s_temp;
        if( n_temp>largestname)
            largestname= n_temp;
    }
    cout<<"The smallest score is :"<<smallestscore<<endl;
    cout<<"The largest score is :"<<largestscore<<endl;
    
    average=total/10;                                  //Displaying Average//
    cout<<"Average scores :"<<average<<endl<<endl;
    
    
    for(int i=0;i<10;i++)                        // Comparing the scores and displaying it with respective names//
    {
    
    for(int j=i+1;j<10;j++)
        {
        if(scores[i]<scores[j])
            {
                a1_temp= scores[i];
                scores[i]= scores[j];
                scores[j]= a1_temp;
            }
            if(names[i]<names[j])              //I dont know how to linked the scores with the names correctly //
            {
                a2_temp=names[i];
                names[i]=names[j];
                names[j]=a2_temp;
            }
        }
    }
    for(int i=0;i<10;i++)
    {
        cout<<names[i]<<":"<<scores[i]<<endl;
    }
    
        
        return 0;
