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
ms.openlocfilehash: df1f8b5bc21021e7771c14c0c3c6399e1d6342d7ebe3803759c8adb5c45024cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248414"
---
# <a name="vmshutdownaction-enumeration"></a>Перечисление Вмшутдовнактион

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Windows Перечисления виртуальных ПК](virtual-pc-enumerations.md)
</dt> <dt>

[**Ивмвиртуалмачине:: Шутдовнактиононкуит**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

