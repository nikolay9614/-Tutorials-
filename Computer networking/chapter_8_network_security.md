
# Глава 8: Сигурност на компютърните мрежи

Сигурността на компютърните мрежи се фокусира върху защитата на данни и ресурси от неоторизиран достъп, злоупотреба или унищожение. Тя е от съществено значение в съвременния свят на глобална свързаност.

## 8.1. Основни заплахи и атаки

### 8.1.1. Видове заплахи:

- **Злонамерен софтуер (Malware):**  
  Включва вируси, троянски коне, рансъмуер и шпионски софтуер.  
  **Пример:** Вирус, който криптира файлове и изисква откуп за декриптиране.

- **Фишинг (Phishing):**  
  Измамни опити за получаване на лични данни чрез имейли или уеб страници, които изглеждат легитимни.  
  **Пример:** Имейл от „банка“, който изисква вашата парола.

- **DDoS атаки (Distributed Denial of Service):**  
  Атаки, които претоварват сървърите, правейки ги недостъпни за легитимни потребители.  
  **Пример:** Хакерска атака, която спира работа на уебсайт чрез изпращане на милиони заявки.

- **Мрежово подслушване (Eavesdropping):**  
  Незаконно прихващане на комуникация чрез използване на мрежови инструменти.

- **Манипулация в средата (Man-in-the-Middle):**  
  Хакер прихваща и променя комуникацията между две страни, без те да забележат.

## 8.2. Мрежови защити

### 8.2.1. Firewall (Мрежова стена):
Устройство или софтуер, който контролира достъпа до мрежата чрез филтриране на трафика.

**Видове:**
- **Пакетен филтър:** Проверява IP адресите и портовете.
- **Състояние на сесиите:** Следи активните сесии за допълнителна сигурност.

### 8.2.2. VPN (Virtual Private Network):
Създава криптирана връзка между устройства, като защитава данните от прихващане.  
**Пример:** Дистанционен служител използва VPN, за да се свърже със служебната мрежа.

### 8.2.3. IDS/IPS (Intrusion Detection/Prevention Systems):
- **IDS:** Открива подозрителна активност и известява администратора.
- **IPS:** Активно предотвратява подозрителната активност, като блокира злонамерени заявки.

### 8.2.4. Антивирусен софтуер:
Сканира за и премахва злонамерен софтуер.  
Постоянно актуализира базите данни за защита от нови заплахи.

## 8.3. Криптиране и управление на ключове

### 8.3.1. Криптиране:
Криптирането защитава данните, като ги прави неразбираеми за неоторизирани лица.

**Видове криптиране:**
- **Симетрично (AES):** Един ключ за криптиране и декриптиране.
- **Асиметрично (RSA):** Публичен ключ за криптиране и частен ключ за декриптиране.

### 8.3.2. Управление на ключове:
Управлението на криптографските ключове е критично за сигурността.  
**PKI (Public Key Infrastructure):** Система за управление на публични и частни ключове.

**Пример:**  
HTTPS използва TLS криптиране, което защитава данните между браузъра и сървъра.

## Примерна реализация на мрежова сигурност:

### Сценарий:
1. Компания използва **Firewall**, за да ограничи достъпа до вътрешната мрежа.
2. Служителите използват **VPN**, за да работят дистанционно, като данните са криптирани.
3. **IDS/IPS** следи за подозрителна активност, като блокира DDoS атаки.

Това е преглед на основите на мрежовата сигурност. Ако желаете, мога да премина към следващата глава за мрежови устройства или да разгледам някой от аспектите по-подробно!