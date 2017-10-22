using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace WpfApplication8
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }

        private void button_Click(object sender, RoutedEventArgs e)
        {
            int num1;
            int num2;
            int answer;
            int a = 10;
            int output = 0;
            bool isnumber = false;
            isnumber = int.TryParse(textBox.Text, out output);

            if (isnumber == false)
            {
                MessageBox.Show("please enter the  nmber ");
            }
            else
            {
                num1 = int.Parse(textBox.Text);
                num2 = int.Parse(textBox1.Text);
                for (int i = num1; i < num2; i++)
                {
                    answer = a * i;
                    MessageBox.Show(answer.ToString());
                    listBox.Items.Add(i + "times" + a + "=" + answer.ToString());

                }
            }

        }
    }
}
