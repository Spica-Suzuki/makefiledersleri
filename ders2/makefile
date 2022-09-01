#Hadi daha tipik bir makefile oluşturalım
# tek bir C dosyası derlesin. 
#Ama bunu yapmadan önce, blah.c adında aşağıdaki içeirklere sahip bir dosya oluşturalım:

#// blah.c
#int main() { return 0; }

#Sonra makefile dosyası oluşturalım

#blah:
#	cc blah.c -o blah

#Bu sefer, basitçe "make"'i çakıştırmayı deneyelim. 
#burada "make" komutuna argüman olarak sağlanan hiçbir hedef olmadığı sürece,
#ilk hedef yürüyecektir. Bu durumda, ortada tek hedef vardır (blah).
#Bunu ilk defa yürüttüğünüzde, blah yaratılacaktır. ikinci seferde, göreceksiniz ki:

# make:'blah' is up to date. 

#Bunun sebebi blah dosyasının çoktan var olmasıdır. Ancak burada bir problem var:
#Eğer blah.c'yi modifiye edersek ve tekrar "make"i yürütürsek, hiçbir şey yeniden derlenmez.

#Bunu bir önkoşul ekleyerek çözeceğiz:

blah: blah.c
	cc blah.c -o blah

#"make"i tekrar yürüttüğümüz zaman, bir dizi adımlar gerçekleşir:

#İlk hedef seçildi, çünkü ilk hedef varsayılan hedef
#blah.c'nin bir ön-koşuluna sahip.
#"blah" hedefinin yürülmesine "make" karar verir. 
#bu sadece blah.c yoksa ve blah.c blah'dan daha yeni ise yürütülür.

#Bu son adım kritiktir ve "make"'in özüdür.
#Yaptığı şey  blah'ın ön-koşullar'ı eğer blah 
#Son derlendiğinden beri değişmş ise ise bunu saptamaktır. 
#Bu kadar, eğer blah.c değiştirilmişse make'i yürütmek blah'ı yeniden derler.
#Ve tersine, eğer blah.c değişmediyse, yeniden derlenmelidir.

#Bunu yapmak için,
#Dosya sisteminin zaman damgalarını bir şeyin değişip değişmediğini saptamak
#adına proxy sunucusu oalrak kullanır
#Bu pratik nedenlerledir, çünkü dosya zaman işaretleri tipik oalrak sadece
#dosyalar modifiye edildiğinde değişir. Ama bunun tek etken olmadığının farkına varmak da önemlidir.
#Bir dosya modifiye edebilirsiniz ve modifiye edilen zaman damgasını daha eski bir şeye 
#değiştirebilirisniz. bunu yaptıysanız make yanlış şekilde o dosyanın daha önceden değiştirilmediğini
#düşündüğünden görmezden gelebilir
