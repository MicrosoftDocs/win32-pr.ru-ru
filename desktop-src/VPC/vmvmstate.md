---
title: Перечисление Вмвмстате (Впккоминтерфацес. h)
description: Указывает состояние виртуальной машины.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- Перечисление Вмвмстате Virtual PC
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691917"
---
# <a name="vmvmstate-enumeration"></a>Перечисление Вмвмстате

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает состояние виртуальной машины.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**Вмвмстате является \_ недопустимым**
</dt> <dd>

Недопустимое состояние (не должно выполняться, если виртуальная машина существует).

</dd> <dt>

<span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**Вмвмстате \_ турнедофф**
</dt> <dd>

Отключено и не сохраняется.

</dd> <dt>

<span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**Вмвмстате \_ сохранен**
</dt> <dd>

Отключено, но гостевой компьютер сохраняется.

</dd> <dt>

<span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**Вмвмстате \_ турнингон**
</dt> <dd>

В процессе включения.

</dd> <dt>

<span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**Вмвмстате \_ восстановление**
</dt> <dd>

Восстановление состояния.

</dd> <dt>

<span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**Вмвмстате \_ работает**
</dt> <dd>

Работа и не приостановлена.

</dd> <dt>

<span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**Вмвмстате \_ приостановлена**
</dt> <dd>

Запуск и приостановка.

</dd> <dt>

<span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**Вмвмстате \_ Сохранение**
</dt> <dd>

Сохранение состояния.

</dd> <dt>

<span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**Вмвмстате \_ турнингофф**
</dt> <dd>

В процессе отключения.

</dd> <dt>

<span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**Вмвмстате \_ мергингдривес**
</dt> <dd>

В процессе объединения дисков отмены.

</dd> <dt>

<span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**Вмвмстате \_ делетемачине**
</dt> <dd>

Идет Удаление виртуальной машины.

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

[**Ивмвиртуалмачине:: State**](ivmvirtualmachine-state.md)
</dt> <dt>

[**Ивмвиртуалмачинивентс:: Онстатечанже**](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[**Ивмвиртуалпцевентс:: Онвмстатечанже**](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

