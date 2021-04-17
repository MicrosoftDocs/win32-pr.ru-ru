---
title: Перечисление Вмшутдовнактион (Впккоминтерфацес. h)
description: Указывает, как завершить работу виртуальной машины при завершении работы узла или завершении процесса vpc.exe.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- Перечисление Вмшутдовнактион Virtual PC
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691832"
---
# <a name="vmshutdownaction-enumeration"></a>Перечисление Вмшутдовнактион

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает, как завершить работу виртуальной машины (ВМ) при завершении работы узла или завершении процесса vpc.exe.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**Вмшутдовнактион \_ сохранить**
</dt> <dd>

Сохраните состояние виртуальной машины.

</dd> <dt>

<span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**Вмшутдовнактион \_ турнофф**
</dt> <dd>

Выключите виртуальную машину без отмены дисков.

</dd> <dt>

<span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**Вмшутдовнактион \_ Завершение работы**
</dt> <dd>

Завершите работу гостевой операционной системы на виртуальной машине, не отменяя диски, если компоненты интеграции доступны и в противном случае сохранит виртуальную машину.

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

[Перечисления Windows Virtual PC](virtual-pc-enumerations.md)
</dt> <dt>

[**Ивмвиртуалмачине:: Шутдовнактиононкуит**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

