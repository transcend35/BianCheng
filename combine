/*  
  归并算法：把两个或两个以上的线性表合并在一起，形成一个新的线性表
  函数模版的基本使用
  程序意图：将两个相同类型的线性表元素排好序，然后将他们组合成一个排好的线性表 
*/
#include <iostream>
using namespace std;
const int n = 5;    //5个元素 

//输出数据元素
template <class T1>
void OutPut(T1 out[(2*n)])
{ 
     for (int i=0; i<(2*n); i++)
     { 
        cout<<out[i]<<" ";
     }
     cout<<endl;
} 
//输入数据元素 
template <class T2>
void InPut(T2 in[n])
{
     cout<<"请输入5个数据元素：";
     for (int i=0; i<n; i++)
     { 
        cin>>in[i];
        cout<<" "; 
     }
     cout<<endl;
}
//模版函数 输入线性表元素并将其排序
template <class T3> 
void MySort(T3 a[2*n])
{
     int temp;   //交换数据临时变量 
     //冒泡锚序 
     for (int i=0; i<2*n-1; i++)
     {
         for (int j=0; j<2*n-1-i; j++)
         {
             if (a[j]>a[j+1])  
             {
                temp   = a[j];
                a[j]   = a[j+1];
                a[j+1] = temp; 
             }
         }
     }
}

//模版函数 归并 
template  <class T> 
void  MergeList(T La[n], T Lb[n], T Lc[(2*n)]) 
{
      int i = 0;  //作为La的下标 
      int j = 0;  //Lb下标
      int k = 0;  //Lc下标 
      
      //将La Lb组合成在一起 
      while (i<n && j<n)
      {
          if (La[i] < Lb[j])
          {
             Lc[k] = La[i];
             k++;
             Lc[k] = Lb[j];
          }
          else
          {
              if (La[i] == Lb[j])
              {
                 Lc[k] = La[i];
                 k++;
                 Lc[k] = Lb[j];
              }
              else
              {
                 Lc[k] = Lb[j];
                 k++;
                 Lc[k] = La[i];
              }
          }
          //各下标往下移动 
          i++;
          j++;
          k++;
      } 
      
      //如果La中的数据没有取完，及La比Lb长，则将La剩下的元素插入Lc中 这里是进行扩展 
      while (i<=n)
      {
            Lc[k++] = La[i++];
      } 
      //如果Lb中的数据没有取完，及Lb比La长，则将Lb剩下的元素插入Lc中
       while (j<=n)
      {
             Lc[k++] = Lb[j++];
      } 
      
      //对组合好的元素进行排序 
      MySort(Lc);   
}

int main()
{
    int a1[n],a2[n], a[(2*n)];
    double b1[n], b2[n],b[(2*n)];
    char  m1[n], m2[n], m[(2*n)];
    
    //输入数据 归并输出 
   /*InPut(a1);
    InPut(a2); 
    MergeList(a1,a2,a);
    OutPut(a);  */ 
     
    InPut(m1);
    InPut(m2); 
    MergeList(m1,m2,m);
    OutPut(m);  
    
    system("pause");
    return 0;
} 
