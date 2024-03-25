# base-humanoid-robot-xml-for-mujoco


mujoco_humanoid_detailed_comments.xml 为mujoco官方提供的humanoid模型的部分源码的详细注释，用于学习xml语法

### body
- `torso`（躯干）: 这是机器人的中心身体部分，位置设置在`(0 0 1.5)`，具有一个球形的几何形状，尺寸为0.14。
- `head`（头部）: 位于躯干正上方，具有一个球形的几何形状，尺寸为0.1。
- `lower_waist`（下腰部）: 位于躯干下方，有一个胶囊形状的几何体。
- `pelvis`（骨盆）: 在下腰部下方，包含一个名为“butt”的球形几何体。
- `right_thigh`（右大腿）: 从骨盆出发，具有一个长方体的几何形状。
- `right_shin`（右小腿）: 接在右大腿下方，有一个长方体的几何形状。
- `right_foot`（右脚）: 包含两个长方体的几何形状，模拟脚部结构。
- `left_thigh`（左大腿）: 与右大腿相似，但位置相对称。
- `left_shin`（左小腿）: 与右小腿相似，位置相对称。
- `left_foot`（左脚）: 与右脚相似，包含两个长方体的几何形状。
- `right_upper_arm`（右上臂）: 在躯干右侧，有一个长方体的几何形状。
- `right_lower_arm`（右前臂）: 接在右上臂下方，有一个长方体的几何形状。
- `right_hand`（右手）: 在右前臂末端，是一个球形的几何体。
- `left_upper_arm`（左上臂）: 与右上臂相似，但位置相对称。
- `left_lower_arm`（左前臂）: 与右前臂相似，位置相对称。
- `left_hand`（左手）: 在左前臂末端，是一个球形的几何体。
### joint
- `root`（根关节）: 位于躯干，是一个自由关节。
- `abdomen_x`、`abdomen_y`、`abdomen_z`（腹部关节）: 位于下腰部，分别控制躯干的三个方向的旋转。
- `right_hip_x`、`right_hip_y`、`right_hip_z`（右髋关节）: 控制右大腿的三个方向的运动。
- `right_knee`（右膝关节）: 控制右小腿的弯曲。
- `right_ankle_x`、`right_ankle_y`（右脚踝关节）: 控制右脚的两个方向的运动。
- `left_hip_x`、`left_hip_y`、`left_hip_z`（左髋关节）: 与右髋关节相似，但位置相对称。
- `left_knee`（左膝关节）: 与右膝关节相似，位置相对称。
- `left_ankle_x`、`left_ankle_y`（左脚踝关节）: 与右脚踝关节相似，位置相对称。
- `right_shoulder1`、`right_shoulder2`（右上肩关节）: 控制右上臂的两个方向的运动。
- `right_elbow`（右肘关节）: 控制右前臂的弯曲。
- `left_shoulder1`、`left_shoulder2`（左上肩关节）: 与右上肩关节相似，但位置相对称。
- `left_elbow`（左肘关节）: 与右肘关节相似，位置相对称。
### geom
- `floor`（地面）: 定义了一个平面几何体，作为机器人的站立面。

- `torso`（躯干几何体）: 是一个球形的几何体，代表躯干的形状。

- `head`（头部几何体）: 是一个球形的几何体，代表头部的形状。

- `lower_waist`、`pelvis`、`right_thigh`、`right_shin`、`right_foot`、`left_thigh`、`left_shin`、`left_foot`、`right_upper_arm`、`right_lower_arm`、`right_hand`、`left_upper_arm`、`left_lower_arm`、`left_hand`（各种身体部位的几何体）: 这些几何体定义了对应身体部位的形状、大小和颜色。

  

  在模型定义中，每个`geom`和`joint`都可以有特定的属性，如尺寸、位置、范围、摩擦系数、阻尼和刚度等

### motor
- `abdomen_y`（腹部Y轴电机）: 用于驱动腹部绕Y轴的旋转，齿轮比为40。

- `abdomen_z`（腹部Z轴电机）: 用于驱动腹部绕Z轴的旋转，齿轮比为40。

- `abdomen_x`（腹部X轴电机）: 用于驱动腹部绕X轴的旋转，齿轮比为40。

