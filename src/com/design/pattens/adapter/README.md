# 适配器模式
####分类
    1、类适配器
    2、对象适配器 
    3、缺省适配器
####实现方式：
    1、类适配器（子类继承方式）
        a)目标抽象角色（定义客户要用的接口）
        
        b)适配器（实现a继承c，作为一个转换器被客户调用）
        
        c)待适配器（真正需要被调用的）
        
        d)客户端（借用a的实例调用c的方法
        
    2、对象适配器 （对象的组合方式）
        a)目标抽象角色（定义客户要用的接口）
        
        b)适配器（实现a，维护一个c的引用，作为一个转换器被d调用）
        
        c)待适配器（真正需要被调用的）
        
        d)客户端（此类，借用a类的实例调用c类的方法，类似静态代理，但是解决的问题不同）
        
    3、缺省适配器
        a)抽象接口
        
        b)实现a的适配器类（空实现）
        
        c)客户端，继承b，调用b中的方法，不必直接实现a（直接实现a需要实现a中的所有的方法）
####应用场景：
    
#####1、优点： 
        1.更好的复用性
        　　系统需要使用现有的类，而此类的接口不符合系统的需要。那么通过适配器模式就可以让这些功能得到更好的复用。
        2.更好的扩展性
            在实现适配器功能的时候，可以调用自己开发的功能，从而自然地扩展系统的功能。
         
#####2、缺点： 
        过多的使用适配器，会让系统非常零乱，不易整体进行把握。比如，明明看到调用的是A接口，其实内部被适配成了B接口的实现，一个系统
        如果太多出现这种情况，无异于一场灾难。因此如果不是很有必要，可以不使用适配器，而是直接对系统进行重构。
        
#####3、使用注意事项： 
        无
        
#####4、适用场景： 
    适配器模式把一个类的接口变换成客户端所期待的另一种接口，从而使原本因接口不匹配而无法在一起工作的两个类能够在一起工作。 
        无 
    以下都是单例模式的经典使用场景： 
        无
    应用场景举例： 
        无
#####5、实现场景
    假设一个手机充电器需要的电压是20V，但是正常的电压是220V，这时候就需要一个变压器，将220V的电压转换成20V的电压，这样，变压器就
    将20V的电压和手机联系起来了。
