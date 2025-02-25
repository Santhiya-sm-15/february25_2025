# february25_2025
The problem that i solved today in leetcode

1.Given an array of integers arr, return the number of subarrays with an odd sum. Since the answer can be very large, return it modulo 109 + 7.

Code:
class Solution {
    public int numOfSubarrays(int[] arr) {
        int cnt=0,sum=0;
        int odd=0,even=1;
        for(int x:arr)
        {
            sum+=x;
            if(sum%2==0)
            {
                cnt+=odd;
                even++;
            }
            else
            {
                cnt+=even;
                odd++;
            }
            cnt%=1000000007;
        }
        return cnt;
    }
}
