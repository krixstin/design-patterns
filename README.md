# design-patterns
singleton pattern and visitor pattern in java &amp; js implemented

## Singleton Pattern

```java
public class SingleObject {

	private static SingleObject instance = new SingleObject();
  
	// PRIVATE: can't create "new" object
	private SingleObject() {
	}

	// Get the only object available
	public static SingleObject getInstance() {
		return instance;
	}

	public void showMessage() {
		System.out.println("Hello World!");
	}
}
```

:heavy_check_mark: SingleObject object = **SingleObject.getInstance()**;

:x: SingleObject object = new SingleObject(); 

		
### Problems/Solutions
Not safe in Multi-Thread Environment: 

- loop can be excuted multiple times at the same moment (조건문이 동시에 두번 돌 수 있음)
- shared value can't be maintained well-> use ` synchronized` key word

    ``` 
    public synchronized static void print(String input) {
    		count++;
    		System.out.println(input + "count : "+ count);
    	}
    ```

Interface can't use static methods

<br>

## Visitor Pattern
Without chaing the classes of the elements on which it operates, it lets you define a new operations 

![image](https://user-images.githubusercontent.com/55266110/113383119-340f8b00-9351-11eb-9e77-371a4beced21.png)

<br>

## Source 
https://www.tutorialspoint.com/design_pattern/design_pattern_quick_guide.htm
