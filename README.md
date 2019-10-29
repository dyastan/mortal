# mortal

/*contoh program sederhana array di dalam struct*/

#include <iostream>
#include <stdio.h>
#include <conio.h>
#include <string.h>
#include <iomanip>
using namespace std;



main ()
{
	struct TMhs
{
char NIM[9];
char Nama[21];
int NilaiUTS,NilaiUAS,NilaiQuis;
float NilaiAkhir;
char index;
};
TMhs mhs[40];
int i,jml;
cout << "jumlah data mahasiswa yang akan diinputkan :";cin>>jml;
for(i=0;i<jml;i++){

cout << "Pengisian Data Mahasiswa Ke-"<<i+1<< endl;

cout << "NIM : "; cin >> mhs[i].NIM;

cout << "NAMA : "; cin >> mhs[i].Nama;

cout <<"Nilai Quiz : ";cin >> mhs[i].NilaiQuis;

cout <<"Nilai UTS : ";cin >> mhs[i].NilaiUTS;

cout <<"Nilai UAS : ";cin >> mhs[i].NilaiUAS;

mhs[i].NilaiAkhir=0.2*mhs[i].NilaiQuis+0.3*mhs[i].NilaiUTS+0.5*mhs[i].NilaiUAS;

if(mhs[i].NilaiAkhir>=80) {
mhs[i].index ='A';}else if(mhs[i].NilaiAkhir>=60) {
mhs[i].index ='B';}else if(mhs[i].NilaiAkhir>=40) {
mhs[i].index ='C';}else if(mhs[i].NilaiAkhir>=20) {
mhs[i].index ='D';}else if(mhs[i].NilaiAkhir>=0) {
mhs[i].index ='E';}
};

cout <<"Data yang telah dimasukkan adalah : \n";
cout <<"---------------------------------------------- \n";
cout <<"| NIM | NAMA | QUIS | UTS | UAS | NA | INDEX | \n";
cout <<"---------------------------------------------- \n";
for(i=0;i<jml;i++)
{

cout << ""<<setiosflags(ios::right)<<setw(5)<<mhs[i].NIM;
cout << ""<<setiosflags(ios::right)<<setw(6)<<mhs[i].Nama;
cout << ""<<setiosflags(ios::right)<<setw(7)<<mhs[i].NilaiQuis;
cout << ""<<setiosflags(ios::right)<<setw(6)<<mhs[i].NilaiUTS;
cout << ""<<setiosflags(ios::right)<<setw(6)<<mhs[i].NilaiUAS;
cout << ""<<setiosflags(ios::right)<<setw(6)<<mhs[i].NilaiAkhir;
cout << ""<<setiosflags(ios::right)<<setw(6)<<mhs[i].index<<endl;
}
cout<<"---------------------------------------------- \n";
getch();
return 0;
}
