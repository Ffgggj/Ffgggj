using System;
using System.Drawing;
using System.Windows.Forms;

public class PracticalTask : Form
{
    public PracticalTask()
    {
        // Властивості вікна
        this.Text = "Практична робота";
        this.BackColor = Color.Gray;
        this.Size = new Size(200, 100);
        this.StartPosition = FormStartPosition.Manual;
        this.Location = new Point(150, 100);

        // Обробник події Click
        this.Click += (sender, e) =>
        {
            this.Size = new Size(300, 300);
            MessageBox.Show("Ми вивчаємо програмування!");
        };

        // Обробник події KeyPress
        this.KeyPress += (sender, e) =>
        {
            this.Location = new Point(300, 200);
        };
    }

    [STAThread]
    public static void Main()
    {
        Application.EnableVisualStyles();
        Application.Run(new PracticalTask());
    }
}
