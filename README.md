# CTDL-GT_Nested_Recursion_2.cpp
Nested Recursion
Nguồn tham khảo : 
Ví Dụ : 

+ lấy một biểu thức truy hồi để làm ví dụ :

  ![bai21-01](https://user-images.githubusercontent.com/129465517/230538989-2f01c52a-d564-4be6-a0c1-18435ac2ebd5.png)
  
- Trong phương trình trên có phần đó là kết quả trả về của phương trình và điểm dừng. 
- Trong trường họp m > 0 và n > 0 thì tham số truyền vào là đệ quy chính nó

// Mình sẽ dùng hàm ackerman() ở phần cài đặt để giải phương trình trên. Vì để cho ngắn gọn, sẽ gọi hàm ackerman() là hàm A() . 

int A(int m, int n){
  if(m == 0)
    return n + 1;
  else if(n == 0)
    return A(m - 1, 1);
  else
    return A(m-1, A(m, n-1));
}
Với hàm A() mình sẽ truyền vào hai tham số m = 2 và n = 1 : 

![bai21-02](https://user-images.githubusercontent.com/129465517/230539255-cff9bc7f-178c-4a58-a4a1-2ba563175f10.png)

+ sau đó chạy với code : 

int A(int m, int n){
  if(m == 0) // nếu m == 0 thì return n + 1
    return n + 1;
  else if(n == 0) // nếu n == 0 thì return đệ quy A(m - 1, 1)
    return A(m - 1, 1);
  else // nếu m > 0 và n > 0 thì return đệ quy lồng A(m-1, A(m, n-1))
    return A(m-1, A(m, n-1));
}
