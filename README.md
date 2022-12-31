# gfg-Square-root-of-a-number
problem solving

Example 1:

Input:
x = 5
Output: 2
Explanation: Since, 5 is not a perfect 
square, floor of square_root of 5 is 2.


class Solution{
  public:
    long long int floorSqrt(long long int x) 
    {
        // Your code goes here
      //  int i = 1;
    //    while(i*i <= x){
      //      i++;
            
        //}
        //return i-1;
        
        int low = 0;
        int high = x;
        while(low <= high){
            long long int mid = low + (high - low)/2;
            if(mid*mid <= x && (mid+1)*(mid+1) > x){
                return mid;
            }
            else if(mid*mid < x)
            low = mid + 1;
            else
            high = mid -1;
        }
    }
};
