# count-primes


# Implementation : Sieve of Eratosthenes

```java
class Solution {
    public int countPrimes(int n) {
        if(n <= 1)
            return 0;
        boolean[] primes = new boolean[n];
        Arrays.fill(primes, true);
        primes[0] = primes[1] = false;
        int primeCount = 0;
    
        for(int i = 2; i < n; i++){
            if(primes[i]){
                primeCount++;
                for(int j = 2; j*i < n; j++){
                    primes[i*j] = false;
                }
            }
        }
        
        return primeCount;
    }
}
```

# References :
1. https://www.youtube.com/watch?v=eKp56OLhoQs
2. https://www.youtube.com/watch?v=UMVa5fRKC8I
