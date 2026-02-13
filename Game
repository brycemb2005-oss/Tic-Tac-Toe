import javax.swing.*;
import java.awt.*;
import javax.swing.border.*;
import java.util.Scanner;

public class GUI {

    private final JTextField[] fields;

    public GUI() {
        JFrame frame = new JFrame();

        JLabel label = new JLabel("Number of clicks: 0");

        JButton button = new JButton("Calculate");

        JPanel panel = new JPanel();
        panel.setBorder(BorderFactory.createEmptyBorder(200, 200, 200, 200));
        panel.setLayout(new GridLayout(5, 3));

        fields = new JTextField[9];

        for (int i = 0; i < 9; i++) {
            fields[i] = new JTextField(3);
            fields[i].setHorizontalAlignment(JTextField.CENTER);
            panel.add(fields[i]);
        }

        panel.add(new JLabel());
        panel.add(new JLabel());

        button.addActionListener(e -> {
            String[] values = new String[9];

            for (int i = 0; i < 9; i++) {
                values[i] = fields[i].getText();
            }

            Calculate(values);

//            System.out.println("Button clicked!");
        });

        panel.add(button);

        frame.add(panel, BorderLayout.CENTER);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setTitle("Tic Tac Toe");
        frame.pack();
        frame.setVisible(true);

    }
    public static void main(String[] args) {

        new GUI();
    }
    public void Calculate(String[] x) {
        int no = 0;
        String[] box = new String[9];
        for (int i = 0; i < 9; i++) {
            box[i] = fields[i].getText();
        }
        for (int i = 0; i < 9; i += 3) {
            if ((!box[i].isEmpty()) && box[i].equals(box[i + 1]) && box[i].equals(box[i + 2])) {
                System.out.println(box[i] + " is the Winner!");
                no++;
            }
        }
        for (int i = 0; i < 3; i++) {
            if (!(box[i].isEmpty()) && box[i].equals(box[i + 3]) && box[i].equals(box[i + 6])) {
                System.out.println(box[i] + " is the Winner!");
                no++;
            }
        }
        if (!(box[0].isEmpty()) && box[0].equals(box[4]) && box[0].equals(box[8])) {
            System.out.println(box[0] + " is the Winner!");
            no++;
        }
        if (!(box[2].isEmpty()) && box[2].equals(box[4]) && box[2].equals(box[6])) {
            System.out.println(box[2] + " is the Winner!");
            no++;
        }
        if (no < 1) {System.out.println("It's a draw!");}
        }
    }
