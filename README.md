Metro Simulation
Bu proje, haritalar üzerindeki en kısa yolu bulmak için BFS ve A* algoritmalarını kullanarak etkili rota planlaması yapmayı amaçlamaktadır.

Kullanılan Kütüphaneler
collections.defaultdict: Anahtar bulunmadığında otomatik olarak varsayılan değer döner.

collections.deque: İki uçtan veri ekleyip çıkarılabilen hızlı bir kuyruk yapısı sağlar.

heapq: Küçükten büyüğe sıralı bir yapı oluşturur ve en küçük öğeye hızlı erişim sağlar.

Kullanılan Algoritmalar
BFS (Breadth-First Search)
BFS, genişlik öncelikli bir arama algoritmasıdır. Algoritmanın işleyişi şu şekildedir:

Başlangıç düğümü kuyruğa eklenir.

Kuyruğun başındaki düğüm işlenir ve komşuları kuyruğa eklenir.

Hedef düğüm bulunana kadar süreç devam eder.

Bulunan en kısa yol geriye doğru takip edilerek sonuç elde edilir.

BFS, özellikle ağırlıksız grafiklerde en kısa yolu bulmada etkili ve basit bir yöntemdir.

A* (A-star)
A* algoritması, Dijkstra ve Greedy Best-First Search yaklaşımlarını birleştirir ve akıllı bir arama algoritmasıdır. Algoritmanın işleyişi şu şekildedir:

Bir öncelik kuyruğu (priority queue) kullanarak düğümler işlenir.

Her düğüm için toplam maliyet (g + h) hesaplanır:

g: Başlangıç düğümünden mevcut düğüme kadar olan gerçek maliyet.

h: Mevcut düğümden hedefe olan tahmini maliyet (heuristic function).

En düşük maliyetli düğüm önce işlenir.

Hedefe ulaşıldığında, en kısa yol geriye doğru takip edilerek sonuç elde edilir.

A* algoritması, Dijkstra’dan daha hızlıdır, çünkü sadece en umut verici yolları genişletir ve Heuristic (h) fonksiyonu sayesinde akıllı seçimler yapar. Bu, yol bulma (pathfinding) problemlerinde yüksek performans sağlar.

Neden BFS ve A*?
BFS: Ağırlıksız grafikte en kısa yolu bulur, basit ve verimli bir yapıya sahiptir.

A*: Dijkstra'dan daha hızlıdır çünkü yalnızca en umut verici yolları genişletir ve Heuristic fonksiyonu sayesinde daha akıllıca seçimler yapar. Bu özellik, yol bulma (pathfinding) problemlerinde en iyi performansları sunar.

Örnek Çıktı
AŞTİ'den OSB'ye:

En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

En hızlı rota (18 dakika): AŞTİ -> Kızılay -> M2 -> Sıhhiye -> Gar -> OSB

Proje Geliştirme Fikirleri
Kullanıcıya hatlar arasında bağlantılar ekleyebilme veya mevcut bağlantıları güncelleyebilme yeteneği verilebilir.

Her istasyon ve hat için bir zaman çizelgesi oluşturulabilir. Bu zaman çizelgesine göre rotalar hesaplanabilir. Ayrıca, duraklardaki bekleme süreleri de hesaba katılabilir.

Navigasyon sistemlerinde bu algoritmalar entegre edilebilir.
