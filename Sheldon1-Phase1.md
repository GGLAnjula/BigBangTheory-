First of all we need to extact the bigbangtheory **_.zip file._** It contains files called **sheldon1** and **sheldon2**. Before execute those files we need to give execute permissions and run it.

![chmod-sheldon](https://user-images.githubusercontent.com/36528620/76437496-a8425e00-63df-11ea-8675-102bf65456f7.PNG)

![sheldon1-2](https://user-images.githubusercontent.com/36528620/76442252-a8922780-63e6-11ea-968a-8b973ace37b8.PNG)

Then use **gdb** with **_sheldon1_**

![gdb sheldon1-3](https://user-images.githubusercontent.com/36528620/76442319-c8295000-63e6-11ea-9816-87c14cbbd3f5.PNG)

Using function called **_info functions_** which is available under **gdb** we can view all available functions inside **sheldon1** file.

![info function-4](https://user-images.githubusercontent.com/36528620/76442619-366e1280-63e7-11ea-99d5-a4cee47008b9.PNG)

After that set **_disasembly flavor_** as **_intel_** and execute that. Then **disassemble** the **main** function.

![disassemble main-6](https://user-images.githubusercontent.com/36528620/76442953-b1cfc400-63e7-11ea-8140-c24f23a86050.PNG)

![info function1-5](https://user-images.githubusercontent.com/36528620/76443384-56520600-63e8-11ea-9eac-aebca22e655d.PNG)

Under **main** function, there is a special function called **_phase_1_**. Identify that function.

![phase1-7](https://user-images.githubusercontent.com/36528620/76443264-2acf1b80-63e8-11ea-9120-f57a204b53ce.PNG)

Use **_disassemble_** command to disassemble the above identified  **phase_1** function.

![disassemble phase1-8](https://user-images.githubusercontent.com/36528620/76443560-a03aec00-63e8-11ea-8ba1-d9eee7ddfc5c.PNG)

Inside the **phase_1** function there is a instruction named **_test_** and that is the program checking the values of eax and eax and there is a static push to the stack which locate 4 lines before.
Finally you can print out the string value of this memory address using **_x/s_** and get the passphrase for **phase_1**.

![xs mem-add-9](https://user-images.githubusercontent.com/36528620/76444569-273c9400-63ea-11ea-8625-a755f516dad2.PNG)
