# DSA NOTES

### **1. What is an Array?**
An **array** is a data structure that stores a fixed-size sequential collection of elements of the same data type. It is used to store multiple values in a single variable, making it easier to work with large sets of data.

---

### **2. Key Features of Arrays**
- **Fixed Size:** The size of an array is defined at the time of declaration and cannot be changed.
- **Homogeneous Elements:** Arrays store elements of the same data type.
- **Indexing:** Array elements can be accessed using an index, starting from `0`.
- **Efficient Access:** Arrays allow random access to elements using their indices.

---

### **3. Declaration and Initialization**
#### In **Java**:
```java
// Declaration
int[] arr;  // Recommended
int arr2[]; // Also valid

// Initialization
arr = new int[5]; // Declares an array of size 5

// Declaration and Initialization together
int[] arr3 = {10, 20, 30, 40, 50};
```

---

### **4. Accessing Array Elements**
Array elements are accessed using their **index**:
```java
int[] numbers = {10, 20, 30, 40};
System.out.println(numbers[0]); // Output: 10
System.out.println(numbers[3]); // Output: 40
```

---

### **5. Types of Arrays**
1. **One-Dimensional Array**
   - A linear array with elements stored in a single row.
   - Example:
     ```java
     int[] arr = {1, 2, 3, 4, 5};
     for (int i = 0; i < arr.length; i++) {
         System.out.println(arr[i]);
     }
     ```

2. **Two-Dimensional Array (Matrix)**
   - Stores data in rows and columns.
   - Example:
     ```java
     int[][] matrix = {
         {1, 2, 3},
         {4, 5, 6},
         {7, 8, 9}
     };
     System.out.println(matrix[1][2]); // Output: 6
     ```

3. **Multidimensional Arrays**
   - Arrays with more than two dimensions.
   - Example:
     ```java
     int[][][] multiArray = new int[2][3][4];
     ```

---

### **6. Common Array Operations**
1. **Traverse an Array**
   ```java
   for (int i = 0; i < arr.length; i++) {
       System.out.println(arr[i]);
   }
   ```

2. **Find Maximum Element**
   ```java
   int max = arr[0];
   for (int i = 1; i < arr.length; i++) {
       if (arr[i] > max) {
           max = arr[i];
       }
   }
   ```

3. **Reverse an Array**
   ```java
   for (int i = arr.length - 1; i >= 0; i--) {
       System.out.print(arr[i] + " ");
   }
   ```

---

### **7. Array Methods in Java**
1. **Length Property**
   ```java
   int[] arr = {10, 20, 30};
   System.out.println(arr.length); // Output: 3
   ```

2. **Sorting an Array**
   ```java
   import java.util.Arrays;

   int[] arr = {5, 2, 8, 1};
   Arrays.sort(arr);
   System.out.println(Arrays.toString(arr)); // Output: [1, 2, 5, 8]
   ```

3. **Copying an Array**
   ```java
   int[] arr = {1, 2, 3};
   int[] newArr = Arrays.copyOf(arr, arr.length);
   ```

4. **Search in Array**
   ```java
   int[] arr = {1, 2, 3, 4};
   int index = Arrays.binarySearch(arr, 3); // Works only on sorted arrays
   ```

---

### **8. Advantages of Arrays**
- Easy to use and implement.
- Random access to elements.
- Efficient for searching and sorting when size is small.

---

### **9. Limitations of Arrays**
- Fixed size; cannot grow or shrink dynamically.
- Insertion and deletion can be costly as elements need to be shifted.
- Only stores elements of the same data type.

---

### **10. Applications of Arrays**
- Storing and manipulating datasets.
- Used in searching and sorting algorithms (e.g., Bubble Sort, Merge Sort).
- Matrices in mathematics and game development.
- Storing records like temperature, grades, etc.

---

### **11. Array vs ArrayList in Java**
| Feature       | Array                          | ArrayList                              |
|---------------|--------------------------------|----------------------------------------|
| Size          | Fixed                         | Dynamic                                |
| Data Type     | Homogeneous                   | Can store objects of any type         |
| Performance   | Faster                        | Slightly slower due to overhead       |
| Flexibility   | Less                          | More                                  |

---

### **Code Example: Array with Basic Operations**
```java
import java.util.Arrays;

public class ArrayExample {
    public static void main(String[] args) {
        // Declaration and Initialization
        int[] arr = {10, 20, 30, 40, 50};

        // Accessing Elements
        System.out.println("Element at index 2: " + arr[2]);

        // Traversing
        System.out.println("Array Elements:");
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();

        // Find Maximum
        int max = arr[0];
        for (int num : arr) {
            if (num > max) max = num;
        }
        System.out.println("Maximum Element: " + max);

        // Sorting
        Arrays.sort(arr);
        System.out.println("Sorted Array: " + Arrays.toString(arr));
    }
}
