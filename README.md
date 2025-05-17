# Sort-Color-
Dutch National Flag Algorithm
This uses 3 pointers: low, mid, and high.

public class SortColors {
    public void sortColors(int[] nums) {
        int low = 0, mid = 0, high = nums.length - 1;

        while (mid <= high) {
            switch (nums[mid]) {
                case 0:
                    // Swap nums[low] and nums[mid], increment both
                    int temp0 = nums[low];
                    nums[low] = nums[mid];
                    nums[mid] = temp0;
                    low++;
                    mid++;
                    break;
                case 1:
                    mid++;
                    break;
                case 2:
                    // Swap nums[mid] and nums[high], decrement high only
                    int temp2 = nums[mid];
                    nums[mid] = nums[high];
                    nums[high] = temp2;
                    high--;
                    break;
            }
        }
    }
}
💡 Explanation:
0s go to the left (low side).

2s go to the right (high side).

1s stay in the middle.
And sort cut method of direct sorting of Integer Arrays.sort(nums)
;
