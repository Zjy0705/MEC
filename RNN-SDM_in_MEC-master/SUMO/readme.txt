SUMO部分
我们使用SUMO生成我们的数据集和仿真数据。

介绍
该目录包含两个子目录：new 和 old。

旧部分步骤
旧部分使用 sumo.exe 生成所有仿真数据。第一步，我们需要修改 osm.sumocfg 文件。然后，使用 SUMO 打开该文件。你也可以使用命令行来操作：

bash
复制代码
run.bat
在得到 fulloutput.xml 文件后，我们需要使用 SUMO 提供的工具 xml2csv.py，运行以下命令：

bash
复制代码
python xml2csv.py fulloutput.xml -o fulloutput.csv
最后，我们可以运行 readcsv.py 来生成 veh.csv 文件。

新部分步骤
新部分使用 traci 包。我们只需要运行 sumo.py 文件，就可以得到 veh.csv 和 ped.csv 文件。