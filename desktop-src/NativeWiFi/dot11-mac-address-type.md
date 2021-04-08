---
description: Используются для определения MAC-адреса, используемого для управления доступом к носителю.
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910659"
---
# <a name="dot11_mac_address"></a>\_Mac- \_ адрес DOT11

Типы **\_ Mac- \_ адресов DOT11** используются для определения MAC-адреса стандарта IEEE.


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

**DOT11 \_ Mac- \_ адрес \[ 6\]**
</dt> <dd>

MAC-адрес в формате одноадресной рассылки, многоадресной рассылки или вещания.

</dd> <dt>

**PDOT11 \_ Mac- \_ адрес**
</dt> <dd>

Указатель на MAC-адрес в формате одноадресной рассылки, многоадресной рассылки или вещания.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                       |
| Распространяемые компоненты<br/>          | Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                                                        |
| Header<br/>                   | <dl> <dt>Windot11. h (включение Windot11. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DOT11 \_ BSSID, \_ список**](dot11-bssid-list.md)
</dt> <dt>

[**\_атрибуты связи \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**\_запись сети BSS \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




