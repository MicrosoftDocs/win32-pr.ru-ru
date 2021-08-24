---
description: Определяет тип сети "базовый набор служб (BSS)".
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: Перечисление DOT11_BSS_TYPE (Влантипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 2d1c83ced842dbb876fea89271a160df2ca07fb9f02f415b13f8f1a46bc8dc79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780324"
---
# <a name="dot11_bss_type-enumeration"></a>\_ \_ Перечисление типов BSS DOT11

Тип **перечисления \_ DOT11 \_ BSS** определяет тип сети "базовый набор служб (BSS)".

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**\_ \_ инфраструктура типов Dot11 \_ BSS**
</dt> <dd>

Указывает сеть BSS инфраструктуры.

</dd> <dt>

<span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**\_тип Dot11 BSS не \_ \_ зависит**
</dt> <dd>

Указывает независимую сеть BSS (ИБСС).

</dd> <dt>

<span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**\_тип Dot11 \_ BSS \_ ANY**
</dt> <dd>

Указывает либо инфраструктуру, либо ИБСС сеть.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                        |
| Распространяемые компоненты<br/>          | API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                                                         |
| Заголовок<br/>                   | <dl> <dt>Влантипес. h (включение Windot11. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_запись сети BSS \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[**\_Параметры подключения \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**вланжетнетворкбсслист**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




