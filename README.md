# MetroSimulation
Bu proje, en kısa yolu bulmak için BFS ve A* algoritmalarını kullanarak haritalar üzerindeki en etkili rota planlamasını yapmayı amaçlamaktadır.

# Kullanılan Kütüphaneler: 
collections defaultdict : anahtar bulunmazsa otomatik olarak varsayılan değer döner <br>
collections deque : iki uçtan veri ekleyip çıkarılabilen hızlı bir kuyruk yapısı <br>
heapq: küçükten büyüğe sıralı bir yapı oluşturur ve en küçük ögeye hızlı erişim sağlar. <br>

# Kullanılan Algoritmalar:

#### BFS algoritması,
genişlik öncelikli bir arama algoritmasıdır.<br>
başlangıç düğümü kuyruğa eklenir.<br>
kuyruğun başındaki düğüm işlenir ve komşuları kuyruğa eklenir.<br>
hedef düğüm bulunana kadar süreç devam eder.<br>
bulunan en kısa yolu geriye doğru takip eder.<br>

#### A* algoritması, 
Dijkstra ve Greedy Best-First Search yaklaşımlarını birleştiren akıllı bir arama algoritmasıdır.<br>
bir öncelik kuyruğu (priority queue) kullanarak düğümleri işler.<br>
her düğümün toplam maliyeti (g + h) hesaplanır.<br>
g: Başlangıç düğümünden mevcut düğüme olan gerçek maliyet.<br>
h: Mevcut düğümden hedefe olan tahmini maliyet (heuristic function).<br>
en düşük maliyetli düğüm önce işlenir.<br>
hedefe ulaşıldığında en kısa yolu geriye doğru takip eder.<br>

# Neden BFS ve A*?
BFS : ağırlıksız grafta en kısa yolu bulur. basit ve verimli bir yapıya sahiptir. <br>

A* : Dijkstra’dan daha hızlıdır çünkü sadece en umut verici yolları genişletir,Heuristic (h) fonksiyonu sayesinde akıllı seçimler yapar<br>
Yol bulma (pathfinding) problemlerinde en iyi performanslardan birini sunar.<br>

# Örnek çıktı
AŞTİ'den OSB'ye:<br>
En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB<br>
En hızlı rota (18 dakika): AŞTİ -> Kızılay -> M2 -> Sıhhiye -> Gar -> OSB<br>


# Proje geliştirme fikirleri 
kullanıcıya hatlar arasında bağlantılar ekleyebilme veya mevcut bağlantıları güncelleyebilme yeteneği verilebilir.<br>
her istasyon ve hat için bir zaman çizelgesi oluşturabilir ve bu zaman çizelgesine göre rotalar hesaplanabilir. Ayrıca, duraklardaki bekleme süreleri de hesaba katılabilir.<br>
navigasyon sistemlerinde bu algoritmaları entegre edebiliriz
