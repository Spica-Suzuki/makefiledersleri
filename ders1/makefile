#hello:
#	echo "hello world"

# hello'nun ne yapacağını söyler o da echodur. make dendiğinde olan olayları ekrana çıktı verir.
#makefile sinteksi:

#Hedefler: ön koşullar
#Komutlar
#komutlar
#komutlar

blah: blah.o
	cc blah.o -o blah # üçüncü olarak yürür

blah.o: blah.c
	cc -c blah.c -o blah.o # ikinci oalrak yürür

blah.c:
	echo "int main() { return 0; }" > blah.c # İlk yürür

# blah blah.o ilk koşuluna bakar. o da blah.c önkoşuluna bakar.  O da komutu verir. 
#Bu sebeple komutların sırası değil önkoşullar daha önemlidir.

hello:
	echo "Hello, World"
	echo "bu cümle her zaman bastırılır çünkü hello diye bir dosya yoktur"

#Hello adında tek bir hedefimiz var
#Bu hedef iki komuta sahip
#Bu hedef hiç ön-gereksinime sahip değil.

#daha sonra "make hello"yu yürüteceğiz. Hello dosyası var olmadığı sürece,
# komutlar çalışacaktır. eğer hello dosyası varsa h,içbir komut çalışmayacaktır.

#Benim hem hello dosyası hem de hello hedefinden bahsettiğimi fark etmek önemlidir.
# Çünkü bu ikisi birbirine doğrudan bağlıdırlar. Hedef yürürken
# (hedefin komutları yürürken.), Komutlar hedef ile aynı isme sahip bir dosya yaratacaktır
# Bu durumda, hello hedefi hello dosyasını yaratmaz.