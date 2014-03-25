       private void Form1_Load(object sender, EventArgs e)
        {
            byte[] _file = File.ReadAllBytes(@"C:\Mac.pdf");
            
            string hex = BitConverter.ToString(_file);
            hex = hex.Replace("-", "");

            StreamWriter sw = new StreamWriter(@"c:\123.txt",true);
            sw.Write(hex);
            sw.Close();

   

        }
