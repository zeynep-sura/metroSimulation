# MetroSimulation
Bu proje, en kısa yolu bulmak için BFS ve A* algoritmalarını kullanarak haritalar üzerindeki en etkili rota planlamasını yapmayı amaçlamaktadır.

## Kullanılan Kütüphaneler: 
collections defaultdict : anahtar bulunmazsa otomatik olarak varsayılan değer döner
collections deque : iki uçtan veri ekleyip çıkarılabilen hızlı bir kuyruk yapısı
heapq: küçükten büyüğe sıralı bir yapı oluşturur ve en küçük ögeye hızlı erişim sağlar.

# Kullanılan Algoritmalar:

# BFS algoritması,
genişlik öncelikli bir arama algoritmasıdır.
başlangıç düğümü kuyruğa eklenir.
kuyruğun başındaki düğüm işlenir ve komşuları kuyruğa eklenir.
hedef düğüm bulunana kadar süreç devam eder.
bulunan en kısa yolu geriye doğru takip eder.

# A* algoritması, 
Dijkstra ve Greedy Best-First Search yaklaşımlarını birleştiren akıllı bir arama algoritmasıdır.
bir öncelik kuyruğu (priority queue) kullanarak düğümleri işler.
her düğümün toplam maliyeti (g + h) hesaplanır:
g: Başlangıç düğümünden mevcut düğüme olan gerçek maliyet.
h: Mevcut düğümden hedefe olan tahmini maliyet (heuristic function).
en düşük maliyetli düğüm önce işlenir.
hedefe ulaşıldığında en kısa yolu geriye doğru takip eder.

#### Neden BFS ve A*?
BFS : ağırlıksız grafta en kısa yolu bulur. basit ve verimli bir yapıya sahiptir. 

A* : Dijkstra’dan daha hızlıdır çünkü sadece en umut verici yolları genişletir,
Heuristic (h) fonksiyonu sayesinde akıllı seçimler yapar
Yol bulma (pathfinding) problemlerinde en iyi performanslardan birini sunar.

##### Örnek çıktı
AŞTİ'den OSB'ye:
En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
En hızlı rota (18 dakika): AŞTİ -> Kızılay -> M2 -> Sıhhiye -> Gar -> OSB


###### Proje geliştirme fikirleri 
kullanıcıya hatlar arasında bağlantılar ekleyebilme veya mevcut bağlantıları güncelleyebilme yeteneği verilebilir.
her istasyon ve hat için bir zaman çizelgesi oluşturabilir ve bu zaman çizelgesine göre rotalar hesaplanabilir. Ayrıca, duraklardaki bekleme süreleri de hesaba katılabilir.
navigasyon sistemlerinde bu algoritmaları entegre edebiliriz
