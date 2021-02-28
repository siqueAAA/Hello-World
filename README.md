# Hello-World
public class Test2 {
    public static void main(String[] args) throws Exception {
        // 需求:编写程序,修改a.txt中k3键对应的值为java
        // 1.创建Properties对象
        Properties pro = new Properties();

        // 2.调用load方法加载a.txt文件中的键值对到Properties对象中
        pro.load(new FileInputStream("day11\\eee\\db.properties"));

        // 3.获取Properties对象中的所有键
        Set<String> keys = pro.stringPropertyNames();

        // 4.循环遍历所有的键
        for (String key : keys) {
            // 5.在循环中,判断遍历出来的键是否是k3,如果是,就修改值为java
            if (key.equals("k3")){
                pro.setProperty(key,"java");
            }
        }
        System.out.println("pro:"+pro);
