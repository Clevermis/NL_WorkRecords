Array 类是 C# 中所有数组的基类，其中提供了一系列用来处理数组的操作，例如对数组元素进行排序、搜索数组中指定的元素等。

Array 类的签名如下所示：

	[SerializableAttribute] 
	[ComVisibleAttribute(true)] 
	public abstract class Array : ICloneable, IList, ICollection,  
	IEnumerable, IStructuralComparable, IStructuralEquatable 

## Array 类中的属性
	Array 类中提供了一系列属性，通过这些属性可以获取数组的各种信息。
	Array 类中的常用属性如下表所示：

<table>
<tbody>
<tr>
<th>
属性</th>
<th>
描述</th>
</tr>
<tr>
<td>
IsFixedSize</td>
<td>
检查数组是否具有固定大小</td>
</tr>
<tr>
<td>
IsReadOnly</td>
<td>
检查数组是否为只读</td>
</tr>
<tr>
<td>
IsSynchronized&nbsp;</td>
<td>
检查是否同步对数组的访问（线程安全）</td>
</tr>
<tr>
<td>
Length</td>
<td>
获取数组中所有维度中元素的总数</td>
</tr>
<tr>
<td>
LongLength</td>
<td>
获取数组中所有维数中元素的总数，并返回一个 64 位整数</td>
</tr>
<tr>
<td>
Rank</td>
<td>
获取数组的秩（维数），例如一维数组返回 1，二维数组返回 2，依次类推</td>
</tr>
<tr>
<td>
SyncRoot</td>
<td>
用来获取一个对象，该对象可以用于同步对数组的访问</td>
</tr>
</tbody>
</table>

***
## Array 类中的方法

<table>
<tbody>
<tr>
<th>
方法</th>
<th>
描述</th>
</tr>
<tr>
<td>
Clear(Array, Int32, Int32)</td>
<td>
将数组中指定范围内的元素设置为该元素所属类型的默认值</td>
</tr>
<tr>
<td>
Copy(Array, Array, Int32)</td>
<td>
从第一个元素开始拷贝数组中指定长度的元素，并将其粘贴到另一个数组中（从第一个元素开始粘贴），使用&nbsp;32 位整数来指定要拷贝的长度</td>
</tr>
<tr>
<td>
CopyTo(Array, Int32)</td>
<td>
从指定的目标数组索引处开始，将当前一维数组的所有元素复制到指定的一维数组中，索引使用&nbsp;32 位整数指定</td>
</tr>
<tr>
<td>
GetLength</td>
<td>
获取数组指定维度中的元素数，并返回一个 32 位整数</td>
</tr>
<tr>
<td>
GetLongLength</td>
<td>
获取数组指定维度中的元素数，并返回一个 64 位整数&nbsp;</td>
</tr>
<tr>
<td>
GetLowerBound</td>
<td>
获取数组中指定维度第一个元素的索引</td>
</tr>
<tr>
<td>
GetType</td>
<td>
获取当前实例的类型（继承自 Object ）</td>
</tr>
<tr>
<td>
GetUpperBound</td>
<td>
获取数组中指定维度最后一个元素的索引</td>
</tr>
<tr>
<td>
GetValue(Int32)</td>
<td>
获取一维数组中指定位置的值</td>
</tr>
<tr>
<td>
IndexOf(Array, Object)</td>
<td>
在一个一维数组中搜索指定对象，并返回其首个匹配项的索引</td>
</tr>
<tr>
<td>
Reverse(Array)</td>
<td>
反转整个一维数组中元素的顺序</td>
</tr>
<tr>
<td>
SetValue(Object, Int32)</td>
<td>
设置一维数组中指定元素的值</td>
</tr>
<tr>
<td>
Sort(Array)</td>
<td>
对一维数组中的元素排序</td>
</tr>
<tr>
<td>
ToString()</td>
<td>
返回一个表示当前对象的字符串（继承自 Object）</td>
</tr>
</tbody>
</table>

```c#
using System;

namespace Array类
{
    class Demo
    {
        static void Main(string[] args) 
        { 
            // 创建一个数组并赋值 
            int[] arr = new int[6] {15, 33, 29, 55, 10, 11 }; 
            // 创建一个空数组
            int[] arr2 = new int[6]; 
            // 获取数组的长度
            Console.WriteLine("数组 arr 的长度为："+arr.Length); 
            // 为数组排序
            Array.Sort(arr); 
            Console.Write("排序后的数组 arr 为："); 
            // 打印排序后的 arr
            PrintArray(arr); 
            // 查找数组元素的索引
            Console.WriteLine("\n数组 arr 中值为 29 的元素的索引为："+Array.IndexOf(arr,29)); 
            // 拷贝 arr 到 arr2 
            Array.Copy(arr, arr2, arr.Length); 
            Console.Write("打印数组 arr2："); 
            // 打印数组 arr2 
            PrintArray(arr2); 
            Array.Reverse(arr); 
            Console.Write("\n反序排列数组 arr： "); 
            PrintArray(arr); 
        } 
        // 遍历数组元素
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
    运行结果如下：
    数组 arr 的长度为：6
    排序后的数组 arr 为：10 11 15 29 33 55
    数组 arr 中值为 29 的元素的索引为：3
    打印数组 arr2：10 11 15 29 33 55
    反序排列数组 arr： 55 33 29 15 11 10