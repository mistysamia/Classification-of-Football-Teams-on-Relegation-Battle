<h1>It is a project using the Oracle PL/SQL . </h1>

• Task Approach:
There are different football leagues where each season different teams participate representing 
various clubs. Throughout one season, the poorly performing teams have to face relegation battles 
and in some leagues, the three teams with least points are relegated while some others survive. In 
this project work, using the K Nearest Neighbor classification approach, teams will be classified 
as Relegation Survivor or Relegated based on different criteria in regards to the information from 
previous seasons.


• Database Schema:

-> Global Schema
Teamlist(teamID, teamName , country, seasonId )
PerformanceList(perID, teamID, win , lost , draw, gf ,ga,points )
RelegationBattle(relID,perID, rbStatus)
RecordList(recID,win,lost,draw,gf,ga,points, predictedStatus)

-> Fragmentation Schema
Teamlist1= SLSeasonID=1 Teamlist
Teamlist2= SLSeasonID=2 Teamlist
Teamlist3= SLSeasonID=3 Teamlist
PerformaceList1= SLpoints<35 PerformanceList
PerformaceList2= SLpoints>=35 PerformanceList

-> Allocation Schema
Teamlist1 , Teamlist2 , PerformaceList1, PerformaceList2, RelegationBattle, Record at sites 1 , 2



• Significance of Distributed Database System:
While working on classification approach, the most important task is to maintain the data properly 
so that the approach can make proper predictions. Distributed database systems allow data 
decentralization which can help with classification tasks. Scaling can be done more conveniently 
in distributed systems without making huge changes to the whole system. Data maintenance, 
expansion, reliability can be ensured more efficiently for classification tasks with distributed 
systems compared to centralized systems