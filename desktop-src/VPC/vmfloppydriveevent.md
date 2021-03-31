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
ms.openlocfilehash: a11b1485f91264713cf96a4f95cab8286261eea4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803460"
---
# <a name="vmfloppydriveevent-enumeration"></a>Перечисление Вмфлоппидрививент

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмфлоппидрививентс**](ivmfloppydriveevents.md)
</dt> </dl>

 

