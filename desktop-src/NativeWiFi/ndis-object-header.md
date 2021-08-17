---
description: Упаковывает сведения о типе объекта, версии и размере, необходимые для многих структур NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: Структура NDIS_OBJECT_HEADER (Нтддндис. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: f9f4a4ef2a833081cde0c3c7ca4d395e59743944291a95d7680c241191988b35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065054"
---
# <a name="ndis_object_header-structure"></a>\_ \_ Структура заголовка объекта NDIS

Структура **\_ \_ заголовка объекта NDIS** упаковывает тип объекта, версию и сведения о размере, которые требуются во многих структурах NDIS 6,0.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**Тип**
</dt> <dd>

Указывает тип объекта NDIS, который описывает структура.

</dd> <dt>

**Редакции**
</dt> <dd>

Указывает номер редакции этой структуры.

</dd> <dt>

**Размер**
</dt> <dd>

Задает общий размер (в байтах) структуры NDIS, содержащей **\_ \_ заголовок объекта NDIS**. Этот размер включает в себя размер элемента **\_ \_ заголовка объекта NDIS** и всех остальных элементов структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                       |
| Распространяемые компоненты<br/>          | API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                                                        |
| Заголовок<br/>                   | <dl> <dt>Нтддндис. h (включение Windot11. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DOT11 \_ BSSID, \_ список**](dot11-bssid-list.md)
</dt> </dl>

 

 




