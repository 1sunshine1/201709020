int merge_sort(int *nums, int left, int right) {
    if (left >= right) return 0;
    int mid = (left + right) >> 1;
    ans += merge_sort(nums, left, mid);
    ans += merge_sort(nums, mid + 1, right);
    int *temp = (int *)malloc(sizeof(int) * (right - left + 1));
    int ind1 = left, ind2 = mid + 1, loc = 0, k = left;
    while (ind1 <= mid || ind2 <= right) {
        while (ind2 > right || (ind1 <= mid) && (nums[ind1] < nums[ind2])) {
            temp[loc++] = nums[ind1++];
        } else {
            while (k < mid && nums[k] <= 3 * nums[ind2]) k++;
            temp[loc++] = nums[ind2++];
            ans += (mid - k + 1);
        }
    }
    return ans;
}
int reverse_pairs(int *nums, int length) {
    return merge_sort(nums, 0, length - 1);
}
