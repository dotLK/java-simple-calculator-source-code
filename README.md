# java-simple-calculator-source-code
java simple calculator source code

🔵 Java for Beginners step by step Complete Java Full Course in 8 Hours Java සිංහලෙන් ඉගන ගනිමු :
 https://youtu.be/_7rZSojr7jk
```java

package GUI;

import java.awt.BorderLayout;
import java.awt.Button;
import java.awt.Color;
import java.awt.Font;
import java.awt.GridLayout;
import java.awt.Menu;
import java.awt.MenuBar;
import java.awt.MenuItem;
import java.awt.TextField;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.JFrame;
import javax.swing.JOptionPane;
import javax.swing.JPanel;

public class Basiccal {

    public static void main(String[] args) {

        clabody cal = new clabody();

    }

}

class clabody extends JFrame {
    
    double fn , sn , sum ;
    String what ;

    clabody() {

        setVisible(true);
        setTitle("My Cal");
        setSize(300, 400);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLocationRelativeTo(null);

        BorderLayout bd = new BorderLayout();

        JPanel p1 = new JPanel();
        //p1.setBackground(Color.red);
        JPanel p2 = new JPanel();
        p2.setBackground(Color.GREEN);

        add(p1, BorderLayout.NORTH);
        add(p2, BorderLayout.CENTER);

        TextField t1 = new TextField(15);
        t1.setFont(new Font("", 0, 30));
        p1.add(t1);

        GridLayout gl = new GridLayout(3, 3);
        p2.setLayout(gl);

        Button b1 = new Button("1");
        // b1.setBackground(Color.red);
        p2.add(b1);
        b1.setFont(new Font("", 0, 30));
        
        b1.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                
               String v = t1.getText(); //0123               
              v += "1"; // 01231 +               
              t1.setText(v);
                
            }
        });

        Button b2 = new Button("2");
        //b2.setBackground(Color.BLUE);
        p2.add(b2);
        b2.setFont(new Font("", 0, 30));
        b2.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
              
              String v = t1.getText(); //0123               
              v += "2"; // 01231 +               
              t1.setText(v);
            }
        });

        Button b3 = new Button("3");
        // b3.setBackground(Color.GRAY);
        p2.add(b3);
        b3.setFont(new Font("", 0, 30));
        b3.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
               String v = t1.getText(); //0123               
              v += "3"; // 01231 +               
              t1.setText(v);
            }
        });

        Button b4 = new Button("4");
        // b4.setBackground(Color.ORANGE);
        p2.add(b4);
        b4.setFont(new Font("", 0, 30));
        b4.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String v = t1.getText(); //0123               
              v += "4"; // 01231 +               
              t1.setText(v);
            }
        });

        Button b5 = new Button("5");
        // b5.setBackground(Color.DARK_GRAY);
        p2.add(b5);
        b5.setFont(new Font("", 0, 30));
        b5.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String v = t1.getText(); //0123               
              v += "5"; // 01231 +               
              t1.setText(v);
            }
        });

        Button b6 = new Button("6");
        // b6.setBackground(Color.PINK);
        p2.add(b6);
        b6.setFont(new Font("", 0, 30));
        b6.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String v = t1.getText(); //0123               
              v += "6"; // 01231 +               
              t1.setText(v);
            }
        });

        Button b7 = new Button("7");
        // b7.setBackground(Color.red);
        p2.add(b7);
        b7.setFont(new Font("", 0, 30));
        b7.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String v = t1.getText(); //0123               
              v += "7"; // 01231 +               
              t1.setText(v);
            }
        });

        Button b8 = new Button("8");
        // b8.setBackground(Color.darkGray);
        p2.add(b8);
        b8.setFont(new Font("", 0, 30));
        b8.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String v = t1.getText(); //0123               
              v += "8"; // 01231 +               
              t1.setText(v);
            }
        });

        Button b9 = new Button("9");
        // b9.setBackground(Color.cyan);
        p2.add(b9);
        b9.setFont(new Font("", 0, 30));
        b9.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String v = t1.getText(); //0123               
              v += "9"; // 01231 +               
              t1.setText(v);
            }
        });

        Button b0 = new Button("0");
        p2.add(b0);
        b0.setFont(new Font("", 0, 30));
        b0.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String v = t1.getText(); //0123               
              v += "0"; // 01231 +               
              t1.setText(v);
            }
        });
        Button dot = new Button(".");
        p2.add(dot);
        dot.setFont(new Font("", 0, 30));
        dot.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String v = t1.getText(); //0123               
              v += "."; // 01231 +               
              t1.setText(v);
            }
        });
        Button clr = new Button("C");
        p2.add(clr);
        clr.setFont(new Font("", 0, 30));
        clr.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                t1.setText("");
                fn = 0.0;
                sn = 0.0;
                what= "";
            }
        });
        
        Button plus = new Button("+");
        p2.add(plus);
        plus.setFont(new Font("", 0, 30));
        plus.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
               
                fn = Double.parseDouble(t1.getText()) ;
                System.out.print(fn);
                t1.setText("");
                what = "+";
                System.out.print(what);
                
            }
        });

        Button min = new Button("-");
        p2.add(min);
        min.setFont(new Font("", 0, 30));
        min.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
               
                fn = Double.parseDouble(t1.getText()) ;
                System.out.print(fn);
                t1.setText("");
                what = "-";
                System.out.print(what);
            }
        });

        Button mul = new Button("*");
        p2.add(mul);
        mul.setFont(new Font("", 0, 30));
        mul.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
               
                fn = Double.parseDouble(t1.getText()) ;
                System.out.print(fn);
                t1.setText("");
                what = "*";
                System.out.print(what);
            }
        });
        Button devi = new Button("/");
        p2.add(devi);
        devi.setFont(new Font("", 0, 30));
        devi.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
               
                fn = Double.parseDouble(t1.getText()) ;
                System.out.print(fn);
                t1.setText("");
                what = "/";
                System.out.print(what);
            }
        });
        Button sqr = new Button("√");
        p2.add(sqr);
        sqr.setFont(new Font("", 0, 30));
        sqr.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
             // math.sqtr();
             double sq = Double.valueOf(t1.getText());
            
             double ans =  Math.sqrt(sq) ;
                System.out.println(ans);
             t1.setText(String.valueOf(ans));
             
                
            }
        });
        Button qe = new Button("=");
        p2.add(qe);
        qe.setFont(new Font("", 0, 30));
        qe.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
               
                sn = Double.parseDouble(t1.getText()) ;
                System.out.print(sn);
                sum = cal(fn, sn, what);
                System.out.println(" = " +sum);
                t1.setText(String.valueOf(sum));
                
            }
        });
        
        MenuBar mb = new MenuBar();
        setMenuBar(mb);

        Menu m1 = new Menu("File");
        Menu m2 = new Menu("Edit");
        Menu m3 = new Menu("View");
        mb.add(m1);
        mb.add(m2);
        mb.add(m3);

        MenuItem m_new = new MenuItem("New File");
        MenuItem m_save = new MenuItem("Save");
        MenuItem m_Exit = new MenuItem("Exit");
        m1.add(m_new);
        m1.add(m_save);
        m1.add(m_Exit);
        m_Exit.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                JOptionPane.showMessageDialog(rootPane, "Hi iam java...!!");
            }
        });
    }
public double cal(double a , double b ,String w){
 
    double tot = 0;
 
    if (w.equals("+")) {
        tot =  a+ b;
        
    } else if(w.equals("-")) {
        tot =  a -  b;
    
    } else if(w.equals("*")) {
        tot =  a  *  b;
    
    } else if(w.equals("/")) {
        tot =  a  /  b;
    }
 
return tot ;
}
}

```
# Java-Basic-for-beginner
Java Basic for beginner sinhala
 In this video, we discuss Java Basic .

 පහළ Link click කර මෙම Code free download කරගන්න.

