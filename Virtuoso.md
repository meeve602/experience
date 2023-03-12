Virtuoso:
  model name 必须为 N_50(使用analoglib和0.5um.lib.scs进行验证时)
  MDE环境仿真时OUTPUT点击instance端口输出为电流current(纵坐标)，点击线为电压voltage(纵坐标) (横坐标为parameter)
  Pin中in out不是变量，可应通过vdc接上in pin去给in赋值，变量只能设在完整的instance器件的输入值内
  DC某个点点电压，直流  (静态工作点，数值变化引起的电压变化，画图为点电压连成线)(直流电压没有时间常数，所有值都是直接算出，类似电容有时间函数的器件直流过不去)
  tran某个瞬态电压，交流+直流  (DC趋向于点取值，tran用于画变化曲线)
  AC微变电压(不可求)，交流  求比值(放大倍数AV，电阻RO,RI)(微变等效)
  DC:
  Design variables可以copy from design即为可设变量，Design variables为定值，DC仿真时，parameter可设variables函数（constant变扫描值sweep），同时Design variables值将被覆写、
  查看原器件点电压时须在DC中勾选save DC op才能查看
  DC voltage显示最大最小，tran voltage显示某一时刻值
  Operating Points ---Vth Vds Vgs    Node voltages ---Vd Vg Vs
  AC：
  Design variables（V）不会被覆写，将被设为定值，电源(VDC)中的magnitude(交流量幅值)需要被设定
  查看单个线的output(相位角phase 幅值log20 magnitude )需要到schematic中单击线右键在下属plot中查看（ADE面板不可用？）
  正弦交流电中magnitude为标量（AC仿真），amplitude为矢量幅值(0到几)(tran仿真)
  math:
  当值相同时，变化率(导数)相同会使接下来的值相同，多重导数拟合函数(泰勒展开式) 人为调节值到某个值到定值，再调节其变化率使信号稳定。
  Parametric Analysis:
  会对方框内的值换参数(额外)后仿真，方框*分析数
  BJT&MOS：
  BJT阈值为前提，顺序电压 MOS阈值为前提，减去阈值相比电压
  Lable:
  lable相同则连线，gnd线lable应为gnd! ,vss线线lable应为vss! gnd!一定为0V vss!值一定不变
  ADE XL:
  CORNER AANALYSIS
  ADE GXL:
  OPTIMATTON
  opamp&inp
  opamp电压传递器，inp电流复制器
  
  Math:
    导数意义：单个固定电阻，U/I可以求出其电阻，为一比例，且其斜线过0点 
              mos管电阻，为非线性电阻，使用dU/dI可以求出其电阻，用来求比例，其斜线不一定过0点，但公式定义为电压除以电流，即u/i没有意义，只看某一电压时的电阻~du/di(导的组合性)
              用来求某一点对应的比例，不能用来求值，是比例（组合）值
