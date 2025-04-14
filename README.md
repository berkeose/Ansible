# Ansible

## ANSIBLE NEDİR?
#### Temel olarak bulut provizyonu, konfigürasyon yönetimi, uygulama dağıtımı sunucu işlemleri, güvenlik olaylarını ve bir çok bilgi teknolojileri ihtiyaçlarını otomatikleştirebilen bir otomasyon motorudur. Ansible çok katmanlı dağıtımlar için tasarlanmıştır. Bir sistemi yönetmekten öte biribirleyirle ilişkili tüm sistemleri yönetebilme olanağını sunmaktadır. Client istemcilere herhangi bir agent kurma ihtiyacı gerektirmeyen, Python ve Ruby dilleri ile geliştirilmiş özgür bir platformdur. Şuan da redhat çatısı altında bulunan ansible open source ve ticari olarak faliyet göstermektedir.


#### Ansible ile çalışmak çok kolaydır; bağlanmak için düğümlerinize “Ansible Modules” adı verilen küçük programları gönderir. Modülleri yürütmek için SSH aracısını kullanarak konumlandırabiliriz ve bağlanabilirler ve bittiğinde o eklenen Ansible Modules kaldırılır. Bu modüllerin makinelerde herhangi bir yerde bulunabilmesi için gerekli hiçbir sunucu, arka plan programı veya veri tabanı yoktur. İçerikteki değişiklikleri yönetmek için herhangi bir metin düzenleyici veya terminal programı ve bir sürüm kontrol sistemi ile birlikte çalışmanız gerekir. Ansible, içinde yerleşik 750’den fazla modüle sahiptir.

