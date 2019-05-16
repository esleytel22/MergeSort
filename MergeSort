import java.util.Arrays;

public class MergeSort<AnyType extends Comparable<? super AnyType>>
{
  private int n;
  private AnyType[] values;

  public MergeSort()
  {
    n = 0;
    values = null;
  }

  public void setValues(AnyType[] items)
  {
    n = items.length;
    values = Arrays.copyOfRange(items, 0, n);
  }

  public void getSortedValues(AnyType[] items)
  {
    int i;

    for (i = 0; i < n; i++) items[i] = values[i];
  }

  public void performMergeSort()
  {
    mergeSortRecursion(values);
  }

  private void mergeSortRecursion(AnyType[] v)
  {
    int n, mid;
    AnyType[] v1, v2;

    n = v.length;
    if (n < 2) return;

    mid = n / 2;
    v1 = Arrays.copyOfRange(v, 0, mid);
    v2 = Arrays.copyOfRange(v, mid, n);

    mergeSortRecursion(v1);
    mergeSortRecursion(v2);

    for (int i = 0; i < v1.length; i++) {
    	System.out.println("v1= " + v1[i] + " v2= " + v2[i]);
    }
    merge(v1, v2, v);
  }

  private void merge(AnyType[] v1, AnyType[] v2, AnyType[] v)
  {
    int i, j, n, n1, n2;

    i = 0;               //keeps track of the index position in v1
    j = 0;				 //keeps track of the index position in v2
    n = v.length;
    n1 = v1.length;		
    n2 = v2.length;
    while ((i + j) < n)	 //(i+j) should be equal to n, which means that it is full.
    {
      if ((j == n2) || ((i < n1) && (v1[i].compareTo(v2[j]) < 0)))
        v[i+j] = v1[i++];
      else
        v[i+j] = v2[j++];
    }
  }
}
