---
title: "Quick Sort"
date: 2023-12-22
draft: false
description: "Quick sort"
image: "/img/quicksort.gif"
---
![quicksort](/img/qicksort.gif)

Thuật toán **Quick Sort** là một thuật toán sắp xếp, còn được gọi là sắp xếp kiểu phân chia (Part Sort). Là một thuật toán hiệu quả dựa trên việc phân chia mảng dữ liệu thành các nhóm phần tử nhỏ hơn.

**Phân loại: Giải thuật sắp xếp**
**Phức tạp thời gian:** Trung bình O(n log n)
**Xấu nhất:** O(n2)
**Phức tạp dữ liệu:** Khác nhau tùy vào cách hiện thực
**Tối ưu:** Thỉnh thoảng

Giải thuật sắp xếp nhanh chia mảng thành hai phần bằng cách so sánh từng phần tử của mảng với một phần tử được gọi là phần tử chốt. Một mảng bao gồm các phần tử nhỏ hơn hoặc bằng phần tử chốt và một mảng gồm các phần tử lớn hơn phần tử chốt.

Quá trình phân chia này diễn ra cho đến khi độ dài của các mảng con đều bằng 1. Với phương pháp đệ quy ta có thể sắp xếp nhanh các mảng con sau khi kết thúc chương trình ta được một mảng đã sắp xếp hoàn chỉnh.