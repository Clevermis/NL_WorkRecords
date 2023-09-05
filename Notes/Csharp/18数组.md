```c#

C#声明数组并初始化，有三种方式。

对于一维数组：

using System;
using System.Data;
using System.Configuration;
using System.Web;
using System.Web.Security;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Web.UI.WebControls.WebParts;
using System.Web.UI.HtmlControls;

public partial class _Default : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {
        string[] arrayA = { "Shirdrn", "Hamtty", "Saxery" };
        Response.Write("<b>第一种声明数组并初始化的方法：</b><br>");
        for (int i = 0; i < arrayA.Length;i++ )
        {
            string arr = arrayA[i];
            Response.Write("arrayA[" + i + "] = " + arr + "<br>");
        }

        string[] arrayB ;
        arrayB = new string[3]{ "shirdrn", "Hamtty", "Saxery" };
        Response.Write("<b>第二种声明数组并初始化的方法：</b><br>");
        for (int i = 0; i < arrayB.Length; i++)
        {
            string arr = arrayB[i];
            Response.Write("arrayB[" + i + "] = " + arr + "<br>");
        }

        string[] arrayC = new string[3];
        arrayC[0] = "Shirdrn";
        arrayC[1] = "Hamtty";
        arrayC[2] = "Saxery";
        Response.Write("<b>第三种声明数组并初始化的方法：</b><br>");
        for (int i = 0; i < arrayC.Length; i++)
        {
            string arr = arrayC[i];
            Response.Write("arrayC["+i+"] = "+arr + "<br>");
        }    
    }
}

对于多维数组(以二维数组为例)：

using System;
using System.Data;
using System.Configuration;
using System.Web;
using System.Web.Security;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Web.UI.WebControls.WebParts;
using System.Web.UI.HtmlControls;

public partial class _Default : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {
        string[,] multiArrayA = { { "Shirdrn", "Hamtty", "Tuuty" }, { "New York", "Beijing", "Shanghai" } };
        Response.Write("<b>第一种声明数组并初始化的方法：</b><br>");
        for (int i = 0; i < multiArrayA.Rank; i++)
        {
            for (int j = 0; j <= multiArrayA.GetUpperBound(multiArrayA.Rank-1);j++ )
            {
                string arr = multiArrayA[i,j];
                Response.Write("multiArrayA[" + i + "]["+j+"] = " + arr + "<br>");
            }
        }

        string[,] multiArrayB = new string[2,3]{ { "Shirdrn", "Hamtty", "Tuuty" }, { "New York", "Beijing", "Shanghai" } };
        Response.Write("<b>第二种声明数组并初始化的方法：</b><br>");
        for (int i = 0; i < multiArrayB.Rank; i++)
        {
            for (int j = 0; j <= multiArrayB.GetUpperBound(multiArrayB.Rank - 1); j++)
            {
                string arr = multiArrayA[i, j];
                Response.Write("multiArrayB[" + i + "][" + j + "] = " + arr + "<br>");
            }
        }

        string[,] multiArrayC = new string[2, 3];
        multiArrayC[0,0] = "Shirdrn";
        multiArrayC[0,1] = "Hamtty";
        multiArrayC[0,2] = "Tuuty";
        multiArrayC[1,0] = "New York";
        multiArrayC[1,1] = "Beijing";
        multiArrayC[1,2] = "Shanghai";
        Response.Write("<b>第二种声明数组并初始化的方法：</b><br>");
        for (int i = 0; i < multiArrayC.Rank; i++)
        {
            for (int j = 0; j <= multiArrayC.GetUpperBound(multiArrayC.Rank - 1); j++)
            {
                string arr = multiArrayA[i, j];
                Response.Write("multiArrayC[" + i + "][" + j + "] = " + arr + "<br>");
            }
        }

   
    }
}
```