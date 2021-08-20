---
title: Перечисление Вмвиртуалмачинивентс (Впккоминтерфацес. h)
description: Указывает события виртуальной машины.
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- Перечисление Вмвиртуалмачинивентс Virtual PC
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5079aee6752c260cd6bab9ee9022d22fd891eb6adf36ad0ec4d1c9987b6ff508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998344"
---
# <a name="vmvirtualmachineevents-enumeration"></a>Перечисление Вмвиртуалмачинивентс

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает события виртуальной машины.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**Вмвиртуалмачинивент \_ StateChanged**
</dt> <dd>

Состояние виртуальной машины изменилось.

</dd> <dt>

<span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**Вмвиртуалмачинивент \_ рекуестшутдовн**
</dt> <dd>

Запрошено завершение работы.

</dd> <dt>

<span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**\_Сброс вмвиртуалмачинивент**
</dt> <dd>

Виртуальная машина сброшена.

</dd> <dt>

<span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**Вмвиртуалмачинивент \_ триплефаулт**
</dt> <dd>

На виртуальной машине возникла тройная ошибка.

</dd> <dt>

<span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**Вмвиртуалмачинивент \_ хеартбеатстоппед**
</dt> <dd>

Пульс виртуальной машины остановлен. Обычно это означает, что произошел сбой гостевой операционной системы.

</dd> <dt>

<span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**Вмвиртуалмачинивент \_ конфигуратиончанжед**
</dt> <dd>

Значение в конфигурации для этой виртуальной машины изменилось

</dd> <dt>

<span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**Вмвиртуалмачинивент \_ енханцедвидеомодечанжед**
</dt> <dd>

Изменился режим видео виртуальной машины.

</dd> <dt>

<span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**Вмвиртуалмачинивент \_ аддитионсунинсталлед**
</dt> <dd>

Компоненты интеграции были удалены с виртуальной машины.

</dd> <dt>

<span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**Вмвиртуалмачинивент \_ аддитионсаваилабле**
</dt> <dd>

Интеграция доступна в гостевой операционной системе.

</dd> <dt>

<span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**Вмвиртуалмачинивент \_ гуестшутдовн**
</dt> <dd>

Работа гостевой операционной системы завершается.

</dd> <dt>

<span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**Вмвиртуалмачинивент \_ гуестлогофф**
</dt> <dd>

Пользователь вышел из операционной системы на виртуальной машине.

</dd> <dt>

<span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**Вмвиртуалмачинивент \_ дискаутофспаце**
</dt> <dd>

Недостаточно места на диске, требуемом для виртуальной машины.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачинивентс**](ivmvirtualmachineevents.md)
</dt> </dl>

 

