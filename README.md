# DataTableFillToolsDocument

## Save Data Section

1. Make sure to enable the plugin
![0](https://github.com/QSWWLTN/DataTableFillToolsDocument/assets/52273933/18956f66-72a5-4bbc-b823-3001b00f0a7a)<br>

2. Fill in which types of functions need to be enabled. The blueprint type needs to add the _C mark after the blueprint name, as shown by the arrow; after the parent blueprint is configured, the subclass blueprint does not need additional configuration
![1](https://github.com/QSWWLTN/DataTableFillToolsDocument/assets/52273933/952f3268-7eea-4793-9182-ce69295a63d8)<br>

3. Make sure that the structure variable you need to save exists in your blueprint; for example, if I want to save a structure with the structure "DataTableTools_Test_Struct", I need to ensure that there is a variable of this structure in the configured blueprint ( Of course, multiple variables are also available, because they can be saved to different tables, this plug-in is saved and loaded by variable name, so please rest assured) as shown in the figure
![2](https://github.com/QSWWLTN/DataTableFillToolsDocument/assets/52273933/ab186cff-8a2d-4671-b527-90dc131bc0ff)<br>

4. Of course, this plug-in can save C++ structures, and supports nesting other types of structures, and does not even need to inherit the FTableRowBase type, it will automatically create yours in the /Game/ConfigDataTable/AutoCreateStruct directory when saving The structure used to save the data of the C++ structure name, the name is your C++ type name _Struct

5. Click "Self" in the component view, you will find a module named "DataTableTools" will appear in the details panel
![image](https://github.com/QSWWLTN/DataTableFillToolsDocument/assets/52273933/1cf4860e-bad8-4d1e-b995-51a7ac2c5998)<br>

6. Click the "Select StructValueName" drop-down box, you will see all the variable names in your blueprint here
![image](https://github.com/QSWWLTN/DataTableFillToolsDocument/assets/52273933/a0b66d15-b4bd-4ad4-b986-f75bff6ea3ba)<br>

7. Select the variable name you need to save, it will be displayed in the original drop-down box
![image](https://github.com/QSWWLTN/DataTableFillToolsDocument/assets/52273933/ecdf80e4-7946-447e-a203-b174bd942c49)<br>

8. First, let's assume that you are using this plugin for the first time or have not created a data table to save the content of this variable. Click the "+" button to create a data table for saving data. After clicking, a "Create DataTable Name" will appear "Input box
![image](https://github.com/QSWWLTN/DataTableFillToolsDocument/assets/52273933/c5370ecd-ec2c-4b3a-af09-1e64c4388dfd)<br>

9. After filling in the name of the data table you want to save, click the "SaveDataToDataTable" button. When the prompt is completed, the created data table will be located in the /Game/ConfigDataTable directory

10. If you have created a data table to save this structure before, or if you want to continue to modify it after creating it according to the above steps, please ensure that the data table is located in the /Game/ConfigDataTable directory, and the plug-in can only read the data table in this directory; <br> Please click "Select Target DataTable Name" (if you just clicked the "+" button, please press the "+" button again, it will return to the "Select Target DataTable Name" drop-down box) and select the data you need to modify table, click the "Save Data To DataTable" button again <br>
![image](https://github.com/QSWWLTN/DataTableFillToolsDocument/assets/52273933/d0f62118-3b9b-48ee-badd-572aa7123135)

## Load Data Section
1. If you want to read the data in the data table, please select the variable name you need to read and the name of the data table you need to read according to the save data section just now

2. Modify the value of the "ID" field in the variable, it will indicate which ID's data is read
![image](https://github.com/QSWWLTN/DataTableFillToolsDocument/assets/52273933/a7bd30a1-a166-4a86-b974-83d58b0c0d53)

3. Click the "Load Data From DataTable" button, it will overwrite the value of the variable in your blueprint (later versions will add the function of reading at runtime)
