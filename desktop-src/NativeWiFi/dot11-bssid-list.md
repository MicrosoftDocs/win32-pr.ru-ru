---
description: Содержит список идентификаторов "базовый набор служб (BSS)".
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: Структура DOT11_BSSID_LIST (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 8abcd2e711d5598c59bb8d4b7aed0f291364f94d04ec17a5fc80de2fd32939eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801394"
---
# <a name="dot11_bssid_list-structure"></a>\_ \_ Структура списка BSSID DOT11

Структура **\_ \_ списка BSSID для DOT11** содержит список основных идентификаторов набора служб (BSS).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a>Члены

<dl> <dt>

**Header**
</dt> <dd>

Структура [**\_ \_ заголовка объекта NDIS**](ndis-object-header.md) , содержащая сведения о типе, версии и размере структуры NDIS. Для большинства **структур \_ \_ списка BSSID DOT11** установите для элемента **типа** значение **\_ \_ \_ по умолчанию тип объекта NDIS**, установите для элемента **Revision** значение **DOT11, \_ \_ \_ редакция \_ 1**, и задайте для элемента **size** значение **sizeof ( \_ список DOT11 BSSID \_ )**.

</dd> <dt>

**унумофентриес**
</dt> <dd>

Число записей в этой структуре.

</dd> <dt>

**утоталнумофентриес**
</dt> <dd>

Общее число поддерживаемых записей.

</dd> <dt>

**бссидс**
</dt> <dd>

Список идентификаторов BSS. Идентификатор BSS хранится в виде типа [**\_ Mac- \_ адреса DOT11**](dot11-mac-address-type.md) .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                       |
| Распространяемые компоненты<br/>          | API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                                                        |
| Заголовок<br/>                   | <dl> <dt>Windot11. h (включение Windot11. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Параметры подключения \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




