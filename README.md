# Splunk Example

## Objective 

The Splunk Example is to emulate an scenario when data needs to be visualized. Mimicing real-world case scenarios allow me to show my experience with Splunk, documentation, and acts as a guide to any aspiring CyberSecurity Professionals to understand the tool. 

### Skill Learned

- Ability to generate data and visualize the data.
- Allows for easier and more stream line communication with parties that arent to familiar with the profession.
- Development of critical thinking and problem-solving skills in CyberSecurity.

### Tools Used

- Splunk

### Steps

1. Selecting Log

![image](https://github.com/user-attachments/assets/25217502-06f0-4833-a598-fd35de127b92)

- Since this is an example of using Splunk I will be using the "Local event log collection" as this will emulate what use-case will look in the real world. 

2. Local Host and Selecting Logs for Ingestion

![image](https://github.com/user-attachments/assets/a3a05141-c3ac-4b16-a078-3aecea80081d)
![image](https://github.com/user-attachments/assets/1596c8b7-9834-40a5-bad5-2e78c1261a88)

- I have selected Application, Security, and Systems as they are the foundational logs that any company would need briefings on. 
[For those trying to emulate: I encourage that after you try what I have done go back and select different logs as practice, thank me later ;)]

3. Make Sure Status is Enabled

![image](https://github.com/user-attachments/assets/944037ce-253e-49e6-828c-dbc684f2cba5)

- This step is self explanitory, however, note under the status table the logs must be enabled. Sometimes this step is looked over and people will be confused as to why their data is showing incorrectly or missing, its always good to double check. 

![image](https://github.com/user-attachments/assets/d1aa75d4-c617-47bc-800e-c43551161c50)

- After this head over back to Search and Reporting. 

4. Search With The * Symbol

- This is where you will will see the logs of your selected injest pop up. Remember this is for local systems only and remote systems will be handled differently.
[Since this is handling local systems I will not post a screenshot here for privacy reasons but I will keep it detailed so you can still follow along.]

5. Event Viewer

![image](https://github.com/user-attachments/assets/71b31dc5-4c9e-4e66-b383-1cf6f0fc56e0)

- Every windows machine there is an application known as Event Viewer, open that.
- (for added information: Event Viewer is an application where significant events on your computer is logged like crashes, application crashes, downloaded updates, and so on. This is especially useful when it comes to troubleshooting on windows)

![image](https://github.com/user-attachments/assets/670d730a-8ad8-414d-b436-7b909f70c1f0)
![image](https://github.com/user-attachments/assets/5da4ca58-2f91-44a6-89ec-296ea720386a)


- For this example: Go under "Windows Logs" and right click "Security" and they "Clear Log".

6. Learning More About Narrowing Searches.

- Go back to your Splunk and go to one of the logs that popped up after you searched *.
- You will find that the values displayed can be clicked on.
- Click on "host =" and your system name. What this will do is narrow down the search to your specific computer. (note: this will be added to the search bar)

![image](https://github.com/user-attachments/assets/790e5230-f745-48bb-b5aa-e7a5e42b6897)

- Narrow it down further by clicking on "source = WinEventLog:Security".
- Now do the same with "EventCode = 1102", if your code is different then your calling a different event and though it may look different essentially the steps are the same.

![image](https://github.com/user-attachments/assets/b1f3c662-466d-460f-9b0a-99c3c46511f9)

- If you want to know more about Event code for windows go to www.ultimatewindowssecurity.com and you can find them there. They also have codes on SQL, SharePoint, and more. 

7. Event Log

- Once you have done step 5 and 6 properly expand the Event Log that we narrowed down and you should get this result:
  
  ![image](https://github.com/user-attachments/assets/92685c8a-95e9-41f8-91ed-a063e592e4c5)

- If you did not get this please repeat step 5 and 6.
- Searching in Splunk is the only way you can get the exact information you need for a specific visual diagram. Knowing how the search function works is vital to how you interact with Splunk or else you will be displaying wrong information. Some companies will set up Splunk in different ways, but the core of Splunk remains the same.

![image](https://github.com/user-attachments/assets/2e09bcf5-c30f-4669-ae1d-e77b0255ad61)

- You can go to the top right and "Create Table View" so that you can see the same log in a table.

![image](https://github.com/user-attachments/assets/5a620127-f1a9-4319-90f5-7878e36e30d6)

- Deselect "raw" and you should see in the table view the fields you have selected.

8. Creating A Dashboard

![image](https://github.com/user-attachments/assets/ec136170-6096-403b-9b43-e8fc0c0e117e)
![image](https://github.com/user-attachments/assets/0f69cb2d-6c8d-4c11-9f52-bd896aa1f253)

- Go to "Dashboard" and select "Create New Dashboard".

![image](https://github.com/user-attachments/assets/8176b46a-3842-4f2c-b313-63fbf771187f)
![image](https://github.com/user-attachments/assets/5942a93a-5bd3-4247-b0a3-b0b5866f3be1)
![image](https://github.com/user-attachments/assets/d28e59c1-71f8-4617-9774-0792c55f2722)

- You can name it whatever you want but for the purpose of this I will name it "Clear Logs" and I have selected "Dashboard Studio".
(note: There is additional functionality here and I implore everyone who is following along to come back to this step and try out the different features of Dashboard)

![image](https://github.com/user-attachments/assets/1e049bbf-c6c0-4157-ad47-6aba28914865)
![image](https://github.com/user-attachments/assets/f2e73155-1cbd-49f8-a05e-6dc460fc3816)

- This is what it should look like and go ahead and click on "Add Chart" and "Table"

![image](https://github.com/user-attachments/assets/34663398-643e-4f42-a126-5402cd620ff0)

- On the right there is a query called "Search with SPL". Add in the search that you have used to get to the specific "Clear Log" that you found in Step 7.
- Apply and Close. Then Save. 
[You can customise this as much as you like]

- Go back to Dashboard

![image](https://github.com/user-attachments/assets/ebfb278d-e1f0-4dad-88b4-8c2207bb8b89)

- You should see your created dashboard and if you were to click on the "Clear Logs" then you will be sent back to your table. You can also set this as your home dashboard and though I will not do it in this example it is very useful to use in a company as the amount of reports that you might need to refer back to can be a lot and having the one dashboard that aids in those reports on your home page can save a lot of time. 













