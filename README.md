import java.util.Random;

public class Captcha {

    private static final String CHARACTERS = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";

    public static String generateCaptcha() {
        Random random = new Random();
        StringBuilder captcha = new StringBuilder();
        for (int i = 0; i < 6; i++) {
            captcha.append(CHARACTERS.charAt(random.nextInt(CHARACTERS.length())));
        }
        return captcha.toString();
    }

    public static void main(String[] args) {
        String captcha = generateCaptcha();
        System.out.println("Captcha: " + captcha);
    }
}
