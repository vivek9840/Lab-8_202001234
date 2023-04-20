# Lab-8_202001234

# Name : harsora vivek

# STd-ID : 202001234

## Create a new Eclipse project, and within the project create a package and Create a class for a Boa.

![image1](https://user-images.githubusercontent.com/75905959/233331835-2af6a50b-2eea-4bf8-b8b5-d35c42d357dd.png)

## creating a test case for the class Boa.

```
package code;


import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.jupiter.api.Test;

public class Boa_test {
    private Boa jen = new Boa("Jennifer", 2, "grapes");
    private Boa ken = new Boa("Kenneth", 3, "granola bars");
    
    @Before
    public void setUp() throws Exception {
        jen = new Boa("Jennifer", 2, "grapes");
        ken = new Boa("Kenneth", 3, "granola bars");
    }
    @Test
    public void testIsHealthy() {
        // check that jen is not healthy
        assertFalse(jen.isHealthy());
        
        // check that ken is healthy
        assertTrue(ken.isHealthy());
    }
    @Test
    public void testFitsInCage() {
        // Test for jen
        assertFalse(jen.fitsInCage(1)); // cage length is less than length of boa
        assertFalse(jen.fitsInCage(2)); // cage length is equal to length of boa
        assertTrue(jen.fitsInCage(3)); // cage length is greater than length of boa

        // Test for ken
        assertFalse(ken.fitsInCage(2)); // cage length is less than length of boa
        assertFalse(ken.fitsInCage(3)); // cage length is equal to length of boa
        assertTrue(ken.fitsInCage(4)); // cage length is greater than length of boa
    }
}
```
![image2](https://user-images.githubusercontent.com/75905959/233333163-c28c72b8-d239-4d6b-822a-f501410f6486.png)

## Writing SetUp() method:
```
    @Before
    public void setUp() throws Exception {
        jen = new Boa("Jennifer", 2, "grapes");
        ken = new Boa("Kenneth", 3, "granola bars");
    }
```


## ADDED method lengthInInches() :

```
public int lengthInInches() {
    return this.length * 12;
}
```

## Run TEsts for all the TEST methods

![image](https://user-images.githubusercontent.com/75905959/233335138-f33e8177-ca84-4d4e-a0fb-9cca1b8a806a.png)

```
package code;


import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.jupiter.api.Test;

public class Boa_test {
    private Boa jen = new Boa("Jennifer", 2, "grapes");
    private Boa ken = new Boa("Kenneth", 3, "granola bars");
    
    @Before
    public void setUp() throws Exception {
        jen = new Boa("Jennifer", 2, "grapes");
        ken = new Boa("Kenneth", 3, "granola bars");
    }
    @Test
    public void testIsHealthy() {
        // check that jen is not healthy
        assertFalse(jen.isHealthy());
        
        // check that ken is healthy
        assertTrue(ken.isHealthy());
    }
    @Test
    public void testFitsInCage() {
        // Test for jen
        assertFalse(jen.fitsInCage(1)); // cage length is less than length of boa
        assertFalse(jen.fitsInCage(2)); // cage length is equal to length of boa
        assertTrue(jen.fitsInCage(3)); // cage length is greater than length of boa

        // Test for ken
        assertFalse(ken.fitsInCage(2)); // cage length is less than length of boa
        assertFalse(ken.fitsInCage(3)); // cage length is equal to length of boa
        assertTrue(ken.fitsInCage(4)); // cage length is greater than length of boa
    }
    @Test
    public void testLengthInInches() {
        assertEquals(24, jen.lengthInInches());
        assertEquals(36, ken.lengthInInches());
    }
}

```
