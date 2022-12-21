# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar Pemograman
<br>Nama		      : Aisyah Muthmainnah
<br>NIM		        :	1227050012
<br>Jurusan		    :[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
ource code yang digunakan untuk membuat array dua dimensi. Program yang digunakan untuk mencari bilangan yang tidak habis dibagi 3,5,7.
Dengan algoritma :
1. User menginputkan banyaknya baris dan kolom dengan jangkauan 0-20
2. User menginputkan nilai array satu persatu
3. Output nilai sesuai dengan matriks
4. Lalu dicek oleh program apakah nilai tersebut habis dibagi 3,5 dan 7
5. Apabila nilai habis dibagi 3,5 dan 7, maka nilai tidak akan ditampilkan. Jika tidak habis, nilai ditampilkan kembali

## Source Code
      #include <iostream>
      using namespace std;

      int main (){
        int A [20][20];
        int baris, kolom, i, j;
        cout << "Masukkan jumlah baris : ";
        cin >> baris;
        cout << "Masukkan jumlah kolom : ";
        cin >> kolom;

        for (i=0; i<= baris -1; i++) {
          for(j=0; j<=kolom -1; j++) {
            cout << "Masukkan nilai (" << i << "." << j << ") : ";
            cin >> A [i][j];
          }
        }
        cout << "Nilai yang diinputkan : \n";
        for(int i = 0; i < baris; i++){
          for(int j = 0; j < kolom; j++){
            cout << A[i][j] << "\t";
          }
          cout<<endl;
        }
        int angka[20];
        int index = 0;
        for(i=0; i<baris ; i++){
          for(j=0; j<kolom; j++) {
            if (A [i][j]%3 != 0 && A[i][j]%5 != 0 && A[i][j]%7 != 0){
              angka[index] = A[i][j];
              index++;
            }
          }
        }
        cout<<"Angka yang tidak bisa dibagi 3, 5, 7 adalah ";
        for(int i = 0; i < index; i++){
          cout<<angka[i]<<", ";

        }
      }

## Output
![image](https://user-images.githubusercontent.com/121163710/208887566-70b134a1-45cf-42bd-848f-ce9af56d3727.png)
