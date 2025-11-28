# DRL_Vize
Trafik Işığı Kontrolü
Kuzey-Güney yönünde 1 gidiş 1 geliş toplam 2 şerit
Dağu- Batı yönünde 1 gidiş 1 geliş toplam 2 şerit
20x20 grid
Ajan Q-learning kullanıyor (yeni_q = mevcut_q + self.alpha * (odul + self.gamma * en_iyi_yeni - mevcut_q)
Epsilon-Greedy keşif stratejisi var
Keşif / sömürü dengesi, ajan hem keşfediyor hem öğreniyor.
if random.random() < self.epsilon:
    return random.choice([0,1])
else:
    return np.argmax(self.q_table[durum])
    Eğitim döngüsü (episode + adım) var
    for ep in range(epizod_sayisi):
    durum = env.reset()
    for adim in range(adim_sayisi):
    Her 5 epizotta kavşağı gerçek zamanlı gösteriyor
    Console log (öğrenme çıktısı)
    Her adımda yazdırılan:
Epizod=2, Adım=35, Faz=1, Ödül=-8, Toplam=-125.0
faz seçimi, anlık ödül, toplam ödül, performans anlık izlenebiliyor





