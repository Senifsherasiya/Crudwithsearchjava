import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
public class Main extends JFrame implements ActionListener {
    private JButton button;
    private JTextField textField;
    private JPanel panel;
    public Main() {
        panel = new JPanel();
        textField = new JTextField("Type some text here", 20);
        button = new JButton("Accept");
        button.addActionListener(this);
        panel.add(textField);
        panel.add(button);
        getContentPane().add(panel);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setSize(300, 200);
        setVisible(true);
    }
    public void actionPerformed(ActionEvent e) {
        String text = textField.getText();
        JOptionPane.showMessageDialog(null, text);
    }
    public static void main(String[] args) {
        new Main();
    }
}
