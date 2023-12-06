<h1>Python - Building an Algorithm to Update a File</h1>

<h2>Description</h2>
In this lab simulation, I take on the role of a security professional at a large organization. At my organization, access to restricted content is controlled with an allow list of IP addresses. The "allow_list.txt" file identifies these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this content. I created an algorithm to automate updating the "allow_list.txt" file and remove these IP addresses that should no longer have access. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b>

<h2>Environments Used </h2>

- <b>Jupyter Notebook</b> 

<h2>Program walk-through:</h2>


<b>Task 1.) Assign Variables:</b>

My first task is to assign variables to both the <b>“allow_list.txt”</b> file as well as the provided list of ip addresses that need to be removed: <br />
<br />

![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/0b12f5e5-2f10-4cd8-b2f4-d27605841e22)

<br />
<br />
<br />

<b>Task 2.) Open the file that contains the allow list:</b>

Next, I used a <b>with</b> statement to open the file: <br />
<br />

![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/7be862c1-8ab2-4d9a-8d62-9072b661e305)

<br />
The <b>with</b> statement is used along with the <b>.open()</b> function in <b>“r”</b> (read mode) to open the allow list file and read the contents. The <b>as</b> keyword was also used to assign a variable named <b>file</b>, which will store the output.

<br />
<br />
<br />
<br />
<br />

<b>Task 3.) Read the file contents:</b>  <br />

Then, I called the <b>.read()</b> function within the body of the <b>with</b> statement, which converts the file into a string, allowing me to read the contents: <br />
<br />

![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/0848f4b2-bed2-4aae-b3a1-baf1bb814b18)

<br />
I also assigned a variable to the string output, called <b>ip_addresses</b>.

<br />
<br />
<br />
<br />
<br />

<b>Task 4.) Convert the string into a list:</b> <br/>

To be able to remove IP addresses individually from the allow list I first used the <b>.split()</b> function to convert the <b>ip_addresses</b> from a string into a list: <br />
<br />

![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/b44dad36-9c1b-4df2-9fe4-4b734d8a2711)

<br />
I also reassigned this list back to the variable <b>ip_addresses</b> in order to save it.

<br />
<br />
<br />
<br />
<br />

<b>Task 5.) Iterate through the remove list:</b>  <br />

I needed to ensure that my algorithm would iterate through all of the IP addresses contained within the <b>ip_addresses</b> list. I used a <b>for</b> loop to manage this: <br />
<br />

![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/89b773b5-973c-4133-a000-a3a136cdf1c0)

<br />
In Python, the <b>for</b> loop will repeat code for a given sequence. I used <b>element</b> as the loop variable as well as the keyword <b>in</b> to iterate through each value.

<br />
<br />
<br />
<br />
<br />

<b> Task 6.) Remove IP addresses that are on the remove list:</b>  <br/>

My next task was to remove any IP address that was found both within the <b>ip_addresses</b> allow list, as well as the <b>remove_list</b>, here is my code for this step:  <br />
<br />

![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/b6d9a70e-eca5-4deb-9c90-af46fe124fd4)

<br />
I created a conditional statement which determined if the <b>element</b> loop variable was found in the <b>remove_list</b> or not. I also applied the <b>.remove()</b> function to <b>ip_addresses</b> so that any element found within both would be automatically removed.

<br />
<br />
<br />
<br />
<br />

<b> Task 7.) Update the file with the revised list of IP addresses:</b>  <br/>

My last task with this algorithm was to then update the original allow list file with the newly revised list of IP addresses. First, I used the <b>.join()</b> function to convert the list back into a string:  <br />
<br />

![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/9efcf611-b750-4bfd-862c-5901bbedce20)

<br />
After the list was converted back into a string, I passed it along as part of an argument in a <b>.write()</b> function to write to the <b>“allow_list.txt”</b> file:<br />
<br />

![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/21efe746-058c-4228-95fe-9bd9b89bdbd2)

<br />
I used the <b>.open()</b> function combined with the <b>import_file</b> and <b>“w”</b> arguments to begin the process of writing the new string data to the file. Finally, using the <b>.write()</b> function I input the <b>ip_addresses</b> argument to have the file rewritten.<br />
<br />


<br />
<br />
<br />

<b> Summary:</b>  <br/>

I crafted an algorithm in Python, utilizng the Jupyter Notebook environment, to remove IP addresses that were identified on a remove list from the approved ip adresses located in the <b>“allow_list.txt”</b> file. I incorporated a wide variety of functions, a loop iteration, and a conditional statement to accomplish this objective. <br />

Here is my code in full for this algorithm:<br />
<br />

![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/e7837b7f-2c37-4de7-b1ad-0fb40a6f48f7)
![image](https://github.com/J-DONDA/Python_BuildingAnAlgorithm/assets/116527248/a9d96e53-bb73-46dd-80d8-d81c276abb4c)

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
