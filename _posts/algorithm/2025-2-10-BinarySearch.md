---
title: "二分查找通用规律(固定模板解决寻找>=, >, <, <=)"
date:   2025-2-10 9:37:00 +0800
categories: [algorithm]
tags: [binarysearch]
toc: true
comments: true
permalink: /algorithm/:title/
---

    
* 范围查询规律
* 初始化:
*   int left = 0;
*   int right = nums.length - 1;
* 循环条件
*   left <= right
* 右边取值
*   right = mid - 1
* 左边取值
*   left = mid + 1
* 查询条件
  *   \>= target值, 则 nums[mid] >= target时, 都减right = mid - 1
  *   \>target值, 则 nums[mid] >  target时, 都减right = mid - 1
  *   <= target值, 则 nums[mid] <= target时, 都加left = mid + 1
  *   <  target值, 则 nums[mid] <  target时, 都加left = mid + 1
* 结果
  *   求大于(含等于), 返回left
  *   求小于(含等于), 返回right

     

* 作者：chendragon
* 链接：https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/solution/er-fen-cha-zhao-tong-yong-gui-lu-gu-ding-g93u/
* 来源：力扣（LeetCode）
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。