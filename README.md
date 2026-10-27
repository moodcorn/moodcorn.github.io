# moodcorn.github.io

Moodcorn uygulamasının internet sitesi ve film listesi.

- `index.html`: ana sayfa (ileride gizlilik politikası da burada olacak)
- `data/catalog.json`: uygulamanın kullandığı film ve dizi listesi
- `data/version.json`: listenin sürüm numarası

## Uygulama listeyi nasıl günceller?

Uygulama her açılışta yalnızca küçük `version.json` dosyasına bakar.
Buradaki `version`, telefondaki listeden büyükse `catalog.json`'u indirir.
Sürüm aynıysa hiçbir şey indirmez.

## Listeyi güncellerken

1. `catalog.json` içindeki `"version"` sayısını bir artır.
2. `version.json` içindeki `"version"` sayısını da aynı yap.
3. İki dosyayı birlikte yükle.

`format` sayısına dokunma. O, listenin yapısı değişirse artar ve eski
uygulamaların okuyamayacağı bir listeyi indirmesini engeller.
