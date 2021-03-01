# Hello-World
public class Test4 {
    public static void main(String[] args) {
        Base64.Encoder encoder = Base64.getEncoder();
        String str = "name=中国?password=123456";
        String s = encoder.encodeToString(str.getBytes());
        System.out.println(s);
        System.out.println("=-==============");
        Base64.Decoder decoder = Base64.getDecoder();
        byte[] decode = decoder.decode(s);
        System.out.println(new String(decode));
    }
