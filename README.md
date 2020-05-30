# calculatorwithJava

package Calculators;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JTextField;
import javax.swing.JButton;
import java.awt.Font;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.text.JTextComponent;
import java.awt.Color;
import java.awt.Window.Type;
import javax.swing.SwingConstants;

public class Calculator {

	private JFrame frmEureka;
	private JTextField textField;
	
	double firstnum;
	double secondnum;
	double result;
	String operations;
	String answer;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Calculator window = new Calculator();
					window.frmEureka.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public Calculator() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frmEureka = new JFrame();
		frmEureka.getContentPane().setForeground(Color.BLACK);
		frmEureka.setFont(new Font("Dialog", Font.BOLD, 12));
		frmEureka.setTitle("EUREKA");
		frmEureka.setBackground(Color.BLACK);
		frmEureka.setBounds(100, 100, 268, 348);
		frmEureka.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frmEureka.getContentPane().setLayout(null);
		
		textField = new JTextField();
		textField.setHorizontalAlignment(SwingConstants.RIGHT);
		textField.setBounds(70, 22, 170, 36);
		frmEureka.getContentPane().add(textField);
		textField.setColumns(10);
		
		//--------------------LINHA 1---------------------//
		
		JButton btn7 = new JButton("7");
		btn7.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				String EnterNumber = textField.getText() + btn7.getText();
				textField.setText(EnterNumber);
			}
		});
		btn7.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn7.setBounds(10, 69, 50, 50);
		frmEureka.getContentPane().add(btn7);
		
		JButton btn8 = new JButton("8");
		btn8.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textField.getText() + btn8.getText();
				textField.setText(EnterNumber);
			}
		});
		btn8.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn8.setBounds(70, 69, 50, 50);
		frmEureka.getContentPane().add(btn8);
		
		JButton btn9 = new JButton("9");
		btn9.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textField.getText() + btn9.getText();
				textField.setText(EnterNumber);
			}
		});
		btn9.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn9.setBounds(130, 69, 50, 50);
		frmEureka.getContentPane().add(btn9);
		
		JButton btnPlus = new JButton("+");
		btnPlus.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				firstnum = Double.parseDouble(textField.getText());
				textField.setText("");
				operations = "+";
			}
		});
		btnPlus.setFont(new Font("Tahoma", Font.BOLD, 18));
		btnPlus.setBounds(190, 69, 50, 50);
		frmEureka.getContentPane().add(btnPlus);
		
		
		//--------------------LINHA 2---------------------//
		
		JButton btn4 = new JButton("4");
		btn4.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textField.getText() + btn4.getText();
				textField.setText(EnterNumber);
			}
		});
		btn4.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn4.setBounds(10, 130, 50, 50);
		frmEureka.getContentPane().add(btn4);
		
		JButton btn5 = new JButton("5");
		btn5.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textField.getText() + btn5.getText();
				textField.setText(EnterNumber);
			}
		});
		btn5.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn5.setBounds(70, 130, 50, 50);
		frmEureka.getContentPane().add(btn5);
		
		JButton btn6 = new JButton("6");
		btn6.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
			
			String EnterNumber = textField.getText() + btn7.getText();
			textField.setText(EnterNumber);
			}
		});
		
		btn6.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn6.setBounds(130, 130, 50, 50);
		frmEureka.getContentPane().add(btn6);
		
		JButton btnSub = new JButton("-");
		btnSub.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				firstnum = Double.parseDouble(textField.getText());
				textField.setText("");
				operations = "-";
			}
		});
		btnSub.setFont(new Font("Tahoma", Font.BOLD, 18));
		btnSub.setBounds(190, 130, 50, 50);
		frmEureka.getContentPane().add(btnSub);
		
		//--------------------LINHA 3---------------------//
		
		JButton btn3 = new JButton("3");
		btn3.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textField.getText() + btn3.getText();
				textField.setText(EnterNumber);
			}
		});
		btn3.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn3.setBounds(10, 191, 50, 50);
		frmEureka.getContentPane().add(btn3);
		
		JButton btn2 = new JButton("2");
		btn2.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textField.getText() + btn2.getText();
				textField.setText(EnterNumber);
			}
		});
		btn2.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn2.setBounds(70, 191, 50, 50);
		frmEureka.getContentPane().add(btn2);
		
		JButton btn1 = new JButton("1");
		btn1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textField.getText() + btn1.getText();
				textField.setText(EnterNumber);
			}
		});
		btn1.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn1.setBounds(130, 191, 50, 50);
		frmEureka.getContentPane().add(btn1);
		
		JButton btnMulti = new JButton("*");
		btnMulti.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				firstnum = Double.parseDouble(textField.getText());
				textField.setText("");
				operations = "*";
			}
		});
		btnMulti.setFont(new Font("Tahoma", Font.BOLD, 18));
		btnMulti.setBounds(190, 191, 50, 50);
		frmEureka.getContentPane().add(btnMulti);
		
		//---------------------LINHA 4------------------//
		
		JButton btn0 = new JButton("0");
		btn0.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String EnterNumber = textField.getText() + btn0.getText();
				textField.setText(EnterNumber);
			}
		});
		btn0.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn0.setBounds(10, 248, 50, 50);
		frmEureka.getContentPane().add(btn0);
		
		JButton btnDut = new JButton(".");
		btnDut.setFont(new Font("Tahoma", Font.BOLD, 18));
		btnDut.setBounds(70, 248, 50, 50);
		frmEureka.getContentPane().add(btnDut);
		
		JButton btnEqual = new JButton("=");
		btnEqual.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				String answer;
				secondnum = Double.parseDouble(textField.getText());
				if(operations == "+") {
					result = firstnum + secondnum;
					answer = String.format("%.2f", result);
					textField.setText(answer);
				}
				else if (operations == "-") {
					result = firstnum - secondnum;
					answer = String.format("%.2f", result);
					textField.setText(answer);
				}
				else if (operations == "*") {
					result = firstnum * secondnum;
					answer = String.format("%.2f", result);
					textField.setText(answer);
				}
				else if (operations =="/") {
					result = firstnum / secondnum;
					answer = String.format("%.2f", result);
					textField.setText(answer);
				}
				
			}
		});
		btnEqual.setFont(new Font("Tahoma", Font.BOLD, 18));
		btnEqual.setBounds(130, 248, 50, 50);
		frmEureka.getContentPane().add(btnEqual);
		
		JButton btnDiv = new JButton("/");
		btnDiv.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				firstnum = Double.parseDouble(textField.getText());
				textField.setText("");
				operations = "/";
			}
		});
		btnDiv.setFont(new Font("Tahoma", Font.BOLD, 18));
		btnDiv.setBounds(190, 248, 50, 50);
		frmEureka.getContentPane().add(btnDiv);
		
		JButton btnBackSpace = new JButton("\uF0E7");
		btnBackSpace.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				
				String backspace=null;
				if(textField.getText().length()>0) {
					StringBuilder strB = new StringBuilder(textField.getText());
					strB.deleteCharAt(textField.getText().length()-1);
					backspace = strB.toString();
					textField.setText(backspace);
				}
			}
		});
		btnBackSpace.setBounds(10, 22, 50, 36);
		frmEureka.getContentPane().add(btnBackSpace);
	
	}
	}
	
