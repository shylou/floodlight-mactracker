floodlight-mactracker
=====================

根据官方文档写的mactracker模块
-----------------------------
该模块是按照floodlight的[官方文档](http://docs.projectfloodlight.org/display/floodlightcontroller/How+to+Write+a+Module)进行编写的(br)
它的主要功能是发现并记录新的mac地址，并将其接入交换机   
该模块的路径为：floodlight\src\main\java\net\floodlightcontroller下   
需要注意的是，模块写好后必须注册模块才能加载，步骤如下：   
    要使floodlight启动时加载新模块，必须要让加载器知道新模块的存在，在src\main\resources\META-INF\services\IFloodlightModule文件上添加模块名：   
    net.floodlightcontroller.mactracker.MACTracker   
    然后将模块的信息添加到floodlight的缺省配置文件src\main\resources\floodlightdefault最后，注意各个模块间要用逗号隔开：   
    floodlight.moudules=<leave the default list of moudles in place>,   
    net.floodlightcontroller.mactracker.MACTracker