![ansible](https://user-images.githubusercontent.com/81867200/188466994-7bf93314-c53d-4361-af2a-745da3fce409.png)
 
#### Ansible’da parolalar desteklenir, ancak Ansible ile çalışma yöntemlerinden biri olarak ssh-agent’larla SSH anahtarlarını kullanabilirsiniz.ssh-copy-id parametresi sayesinde Ansible işlerini yöneteceğimiz olan master sunucuyu bu parametre bilgisi eklenerek gerçekleştirebiliriz.Herhangi bir kullanıcı hesabı oluşturabilirsiniz ve kök kullanıcı gereklidir. Hangi makinelerin hangi ana bilgisayarlara erişebileceğini yapılandırmak için “yetkili_anahtar” adlı bir modül vardır. 

#### Ansible’a basit bir metin biçiminde makineler ekleyebilir ve envanterinizi yönetebilirsiniz. Rackspace, EC2 ve Openstack gibi diğer kaynaklardan gelen envanter ve değişken bilgileri kullanabilir. Kodunuzu yazmanız gerekiyorsa, Ansible’ı Python, Ruby ve Bash gibi JSON döndüren dillerde de kullanabilirsiniz. Modüllerinizi, API’nizi ve Eklentilerinizi yazabilirsiniz. Playbook’lar, birden çok altyapıyı tek seferde düzenlemek için kullanılan basit ve güçlü otomasyon dilidir. Bu Ansible’da yapılabilir.

### Ansible’a ihtiyacımız var mı?  Varsa Neden?
#### Ansible çok kullanışlıdır ve yapılandırılacak ve dağıtılacak 4 veya 5 web sunucusu olduğunda ve yapılandırılacak ve dağıtılacak 4’ten fazla veritabanı sunucusu olduğunda bu örneği takdir edersiniz. Web sunucularında uygulamalar vardır ve arka uçta veritabanı sunucularını birbirine bağlar. Artık geleneksel durum, bu sunucuları ayrı ayrı yapılandırmanızı ve yönetmenizi gerektiriyor.

#### Ancak bu sunucularda çeşitli uygulama güncellemeleri olacaktır. Daha fazla sunucu varsa ve bunların yapılandırmaları aynı olmayacaksa, bir sistem yöneticisi bile işleyemez. Bu görevler, sistem yöneticisinin yanı sıra uygulamaları geliştiren geliştiriciler tarafından çok fazla çaba sarf etmeden sunucu sayısını yapmak ve yönetmek karmaşıktır. Kuruluşun DNS, NTP, AD, E-posta vb. gibi sahip olduğu diğer sunucuları hayal edin.

#### Ansible’ın resme girdiği yer burasıdır. Altyapı otomasyonu ve orkestrasyonları Ansible tarafından yapılabilir. Tüm benzer sunucular Ansible tarafından tek seferde işlenebilir ve yönetilebilir.

#### Ansible’ın Kullanım Alanları
Ansible’ın kullanım durumları aşağıda listelenmiştir.

Altyapı Sağlama (Infrastructure Provisioning)
Konfigürasyon yönetimi (Configuration Management)
BT otomasyonu (IT automation)
Sürekli dağıtım (Continuous deployment)
Uygulama geliştirme (Application Development)
Ağ Otomasyonu (Network Automation)
Güvenlik Otomasyonu (Security Automation)
Altyapı Orkestrasyon (Infrastructure Orchestration)

### ANSIBLE'IN TEMEL ELEMENLARI
#### Inventory : Ansible'ın yöneteceği sunucu adları veya IP adreslerinin tanımlandığı belge
#### Module: Bağımsız komut dosyalarıdır.
#### Fact: Uzak Sistem verilerini otomatik olarak keşfeder ve edindiği bilgileri görüntüler.
#### Play: Her bir görev play olarak adlandırılır.
#### Playbook: Tüm görevlerin tanımlandığı yapılandırma belgesinin adı playbooktur.

### Ansible İle Ne Yapılabilir?
#### Konfigürasyon Yönetimi (Configuration Management ) – Kurumsal donanım ve yazılım bilgileri ayrıntılı olarak kaydedilir ve güncellenir, böylece ürün performansının tutarlılığı korunur.
Uygulama Dağıtımı (Application Deployment) – Uygulamaları Ansible kullanarak tanımladığınızda ve yönettiğinizde, uygulamalar Geliştirmeden Üretime Ansible’da yönetilebilir.
Orkestrasyon (Orchestration) – Bir bütün olarak ve konfigürasyonların nasıl etkileşime girdiğini yönetmek için kullanırız.
Güvenlik ve Uyumluluk (Security and Compliance) – Politika Ansible’da tanımlandığında, altyapı genelinde geniş güvenlik politikası dağıtılabilir
Sağlama (Provisioning) – Süreci otomatikleştirmemize ve yönetmemize yardımcı olur

## Ansible Architecture’a genel bakış
![Ansible-Orchestration](https://user-images.githubusercontent.com/81867200/188469216-8247c65b-41c4-4034-939a-927009907d43.png)
### Ansible Orchestration motoru, Ansible aracının merkezidir.

### Süreci yapılandırmak, yönetmek, otomatikleştirmek ve düzenlemek için yazılmış bir Envanter tablosu, API, Eklentiler ve modüllerden oluşur.
Ağ oluşturmayı ana bilgisayarları veya sunucuları, işletim sistemlerini yönetmek ve güvenliği yönetmek için Playbook yazılımından, genel/özel buluttan ve yapılandırma yönetimi veritabanlarından girdi alabilir.

## INVENTORY
### MEVCUTTA KULLANLAN TĞM SUNCULARIN IP ADRESLERİNİ GİRECEĞİZ.
![ans](https://user-images.githubusercontent.com/81867200/188875254-c85ed25e-d17d-4d5a-a157-662187a1bec6.png)


ssh-keygen -t ed25519 -C "Ansible Anahtari"  anahtar oluşturma


ssh-copy-id -i /home/theadmin/.ssh/ansible.pub  192.168.0.0 ---> buraya kopyala

sudo apt install software-properties-common ---> ansible kurmadan önce indirilmeli

sudo add-apt-repository --yes --update ppa:ansible/ansible --> ansible'in kurulumu için repository ekleme ve tanımlama işlemi

sudo apt install ansible --> ansible kurulum

ansible all --key-file ~/.ssh/ansible -i inventory -m ping  --> keyleri al dizinden inventorydekleri pingle komutu ( config dosyası oluşturursan oradan da aynı işlemi yaparsın ansible all -m ping yeterli olacaktır. )

cat /etc/ansible/ansible.cfg ---> ansible'in kendi config dosyası

ad-hoc commands --> bir veya birden fazla node'da tek bir görevi otomatikleştirmek için kullandıgımız komut satırı aracıdır (tek kullanımlıktır)

 ansible all -a "/sbin/reboot" --become --ask-become-pass  --> reboot et ve yetki al yetki içinde passw sor 

 ansible all -m apt -a name=hwinfo --become -K ---> bütün node'lara paket indirmek için kullanbilir (-K yukaridakinin kısaltımıdır). Ad-hoc commandleriyle playbookta yapabiliceğimiz herşeyi yapabiliriz.

 cat /var/log/apt/history.log ---> logları kontrol etmek

 git config --global user.name "BERKE KOSE" ---> git'e commit edebilmek için

 ansible all -m apt -a "upgrade=dist" --become -K ---> Ansible ile envanterdeki tüm makinelerde apt-get dist-upgrade yap, ama bu işlemi sudo ile çalıştır ve sudo parolamı da sor.

  ansible-playbook --ask-become-pass apche_yukleme.yml --> apche_yukleme.yml adlı Ansible playbook dosyasını çalıştır, işlemleri sudo (yani yönetici yetkisiyle) yapacağım için şifremi sor.

  ansible all -m gather_facts --limit 192.168.0.102 | grep ansible_distribution --> burdan factleri çağır greple özel çağrı yapabiliriz.