🎁  https://bit.ly/3oZkT0p
📝 https://github.com/dotLK/Java-Basic-for-beginner

Java සිංහලෙන් ඉගන ගනිමු – Sinhala Java Tutorials. Java tutorial for beginners Sinhala. පරිගණක මෘදුකාංග නිර්මාණය කීරීම සදහා වර්තමානයේ බහුලව භාවිතා කරන පරිගණක භාෂාවක් ලෙස Java හැදින්විය හැක. මෙම  video පාඩම් මගින් අපි ඔබට නොමිලේම  Java හදුන්වා දෙනවා. Coding ඉගෙන ගන්න දැන්ම Subscribe කරන්න.

Java Programming Sinhala Video Tutorials, Free Lessons( Java සිංහලෙන් ඉගන ගනිමු)


⭐️ Want to learn more from me? Check out these links:

►  🔵 Java for Beginners step by step in Sinhala | Java Sinhala |Complete Java Full Course in 8 Hours Java සිංහලෙන් ඉගන ගනිමු :
 https://youtu.be/_7rZSojr7jk
   
►  🔴  Java English Alphabet  Print A To Z  | Java in Sinhala ජාවා සිංහලෙන්  : 

https://youtu.be/Co1oadPaptI

►  🔵  Java calculator Sinhala 

Part 1 : https://youtu.be/SpbjLFxk42g    Part 2 : https://youtu.be/7YrRL5mQqZE

►  🔴   Java Odd And Even Numbers with Example Program :

https://youtu.be/E89Byqb9nwU
 
►  🔵  Java Sinhala For Loop Design Pattern Print 1 :

https://youtu.be/Chq5wyY4e3w

►  🔴   Java Sinhala For Loop Design Pattern Print 2 :

https://youtu.be/vBuyYkb3H1A
 

😍 Connect with us on 

   📸  Follow us on Instagram -  https://www.instagram.com/dappyoutube
   🐦  Follow us on Instagram - https://twitter.com/dappyoutube
   😊  Like us on Facebook -  https://www.facebook.com/javafreecode/
   📚   Get Insights and tips from our Blog -  http://www.ideclo.com
   

✌🏽 Also, follow me on Github for some FreeCode https://github.com/coolsasindu ✌🏽


✨🥤 CHEARS!  Thanks For Watching This Tutorial  ✨

එහෙනම් හැමෝටම ජය...සහයෝගය දුන් සැමටම ස්තූතියි...!!!!!

#javasinhala #sinhala #javaFreecode #sinhalajava #sinhalapython #python #javaSInhalen 





