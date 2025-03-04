# python-voters
nominee_1=input("enter the nominee 1 name : ")
nominee_2=input("enter the nominee 2 name : ")
nom_1_votes=0
nom_2_votes=0
voters_id=[1,2,3,4,5,6,7,8,9,10]
num_of_voter=len(voters_id)
while True:
    if voters_id==[]:
        print("voting session over")
        if nom_1_votes>nom_2_votes:
            percent=(nom_1_votes/num_of_voters)*100
            print(nominee_1,"HAS WON","with",percent,"%votes")

        elif nom_2_votes>nom_1_votes:
            percent=(nom_2_votes/num_of_voters)*100
            print(nominee_2,"HAS WON","with",percent,"%votes")    
    else:    
         voter=int(input("Enter your voter id no: "))
    if voter in voters_id:
        print("You are a voter ")
        voters_id.remove(voter)
        vote=int(input("Enter your vote 1 or 2 : "))
        if vote==1:
            nom_1_votes+=1
            print("THANK YOU FOR VOTING")
        elif vote==2:
            nom_2_votes+=1
            print("THANK YOU FOR VOTING ")
    else:
        print("YOU ARE NOT A VOTER HERE OR YOU HAVE ALREADY VOTED ")