- `right_hip_x`（右髋X轴电机）: 用于驱动右大腿绕X轴的旋转，齿轮比为40。

- `right_hip_z`（右髋Z轴电机）: 用于驱动右大腿绕Z轴的旋转，齿轮比为40。

- `right_hip_y`（右髋Y轴电机）: 用于驱动右大腿绕Y轴的旋转，齿轮比为120。

- `right_knee`（右膝关节电机）: 用于驱动右小腿的弯曲，齿轮比为80。

- `right_ankle_x`（右脚踝X轴电机）: 用于驱动右脚绕X轴的旋转，齿轮比为20。

- `right_ankle_y`（右脚踝Y轴电机）: 用于驱动右脚绕Y轴的旋转，齿轮比为20。

- `left_hip_x`（左髋X轴电机）: 用于驱动左大腿绕X轴的旋转，齿轮比为40。

- `left_hip_z`（左髋Z轴电机）: 用于驱动左大腿绕Z轴的旋转，齿轮比为40。

- `left_hip_y`（左髋Y轴电机）: 用于驱动左大腿绕Y轴的旋转，齿轮比为120。

- `left_knee`（左膝关节电机）: 用于驱动左小腿的弯曲，齿轮比为80。

- `left_ankle_x`（左脚踝X轴电机）: 用于驱动左脚绕X轴的旋转，齿轮比为20。

- `left_ankle_y`（左脚踝Y轴电机）: 用于驱动左脚绕Y轴的旋转，齿轮比为20。

- `right_shoulder1`、`right_shoulder2`（右上肩电机）: 用于驱动右上臂的两个方向的运动，齿轮比为20。

- `right_elbow`（右肘关节电机）: 用于驱动右前臂的弯曲，齿轮比为40。

- `left_shoulder1`、`left_shoulder2`（左上肩电机）: 与右上肩电机相似，但位置相对称，齿轮比为20。

- `left_elbow`（左肘关节电机）: 与右肘关节电机相似，位置相对称，齿轮比为40。

  

  每个`motor`元素都通过`gear`属性指定了与关节连接的齿轮比，这是电机输出力和关节运动速度之间的比例。通过`joint`属性，每个电机都与一个特定的关节相关联，从而控制该关节的运动。电机的其他属性（如控制范围和控制是否受限）在`default`部分中进行了定义。
  
  ```xml
      <actuator>
          <motor name="abdomen_y"       gear="40"  joint="abdomen_y"/>
          <motor name="abdomen_z"       gear="40"  joint="abdomen_z"/>
          <motor name="abdomen_x"       gear="40"  joint="abdomen_x"/>
          <motor name="right_hip_x"     gear="40"  joint="right_hip_x"/>
          <motor name="right_hip_z"     gear="40"  joint="right_hip_z"/>
          <motor name="right_hip_y"     gear="120" joint="right_hip_y"/>
          <motor name="right_knee"      gear="80"  joint="right_knee"/>
          <motor name="right_ankle_x"   gear="20"  joint="right_ankle_x"/>
          <motor name="right_ankle_y"   gear="20"  joint="right_ankle_y"/>
          <motor name="left_hip_x"      gear="40"  joint="left_hip_x"/>
          <motor name="left_hip_z"      gear="40"  joint="left_hip_z"/>
          <motor name="left_hip_y"      gear="120" joint="left_hip_y"/>
          <motor name="left_knee"       gear="80"  joint="left_knee"/>
          <motor name="left_ankle_x"    gear="20"  joint="left_ankle_x"/>
          <motor name="left_ankle_y"    gear="20"  joint="left_ankle_y"/>
          <motor name="right_shoulder1" gear="20"  joint="right_shoulder1"/>
          <motor name="right_shoulder2" gear="20"  joint="right_shoulder2"/>
          <motor name="right_elbow"     gear="40"  joint="right_elbow"/>
          <motor name="left_shoulder1"  gear="20"  joint="left_shoulder1"/>
          <motor name="left_shoulder2"  gear="20"  joint="left_shoulder2"/>
          <motor name="left_elbow"      gear="40"  joint="left_elbow"/>
        </actuator>
  ```
  
  