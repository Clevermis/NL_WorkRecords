    ʹ�� switch ���ʱ�����������¹���
    switch ����б��ʽ��ֵ������һ�����ͻ���ö�����ͣ�
    ��һ�� switch ����п��������������� case ��䣬ÿ�� case �ؼ��ֺ���Ҫ��һ������ʽ�Ƚϵ�ֵ��һ��ð�ţ�
    case �ؼ��ֺ����ֵ������ switch �б��ʽ��ֵ������ͬ���������ͣ����ұ�����һ��������Ҳ�������Ϊ��һ���̶���ֵ���������������з����ı䣩��
    �����ʽ��ֵ���� case �е�ֵʱ���ͻ�ִ�� case �������䣬������ break �ؼ���ʱֹͣ��
    ������ break �ؼ���ʱ��switch ����ֹͣ���У�����ת�� switch ����������һ�д���������У�
    ������ÿһ�� case �����涼��Ҫ���� break �ؼ��֣���� case ���Ϊ�գ�case ������û��Ҫִ�еĴ��룩������Բ����� break �ؼ��֣���ʱ��������ִ�к����� case ��䣬ֱ������ break �ؼ���Ϊֹ��
    C# �������һ�� case �������ִ�е���һ�� case ��䣬������ case ����а���Ҫִ�е���䣬�ͱ������ break �ؼ��ֻ�������ת��䣻
    һ�� switch ����ĩβ������һ����ѡ�� default��Ĭ��ѡ��������� case ��䶼��������ʽ��ƥ��ʱ���ִ�� default �����еĴ��룬���� default �е� break ������ʡ�ԣ�
    C# ��֧�ִ�һ�� case �����ת����һ�� case ��䣬���Ҫ��һ�� case �����ת����һ�� case ���Ļ�������ʹ�� goto ��䣬����goto default��

```C#
using System;

namespace switch���
{
    class Demo
    {
        static void Main(string[] args){
            Console.WriteLine("������ѧ�����Եĳɼ���0~100��������");
            int points = Convert.ToInt32(Console.ReadLine());
            switch (points / 10)
            {
                case 10:
                    Console.WriteLine("����");
                    break;
                case 9:
                    Console.WriteLine("����");
                    break;
                case 8:
                    Console.WriteLine("����");
                    break;
                case 7:
                    Console.WriteLine("����");
                    break;
                case 6:
                    Console.WriteLine("����");
                    break;
                default:
                    Console.WriteLine("������");
                    break;
            }
        }
    }
}


```