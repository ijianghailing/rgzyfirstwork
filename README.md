# rgzyfirstworkd
package rgzyone;
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;
import java.util.*;
import java.math.*;
import java.io.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.FlowLayout;
import java.awt.event.ActionListener;
import java.io.File;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JTextField;
import javax.swing.JFileChooser;
import javax.swing.*;
import java.lang.*;
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class WCexe6 extends JFrame implements ActionListener{
	JButton btn =null;
	JTextField textField =null;
   public WCexe6() {
	   this.setTitle("选择文件窗口");
	   FlowLayout layout = new FlowLayout();
	   JLabel label=new FlowLayout();
	   textField =new JTextField(30);
	   btn =new JButton("浏览");
	   layout.setAlignment(FlowLayout.LEFT);
	   this.setLayout(layout);
	   this.setBounds(400,200,600,70);
	   this.setVisible(true);
	   this.setResizable(false);
	   this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	   btn.addActionListener(this);
	   this.add(label);
	   this.add(textField);
	   this.add(btn);
   }


@Override
public void actionPerformed(ActionEvent e) {
	// TODO Auto-generated method stub
	JFileChooser chooser =new JFileChooser();
	chooser.setFileSelectionMode(JFileChooser.FILES_AND_DIRECTORIES);
	chooser.showDialog(new JLabel(),"选择");
	File file=chooser.getSelectedFile();
	textField.setText(file.getAbsolutePath().toString());
	/*textField.setText("The number of char in the file selected is 20");
	textField.setText("The number of line in the file selected is 14");
	textField.setText("The number of word in the file selected is 10");
	*/
}
}
