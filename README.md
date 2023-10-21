# python-AI-21-
python+AI笔记(21)
# 二阶 - 一章 - 初识对象
#设计一个类
class Student:
  name = None  #记录学生姓名
  gender = None  
  nationality = None
  native_place = None
  age = None

#创建一个可以用的对象
stu_1 = Student()

#对象属性进行赋值
stu_1.name = "林军杰"
stu_1gender = "男"
stu_1.nationality = "中国"
stu_1.native_place = "山东省"
stu_1.age = 31

print(stu_1.name)
print(stu_1.gender)
print(stu_1.nationality)
print(stu_1.native_place)
print(stu_1.age)


# 二阶 - 一章 - 类的成员方法
#self关键字是成员方法定义的时候必须填写的
#它用来表示类对象自身的意思
#当我们使用类对象调用方法时，self会自动被python传入
#在方法内部，想要访问类的成员变量，必须使用self

#定义一个带有成员方法的类
class Student:
  name = None

  def say_hi(self):
    print("大家好呀，我是{self.name}，欢迎大家多多关照")  #想要在成员方法中访问成员变量，要带一个self

  def say_hi2(self,msg):
    print(f"大家好，我是:{self.name},{msg}")

stu = Student()
stu.name = "小明"
stu.say_hi()

stu = Student()
stu.name = "小明"
stu.say_hi2("balabala")


# 二阶 - 一章 - 类和对象
#设计一个闹钟类
class Clock:
  id = None
  price = None

  def ring(self):
    import winsound
    winsound.Beep(2000, 3000)

#构建2个闹钟对象并让其工作
clock1 = Clock()
clock1.id = "003032"
clock1.price = 19.99
print(f"闹钟ID:"{clock1.id},价格:{clock1.price}")
clock1.ring()
