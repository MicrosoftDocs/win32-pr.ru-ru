---
description: Определяет алгоритм шифра для шифрования и расшифровки данных.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: Перечисление DOT11_CIPHER_ALGORITHM (Влантипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: c99ef5b648c5503743de6f51ce7d035d75dbe1f3e5593d473a374813f4000566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780244"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>\_ \_ Перечисление алгоритма шифрования DOT11

Перечисляемый тип **\_ \_ алгоритма шифра DOT11** определяет алгоритм шифра для шифрования и расшифровки данных.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**\_Algo шифра DOT11 \_ \_ нет**
</dt> <dd>

Указывает, что алгоритм шифра не включен или не поддерживается.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**\_Algo шифра DOT11 \_ \_ WEP40**
</dt> <dd>

Задает алгоритм, основанный на протоколе WEP, который является алгоритмом на основе RC4, указанным в стандарте 802.11-1999. Этот перечислитель задает алгоритм шифра WEP с 40-битным ключом шифрования.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_Шифрование DOT11 \_ Algo \_ TKIP**
</dt> <dd>

Указывает алгоритм TKIP, который является комплектом шифров на основе RC4, основанным на алгоритмах, определенных в спецификации WPA и стандарте IEEE 802.11 i-2004 Standard. Этот шифр также использует алгоритм MIC (код целостности сообщений) для защиты от подделки.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**\_Шифрование DOT11 \_ Algo \_ CCMP**
</dt> <dd>

Указывает алгоритм AES-CCMP, как указано в стандарте IEEE 802.11 i-2004 Standard и RFC 3610. AES (AES) — алгоритм шифрования, определенный в FIPS PUB 197.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**\_Algo шифра DOT11 \_ \_ WEP104**
</dt> <dd>

Задает алгоритм шифра WEP с 104-битным ключом шифрования.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**\_Группа шифрования DOT11 \_ Algo \_ WPA \_ USE \_**
</dt> <dd>

Указывает Wi-Fi защищенный доступ (WPA) использование набора шифров группового ключа. Дополнительные сведения об использовании набора шифров групповых ключей см. в предложении 7.3.2.25.1 стандарта IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**\_Группа шифрования DOT11 \_ Algo \_ RSN \_ USE \_**
</dt> <dd>

Указывает надежную сеть безопасности (RSN) использовать набор шифров группового ключа. Дополнительные сведения об использовании набора шифров групповых ключей см. в предложении 7.3.2.25.1 стандарта IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**\_Шифрование DOT11 \_ Algo \_ WEP**
</dt> <dd>

Задает алгоритм шифра WEP с ключом шифра любой длины.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**\_ \_ \_ Запуск Algo IHV \_ для шифра DOT11**
</dt> <dd>

Указывает начало диапазона, используемого для определения собственных алгоритмов шифра, разработанных независимым поставщиком оборудования (IHV).

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**\_ \_ \_ Окончание IHV Algo для шифра DOT11 \_**
</dt> <dd>

Задает конец диапазона, который используется для определения собственных алгоритмов шифра, разработанных независимо от поставщика оборудования.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                        |
| Распространяемые компоненты<br/>          | API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                                                         |
| Заголовок<br/>                   | <dl> <dt>Влантипес. h (включение Windot11. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ Пара шифров для проверки подлинности DOT11 \_**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**\_доступная \_ сеть WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**\_атрибуты безопасности \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




