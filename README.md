# giai bai toan n-puzzle bang a* va greedy best-first search

## gioi thieu

repository nay trinh bay viec giai bai toan n-puzzle (vi du 8-puzzle, 15-puzzle) bang hai thuat toan tim kiem thong dung trong tri tue nhan tao:

* greedy best-first search (akt)
* a* search

chuong trinh duoc viet bang python, chay tren console, co the nhap du lieu tu ban phim va in ra cac buoc giai chi tiet.

---

## mo ta bai toan n-puzzle

ap dung trong bai toan giai o chu co ma tran 2 chieu kich thuoc nxn, trong do co mot o trong con lai duong danh so khong theo thu tu, nhiem vu la can phai sap xep lai cac o theo thu tu. 
bat dau tu mo dinh dau tien den dich ,dung khoang cach(h) va trong so(g) de tinh (f) va tri thuc bo sung (h) nham thu hep khoang cach tim kiem, giam thieu cac buoc va tang toc do tim kiem ma khong can phai duyet tung nhanh cua cay

trang thai dich mac dinh co dang:

1  2  3
4  5  6
7  8  0

voi n = 3 (8-puzzle)

---

## thuat toan su dung

### 1. greedy best-first search (akt)

greedy best-first search lua chon trang thai tiep theo dua tren gia tri heuristic h(n), tuc la do "gan dich" cua trang thai do.

* ham uu tien: f(n) = h(n)
* uu diem: tim nhanh
* nhuoc diem: khong dam bao loi giai toi uu

### 2. a* search

a* search la thuat toan tim kiem toi uu ket hop giua chi phi thuc te va heuristic.

* ham uu tien: f(n) = g(n) + h(n)
* g(n): so buoc tu trang thai ban dau
* h(n): heuristic
* uu diem: dam bao tim duoc duong di ngan nhat neu heuristic hop le

---

## heuristic su dung

chuong trinh su dung heuristic "misplaced tiles":

* dem so luong o khong nam dung vi tri so voi trang thai dich
* bo qua o trong (0)

heuristic nay la admissible (khong danh gia qua cao), phu hop cho a* search.

---

## cau truc chuong trinh

* puzzlesolverbase: lop co so truu tuong dung chung cho a* va greedy
* akt: ke thua puzzlesolverbase, cai dat greedy best-first search
* astar: ke thua puzzlesolverbase, cai dat a* search
* get_puzzle_input(): ham nhap du lieu tu nguoi dung
* main: chay chuong trinh va thuc thi cac thuat toan

---

## huong dan chay chuong trinh

### yeu cau

* python 3.8 tro len
* khong can thu vien ben ngoai

### cach chay

```bash
python main.py
```

sau do:

1. nhap kich thuoc n (vi du: 3)
2. nhap n*n so cho trang thai ban dau (0 la o trong)

vi du input:

```text
nhap kich thuoc ma tran n: 3
trang thai ban dau: 1 2 3 4 0 5 7 8 6
```

chuong trinh se lan luot chay:

* greedy best-first search
* a* search

va in ra cac buoc giai chi tiet tren console.

---

## vi du ket qua

* in ra trang thai ban dau va trang thai dich
* hien thi so buoc di
* hien thi tung trang thai trung gian cho den khi giai xong

---

## nhan xet

* greedy best-first search chay nhanh nhung co the cho loi giai khong toi uu
* a* search chay cham hon nhung dam bao tim duoc duong di ngan nhat



* chuong trinh chay tren console, khong xay dung giao dien web hay gui
* ma nguon duoc chu thich de de hieu va de mo rong trong tuong lai
