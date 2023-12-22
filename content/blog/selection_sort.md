---
title: "Selection Sort"
date: 2023-12-22
draft: false
description: "Selection Sort"
image: "/img/selection-sort.gif"
---
# Giới thiệu
Thuật toán selection sort sắp xếp một mảng bằng cách đi tìm phần tử có giá trị nhỏ nhất(giả sử với sắp xếp mảng tăng dần) trong đoạn đoạn chưa được sắp xếp và đổi cho phần tử nhỏ nhất đó với phần tử ở đầu đoạn chưa được sắp xếp(không phải đầu mảng). Thuật toán sẽ chia mảng làm 2 mảng con

1.Một mảng con đã được sắp xếp  
2.Một mảng con chưa được sắp xếp

Tại mỗi bước lặp của thuật toán, phần tử nhỏ nhất ở mảng con chưa được sắp xếp sẽ được di chuyển về đoạn đã sắp xếp.

![selection-sort](/img/selection-sort.gif)
# Minh họa thuật toán:
```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        # Tìm phần tử nhỏ nhất trong mảng chưa sắp xếp
        min_index = i
        for j in range(i+1, n):
            if arr[j] < arr[min_index]:
                min_index = j
        
        # Hoán đổi phần tử nhỏ nhất với phần tử đầu tiên chưa sắp xếp
        arr[i], arr[min_index] = arr[min_index], arr[i]

# Sử dụng:
arr = [64, 25, 12, 22, 11]
selection_sort(arr)
```
# Đánh giá thuật toán selection sort

## Phân loại:

Selection Sort thuộc loại thuật toán sắp xếp so sánh (comparison-based sorting algorithm). Nó so sánh các phần tử của mảng để xác định thứ tự sắp xếp.

## Phức tạp thời gian:

Trong trường hợp xấu nhất, trung bình và tốt nhất, độ phức tạp thời gian của Selection Sort đều là O(n^2), nơi n là số lượng phần tử của mảng.

## Trường hợp xấu nhất:

Trong trường hợp xấu nhất, Selection Sort phải thực hiện nhiều phép so sánh và trao đổi, khiến cho độ phức tạp thời gian là O(n^2). Nguy cơ xấu nhất xảy ra khi mảng đã được sắp xếp ngược, nghĩa là phần tử nhỏ nhất cần phải được đặt ở vị trí cuối cùng.

## Phức tạp dữ liệu:

Selection Sort không quan tâm đến cấu trúc của dữ liệu, vì nó chỉ làm việc với các phần tử của mảng và thực hiện các phép so sánh và trao đổi dựa trên giá trị của chúng. Vì vậy, phức tạp dữ liệu không phụ thuộc vào cấu trúc cụ thể của dữ liệu.

## Tối ưu:

Trong nhiều trường hợp, Selection Sort không được coi là tối ưu về mặt hiệu suất so với một số thuật toán sắp xếp khác như Quick Sort hay Merge Sort. Đối với các tập dữ liệu lớn, Selection Sort có thể trở nên không hiệu quả vì độ phức tạp thời gian của nó là O(n^2). Tuy nhiên, nếu dữ liệu đã gần như sắp xếp, Selection Sort có thể thực hiện tốt hơn so với một số thuật toán khác.