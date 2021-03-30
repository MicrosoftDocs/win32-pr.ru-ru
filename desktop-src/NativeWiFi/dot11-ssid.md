---
description: Содержит идентификатор SSID интерфейса.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: Структура DOT11_SSID (Влантипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910651"
---
# <a name="dot11_ssid-structure"></a>\_Структура SSID по идентификатору DOT11

Структура **\_ SSID DOT11** содержит идентификатор SSID интерфейса.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a>Члены

<dl> <dt>

**уссидленгс**
</dt> <dd>

Длина массива **укссид** в байтах.

</dd> <dt>

**укссид**
</dt> <dd>

Идентификатор SSID. \_Максимальная длина DOT11 SSID равна \_ \_ 32.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Идентификатор SSID, заданный членом **укссид** , не является строкой ASCII, завершающейся нулем. Длина идентификатора SSID определяется членом **уссидленгс** .

Подстановочный знак SSID — это идентификатор SSID, для элемента **уссидленгс** которого установлено значение 0. Если для нужного идентификатора SSID задан подстановочный знак SSID, станция 802,11 может подключаться к любой сети "базовый набор служб (BSS)".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                        |
| Распространяемые компоненты<br/>          | Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                                                         |
| Header<br/>                   | <dl> <dt>Влантипес. h (включение Windot11. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Параметры подключения \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**вланжетнетворкбсслист**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[**вланскан**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




