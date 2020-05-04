# Leetcode-May
Week 1, May 1st - May 7th

public class Solution extends VersionControl {
    public int firstBadVersion(int n) {
        // binary search
        int low = 1;
        int high = n;
        while (low <= high) {
            int mid = low + (high - low) / 2; 
            if (isBadVersion(low)) {
                return low;
            }
            if (isBadVersion(mid)) {
                high = mid;
            }
            else {
                low = mid + 1;   
            }            
        }
        return n;
    }
}  
