Array ���� C# ����������Ļ��࣬�����ṩ��һϵ��������������Ĳ��������������Ԫ�ؽ�����������������ָ����Ԫ�صȡ�

Array ���ǩ��������ʾ��

	[SerializableAttribute] 
	[ComVisibleAttribute(true)] 
	public abstract class Array : ICloneable, IList, ICollection,  
	IEnumerable, IStructuralComparable, IStructuralEquatable 

## Array ���е�����
	Array �����ṩ��һϵ�����ԣ�ͨ����Щ���Կ��Ի�ȡ����ĸ�����Ϣ��
	Array ���еĳ����������±���ʾ��

<table>
<tbody>
<tr>
<th>
����</th>
<th>
����</th>
</tr>
<tr>
<td>
IsFixedSize</td>
<td>
��������Ƿ���й̶���С</td>
</tr>
<tr>
<td>
IsReadOnly</td>
<td>
��������Ƿ�Ϊֻ��</td>
</tr>
<tr>
<td>
IsSynchronized&nbsp;</td>
<td>
����Ƿ�ͬ��������ķ��ʣ��̰߳�ȫ��</td>
</tr>
<tr>
<td>
Length</td>
<td>
��ȡ����������ά����Ԫ�ص�����</td>
</tr>
<tr>
<td>
LongLength</td>
<td>
��ȡ����������ά����Ԫ�ص�������������һ�� 64 λ����</td>
</tr>
<tr>
<td>
Rank</td>
<td>
��ȡ������ȣ�ά����������һά���鷵�� 1����ά���鷵�� 2����������</td>
</tr>
<tr>
<td>
SyncRoot</td>
<td>
������ȡһ�����󣬸ö����������ͬ��������ķ���</td>
</tr>
</tbody>
</table>

***
## Array ���еķ���

<table>
<tbody>
<tr>
<th>
����</th>
<th>
����</th>
</tr>
<tr>
<td>
Clear(Array, Int32, Int32)</td>
<td>
��������ָ����Χ�ڵ�Ԫ������Ϊ��Ԫ���������͵�Ĭ��ֵ</td>
</tr>
<tr>
<td>
Copy(Array, Array, Int32)</td>
<td>
�ӵ�һ��Ԫ�ؿ�ʼ����������ָ�����ȵ�Ԫ�أ�������ճ������һ�������У��ӵ�һ��Ԫ�ؿ�ʼճ������ʹ��&nbsp;32 λ������ָ��Ҫ�����ĳ���</td>
</tr>
<tr>
<td>
CopyTo(Array, Int32)</td>
<td>
��ָ����Ŀ��������������ʼ������ǰһά���������Ԫ�ظ��Ƶ�ָ����һά�����У�����ʹ��&nbsp;32 λ����ָ��</td>
</tr>
<tr>
<td>
GetLength</td>
<td>
��ȡ����ָ��ά���е�Ԫ������������һ�� 32 λ����</td>
</tr>
<tr>
<td>
GetLongLength</td>
<td>
��ȡ����ָ��ά���е�Ԫ������������һ�� 64 λ����&nbsp;</td>
</tr>
<tr>
<td>
GetLowerBound</td>
<td>
��ȡ������ָ��ά�ȵ�һ��Ԫ�ص�����</td>
</tr>
<tr>
<td>
GetType</td>
<td>
��ȡ��ǰʵ�������ͣ��̳��� Object ��</td>
</tr>
<tr>
<td>
GetUpperBound</td>
<td>
��ȡ������ָ��ά�����һ��Ԫ�ص�����</td>
</tr>
<tr>
<td>
GetValue(Int32)</td>
<td>
��ȡһά������ָ��λ�õ�ֵ</td>
</tr>
<tr>
<td>
IndexOf(Array, Object)</td>
<td>
��һ��һά����������ָ�����󣬲��������׸�ƥ���������</td>
</tr>
<tr>
<td>
Reverse(Array)</td>
<td>
��ת����һά������Ԫ�ص�˳��</td>
</tr>
<tr>
<td>
SetValue(Object, Int32)</td>
<td>
����һά������ָ��Ԫ�ص�ֵ</td>
</tr>
<tr>
<td>
Sort(Array)</td>
<td>
��һά�����е�Ԫ������</td>
</tr>
<tr>
<td>
ToString()</td>
<td>
����һ����ʾ��ǰ������ַ������̳��� Object��</td>
</tr>
</tbody>
</table>

```c#
using System;

namespace Array��
{
    class Demo
    {
        static void Main(string[] args) 
        { 
            // ����һ�����鲢��ֵ 
            int[] arr = new int[6] {15, 33, 29, 55, 10, 11 }; 
            // ����һ��������
            int[] arr2 = new int[6]; 
            // ��ȡ����ĳ���
            Console.WriteLine("���� arr �ĳ���Ϊ��"+arr.Length); 
            // Ϊ��������
            Array.Sort(arr); 
            Console.Write("���������� arr Ϊ��"); 
            // ��ӡ������ arr
            PrintArray(arr); 
            // ��������Ԫ�ص�����
            Console.WriteLine("\n���� arr ��ֵΪ 29 ��Ԫ�ص�����Ϊ��"+Array.IndexOf(arr,29)); 
            // ���� arr �� arr2 
            Array.Copy(arr, arr2, arr.Length); 
            Console.Write("��ӡ���� arr2��"); 
            // ��ӡ���� arr2 
            PrintArray(arr2); 
            Array.Reverse(arr); 
            Console.Write("\n������������ arr�� "); 
            PrintArray(arr); 
        } 
        // ��������Ԫ��
        static void PrintArray(int[] arr) 
        { 
            foreach (Object elem in arr) 
            { 
                Console.Write(elem+" "); 
            } 
        } 
    }
}
```
    ���н�����£�
    ���� arr �ĳ���Ϊ��6
    ���������� arr Ϊ��10 11 15 29 33 55
    ���� arr ��ֵΪ 29 ��Ԫ�ص�����Ϊ��3
    ��ӡ���� arr2��10 11 15 29 33 55
    ������������ arr�� 55 33 29 15 11 10