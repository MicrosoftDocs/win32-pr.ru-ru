---
title: Перечисление Вмвиртуалпцевент (Впккоминтерфацес. h)
description: Указывает события виртуальных ПК Windows.
ms.assetid: 3b239cd0-d922-42de-8bcc-51f625c0d8b0
keywords:
- Перечисление Вмвиртуалпцевент Virtual PC
topic_type:
- apiref
api_name:
- VMVirtualPCEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de7ecb639d0b62165dec691d522bed8116670c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072012"
---
# <a name="vmvirtualpcevent-enumeration"></a>Перечисление Вмвиртуалпцевент

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает события виртуальных ПК Windows.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmVirtualPCEvent_VMStateChange  = 2,
  vmVirtualPCEvent_EventLogged    = 3
} VMVirtualPCEvent;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**Вмвиртуалпцевент \_ вмстатечанже**
</dt> <dd>

Состояние виртуальной машины изменилось.

</dd> <dt>

<span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**Вмвиртуалпцевент \_ евентлогжед**
</dt> <dd>

Виртуальный ПК зарегистрировал событие.

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

[**ивмвиртуалпцевентс**](ivmvirtualpcevents.md)
</dt> </dl>

 

