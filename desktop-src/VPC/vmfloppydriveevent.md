---
title: Перечисление Вмфлоппидрививент (Впккоминтерфацес. h)
description: Указывает события дисковода гибких дисков.
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- Перечисление Вмфлоппидрививент Virtual PC
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f8ded5cf87d740f113bab54d9f7587c8f8927e5ae37352dceb4a30be09d104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767904"
---
# <a name="vmfloppydriveevent-enumeration"></a>Перечисление Вмфлоппидрививент

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает события дисковода гибких дисков.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**Вмфлоппидрививент \_ INSERT**
</dt> <dd>

Прикрепленный образ дискеты или реальный носитель вставлен в диск узла.

</dd> <dt>

<span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**Вмфлоппидрививент \_**
</dt> <dd>

Носитель был извлечен.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмфлоппидрививентс**](ivmfloppydriveevents.md)
</dt> </dl>

 

