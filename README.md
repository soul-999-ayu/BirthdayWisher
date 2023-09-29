# Birthday-Wisher-simple-
Modify and share this program to the BDay Boy/Girl.

Birthday Wisher:
This is a very simple program created using a bunch of JLabels.
This program can be modified easily and looks great to a non programmer. 

As soon as the BDay Boy/Girl run this program, it will play a music (Birthday instumental music) and a bunch of text will appear after some seconds like "Happy Birthday" and all. You can change the music, text, time of appearance and many more.

Modify this program, convert it to exe and send it to the BDay Boy/Girl to wish them.

Features:
* GUI looks great.
* Written in very less lines.
* You can change text, music, appearance and add more components (such as a "Thank You" button with link of your Whatsapp).
* And many more.

Check sample video to understand:
[Note: The ui will look better in windows as this program uses some cool preinstalled fonts of windows.]

https://user-images.githubusercontent.com/119154806/217190958-dbf63741-5885-4eda-9629-be46e601537b.mp4

Check the code:

	import java.awt.*;
	import java.io.IOException;
	import java.net.*;
	import javax.sound.sampled.*;
	import javax.swing.*;

	public class MyFrame extends JFrame {

	JLabel labels[] = new JLabel[17];
	URL imageURL, imageURL2, imageURL3, imageURL4, imageURL5, imageURL6, imageURL7;
	URL urlsd;
	ImageIcon imageIcon8;
	
	private static final long serialVersionUID = 1L;
	
	void anim() throws InterruptedException {
		Thread.sleep(1000);
		labels[1].setVisible(true);
		Thread.sleep(1000);
		labels[0].setVisible(true);
		Thread.sleep(2000);
		labels[2].setVisible(true);
		labels[3].setVisible(true);
		labels[4].setVisible(true);
		labels[5].setVisible(true);
		Thread.sleep(4000);
		labels[6].setVisible(true);
		labels[7].setVisible(true);
		Thread.sleep(4000);
		labels[8].setVisible(true);
		labels[9].setVisible(true);
		Thread.sleep(2000);
		labels[13].setVisible(true);
		Thread.sleep(2000);
		labels[10].setVisible(true);
		Thread.sleep(2000);
		labels[11].setVisible(true);
		labels[12].setVisible(true);
		balloon();
	}
	
	void balloon() {
		labels[14].setVisible(true);
		labels[15].setVisible(true);
		labels[16].setVisible(true);
		int i=0;
		while(i==0) {
			labels[14].setLocation(labels[14].getX(), (labels[14].getY()-1));
			labels[15].setLocation(labels[15].getX(), (labels[15].getY()-1));
			labels[16].setLocation(labels[16].getX(), (labels[16].getY()-1));
			try {
				Thread.sleep(1);
			} catch (InterruptedException e) {}
			if(labels[16].getY()==-300) {
				labels[14].setBounds(10, 820, 300, 200);
				labels[15].setBounds(260, 820, 300, 200);
				labels[16].setBounds(110, 720, 300, 200);
			}
		}
	}
	
	@SuppressWarnings("static-access")
	MyFrame() throws UnsupportedAudioFileException, IOException, LineUnavailableException, InterruptedException{
		
		String lab[] = {"", "Happy Birthday", "Happy Birthday", "to you", "Name", "", "Today is your day", "","Hope you'll get everything", "You've dreamed of.", "", "Best Wishes", "From AYUSH", "","", "", ""};
		for(int i=0; i<17; i++) {
			labels[i] = new JLabel(lab[i]);
			labels[i].setForeground(Color.RED);
			labels[i].setVisible(false);
			this.add(labels[i]);
			labels[i].setFont(new Font("Segoe Print", Font.PLAIN, 16));
		}
		
		labels[4].setFont(new Font("Segoe Print", Font.PLAIN, 18));
		labels[6].setFont(new Font("Segoe Print", Font.PLAIN, 19));
		labels[7].setFont(new Font("Segoe Print", Font.PLAIN, 19));
		
		imageURL = new URL("https://user-images.githubusercontent.com/119154806/216777668-d3819eb6-06aa-4977-a5a6-633765270eb0.png");
		Image img = java.awt.Toolkit.getDefaultToolkit().getDefaultToolkit().createImage(imageURL);
		Image dimg = img.getScaledInstance(350, 450, Image.SCALE_SMOOTH);
		ImageIcon imageIcon = new ImageIcon(dimg);
		
		imageURL2 = new URL("https://user-images.githubusercontent.com/119154806/215511510-112d477c-462b-4c08-9ee9-ea2af5e8063f.png");
		Image img2 = java.awt.Toolkit.getDefaultToolkit().getDefaultToolkit().createImage(imageURL2);
		Image dimg2 = img2.getScaledInstance(120, 90, Image.SCALE_SMOOTH);
		ImageIcon imageIcon2 = new ImageIcon(dimg2);
		
		imageURL3 = new URL("https://user-images.githubusercontent.com/119154806/216823875-7e0d465b-0112-4c2e-9860-df93d4661c3c.png");
		Image img3 = java.awt.Toolkit.getDefaultToolkit().getDefaultToolkit().createImage(imageURL3);
		Image dimg3 = img3.getScaledInstance(150, 90, Image.SCALE_SMOOTH);
		ImageIcon imageIcon3 = new ImageIcon(dimg3);
    
		imageURL4 = new URL("https://user-images.githubusercontent.com/119154806/216823065-bdd79048-675a-4ce7-b62b-15c2f5c952b6.png");
		Image img4 = java.awt.Toolkit.getDefaultToolkit().getDefaultToolkit().createImage(imageURL4);
		Image dimg4 = img4.getScaledInstance(150, 200, Image.SCALE_SMOOTH);
		ImageIcon imageIcon4 = new ImageIcon(dimg4);
		
		imageURL5 = new URL("https://user-images.githubusercontent.com/119154806/216778810-6c045fcc-99c6-4306-aef7-02a0d10210c4.png");
		Image img5 = java.awt.Toolkit.getDefaultToolkit().getDefaultToolkit().createImage(imageURL5);
		Image dimg5 = img5.getScaledInstance(100, 200, Image.SCALE_SMOOTH);
		ImageIcon imageIcon5 = new ImageIcon(dimg5);
		
		imageURL6 = new URL("https://user-images.githubusercontent.com/119154806/217014917-57faf79a-c7ac-4cbe-bf0c-fb134d84ef48.png");
		Image img6 = java.awt.Toolkit.getDefaultToolkit().getDefaultToolkit().createImage(imageURL6);
		Image dimg6 = img6.getScaledInstance(20, 23, Image.SCALE_SMOOTH);
		ImageIcon imageIcon6 = new ImageIcon(dimg6);
		
		imageURL7 = new URL("https://user-images.githubusercontent.com/119154806/217017185-6384042d-28c1-47b9-95a7-b377eab5be9b.png");
		Image img7 = java.awt.Toolkit.getDefaultToolkit().getDefaultToolkit().createImage(imageURL7);
		Image dimg7 = img7.getScaledInstance(25, 24, Image.SCALE_SMOOTH);
		ImageIcon imageIcon7 = new ImageIcon(dimg7);
		
		labels[1].setBounds(125, 0, 180, 25);
		labels[0].setIcon(imageIcon);
		labels[10].setIcon(imageIcon2);
		labels[13].setIcon(imageIcon3);
		labels[14].setIcon(imageIcon5);
		labels[15].setIcon(imageIcon5);
		labels[16].setIcon(imageIcon4);
		labels[5].setIcon(imageIcon6);
		labels[7].setIcon(imageIcon7);
		labels[0].setBounds(5, 20, 500, 450);
		labels[2].setBounds(125, 50, 250, 25);
		labels[3].setBounds(155, 80, 180, 25);
		labels[4].setBounds(130, 110, 100, 25);
		labels[5].setBounds(205, 110, 180, 25);
		labels[6].setBounds(80, 145, 200, 25);
		labels[7].setBounds(260, 145, 180, 25);
		labels[8].setBounds(70, 180, 230, 25);
		labels[9].setBounds(95, 210, 200, 25);
		labels[10].setBounds(35, 335, 135, 100);
		labels[13].setBounds(100, 230, 160, 100);
		labels[11].setBounds(165, 320, 150, 113);
		labels[12].setBounds(155, 350, 150, 113);
		labels[14].setBounds(10, 820, 300, 200);
		labels[15].setBounds(260, 820, 300, 200);
		labels[16].setBounds(110, 720, 300, 200);
		
		this.setLocationRelativeTo(null);
		this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		this.setResizable(false);
		this.setLayout(null);
		this.setSize(new Dimension(370, 520));
		this.getContentPane().setBackground(Color.WHITE);
		this.setVisible(true);
		
		Clip clip = AudioSystem.getClip();
		AudioInputStream ais = AudioSystem.getAudioInputStream(new URL("https://drive.ayubackup.workers.dev/0:/happy-birthday-music-box.wav"));
		clip.open(ais);
		clip.start();
		anim();
	}
	}

Info about code:
* Change the NAME in code and AYUSH with the name of wisher.
* Modify the code to add poppers or more balloons and it will look awesome.

Thanks for using my codes, kindly check my other repos as well.
