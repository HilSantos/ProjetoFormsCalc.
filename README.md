# ProjetoFormsCalc.
Preencha os valores e pressione o botão da operação.

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace ProjetoFormsCalc
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        //declarar as var´s globais
        int val1, val2,total;

  private void btnMulti_Click(object sender, EventArgs e)
        {
            //validar se os campos foram preenchidos
            if (txtVal1.Text == "" || txtVal2.Text == "")
            {
                lblStatus.Text = "Preencha os campos!";
            }
            else
            {
                lblStatus.Text = "";
                //capturar os valores dos textbox´s nas var´s
                val1 = Convert.ToInt32(txtVal1.Text);
                val2 = Convert.ToInt32(txtVal2.Text);
                total = val1 * val2;
                lblTotal.Text = total.ToString();
            }
        }

  private void btnDivisao_Click(object sender, EventArgs e)
        {
            //validar se os campos foram preenchidos
            if (txtVal1.Text == "" || txtVal2.Text == "")
            {
                lblStatus.Text = "Preencha os campos!";
            }
            else
            {
                lblStatus.Text = "";
                
  //capturar os valores dos textbox´s nas var´s
                val1 = Convert.ToInt32(txtVal1.Text);
                val2 = Convert.ToInt32(txtVal2.Text);
                if (val2 == 0)
                {
                    lblStatus.Text = "Valor 2 não pode ser 0.\n" +
                        "Altere o valor!";
                    txtVal2.Focus();
                }
                else
                {
                    val2 = Convert.ToInt32(txtVal2.Text);
                    total = val1 / val2;
                    lblTotal.Text = total.ToString();
                }
                
         }
  }

  private void btnLimpar_Click(object sender, EventArgs e)
        {
            txtVal2.Clear();
            txtVal1.Clear();
            lblStatus.Text = "";
            lblTotal.Text = "";
            txtVal1.Focus();
        }

  private void txtVal1_TextChanged(object sender, EventArgs e)
        {

  }

  private void label1_Click(object sender, EventArgs e)
        {

  }

  private void txtVal2_TextChanged(object sender, EventArgs e)
        {

  }

  private void label2_Click(object sender, EventArgs e)
        {

  }

  private void btnSoma_Click(object sender, EventArgs e)
        {
            //validar se os campos foram preenchidos
            if (txtVal1.Text=="" || txtVal2.Text=="")
            {
                lblStatus.Text = "Preencha os campos!";
            }
            else
            {
                lblStatus.Text = "";
                //capturar os valores dos textbox´s nas var´s
                val1 = Convert.ToInt32(txtVal1.Text);
                val2 = Convert.ToInt32(txtVal2.Text);
                total=val1 + val2;
                lblTotal.Text = total.ToString();
            }
           

  }

  private void btnSubtracao_Click(object sender, EventArgs e)
        {
            //validar se os campos foram preenchidos
            if (txtVal1.Text == "" || txtVal2.Text == "")
            {
                lblStatus.Text = "Preencha os campos!";
            }
            else
            {
                lblStatus.Text = "";
                //capturar os valores dos textbox´s nas var´s
                val1 = Convert.ToInt32(txtVal1.Text);
                val2 = Convert.ToInt32(txtVal2.Text);
                total = val1 - val2;
                lblTotal.Text = total.ToString();
            }
        }
    }
}
