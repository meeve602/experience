Virtuoso:
  model name 必须为 N_50(使用analoglib和0.5um.lib.scs进行验证时)
  MDE环境仿真时OUTPUT点击instance端口输出为电流current(纵坐标)，点击线为电压voltage(纵坐标) (横坐标为parameter)
  Pin中in out不是变量，可应通过vdc接上in pin去给in赋值，变量只能设在完整的instance器件的输入值内
  DC，tran求值，AC求比值(放大倍数AV，电阻RO,RI)
  DC:
  Design variables可以copy from design即为可设变量，Design variables为定值，DC仿真时，parameter可设variables函数（constant变扫描值sweep），同时Design variables值将被覆写、
  查看原器件点电压时须在DC中勾选save DC op才能查看
  DC voltage显示最大最小，tran voltage显示某一时刻值
  AC：
  Design variables（V）不会被覆写，将被设为定值，电源(VDC)中的magnitude(交流量幅值)需要被设定
  查看单个线的output(相位角phase 幅值log20 magnitude )需要到schematic中单击线右键在下属plot中查看（ADE面板不可用？）
  正弦交流电中magnitude为标量（AC仿真），amplitude为矢量幅值(0到几)(tran仿真)
  
