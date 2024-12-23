
# Глава 11: Мрежово администриране

Мрежовото администриране е процес на управление, поддръжка и мониторинг на компютърните мрежи, за да се гарантира тяхната ефективност, сигурност и безпроблемна работа. Това включва конфигуриране на устройства, следене на мрежовия трафик и реагиране при възникване на проблеми.

## 11.1. Основни задачи на мрежовия администратор

### 11.1.1. Управление на мрежови устройства:
- Конфигуриране на устройства като рутери, суичове, точки за достъп и защитни стени.
- Актуализация на фърмуер за подобряване на сигурността и функционалността.

**Пример:**  
Мрежовият администратор настройва суич, за да създаде VLAN (виртуални локални мрежи) за различни отдели в компанията.

### 11.1.2. Управление на IP адреси:
- Използване на DHCP сървъри за автоматично разпределение на IP адреси.
- Поддръжка на IP адресна схема, която е оптимизирана и без конфликти.

**Пример:**  
IT екипът конфигурира DHCP сървър, за да раздава адреси в диапазона 192.168.1.100–192.168.1.200.

### 11.1.3. Мониторинг на мрежовия трафик:
- Използване на инструменти за анализ на мрежовия трафик (напр. Wireshark, SolarWinds).
- Засичане на подозрителни дейности или претоварвания в мрежата.

**Пример:**  
При необичайно високо натоварване на мрежата, администраторът използва Wireshark, за да идентифицира източника на проблема.

### 11.1.4. Управление на потребители:
- Добавяне и премахване на потребители от мрежата.
- Настройка на права за достъп до ресурси като файлове, принтери или приложения.

**Пример:**  
Нов служител получава достъп до принтера в отдела чрез мрежовия сървър.

### 11.1.5. Реакция при инциденти:
- Засичане и справяне с мрежови проблеми като прекъсвания, атаки или хардуерни повреди.
- Създаване на резервни копия (backups) за бързо възстановяване.

**Пример:**  
След DDoS атака, администраторът пренасочва мрежовия трафик и блокира злонамерените IP адреси.

## 11.2. Мрежово мониториране

### 11.2.1. Инструменти за мрежово наблюдение:
- **Wireshark:**  
  Анализира пакети данни в реално време. Помага за откриване на проблеми като загубени пакети или подозрителен трафик.

- **Nagios:**  
  Система за мониторинг на сървъри и мрежови устройства. Изпраща известия при възникване на проблеми.

- **SolarWinds:**  
  Предлага функции за наблюдение на мрежи и управление на производителността.

### 11.2.2. Ключови метрики за мониторинг:
- **Използване на честотна лента:** Проверява се дали капацитетът на мрежата е претоварен.
- **Загуба на пакети:** Високата загуба на пакети показва проблеми със свързаността.
- **Закъснение (latency):** Високото закъснение води до забавяне в комуникацията.

**Пример:**  
Администраторът забелязва необичайно натоварване на честотната лента и установява, че голямо количество данни се прехвърля от необозначен източник.

## 11.3. Управление на потребители и достъп

### 11.3.1. Политики за достъп:
Определят какви ресурси са достъпни за различните потребители. Включват контрол на правата чрез ACL (Access Control Lists).

**Пример:**  
Служител от маркетинговия отдел има достъп само до споделената папка на отдела, но не и до базата данни на ИТ отдела.

### 11.3.2. Аутентикация и удостоверяване:
- **Системи за еднократно влизане (SSO):**  
  Потребителят се логва веднъж, за да получи достъп до всички мрежови ресурси.

**Пример:**  
Google Workspace.

- **Двуфакторна аутентикация (2FA):**  
  Повишава сигурността чрез допълнителен фактор за удостоверяване (напр. SMS код или приложение).

**Пример:**  
Служител влиза в корпоративната мрежа, като потвърджа самоличността си с парола и код, изпратен на телефона.

## 11.4. Резервиране и възстановяване

### 11.4.1. Резервни копия (Backups):
Редовно създаване на резервни копия на мрежови настройки, данни и системи.  
Използване на локални сървъри или облачни услуги за съхранение.

**Пример:**  
Администраторът създава дневни резервни копия на корпоративния сървър, за да предотврати загуба на данни.

### 11.4.2. Планове за възстановяване (Disaster Recovery):
Изготвяне на стратегия за бързо възстановяване на мрежата при сривове или атаки.  
Тестове на възстановителните процедури.

**Пример:**  
След повреда на основния сървър, мрежовият администратор стартира резервен сървър и възстановява системата за по-малко от час.

## Примерна организация на мрежово администриране:

### Сценарий: Корпоративна мрежа
1. Мрежовият администратор използва Nagios за наблюдение на устройствата и производителността.
2. Системата за управление на достъпа (ACL) определя права за всеки служител.
3. Резервни копия на сървърите се създават всяка нощ.
4. При инцидент, администраторът използва Wireshark за диагностициране на проблема и предприема действия за възстановяване.
