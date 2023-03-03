Virtuoso:
  model name 必须为 N_50(使用analoglib和0.5um.lib.scs进行验证时)
  MDE环境仿真时OUTPUT点击instance端口输出为电流current(纵坐标)，点击线为电压voltage(纵坐标) (横坐标为parameter)
  Pin中in out不是变量，可应通过vdc接上in pin去给in赋值，变量只能设在完整的instance器件的输入值内
  DC:
  Design variables可以copy from design即为可设变量，Design variables为定值，DC仿真时，parameter可设variables函数（constant变扫描值sweep），同时Design variables值将被覆写
