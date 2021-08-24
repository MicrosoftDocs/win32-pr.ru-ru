---
title: Перечисление Вмлогоффтипе (Впккоминтерфацес. h)
description: Указывает, как завершить работу виртуальной машины.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- Перечисление Вмлогоффтипе Virtual PC
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19d2b2785af4ffdedb2f2956658b678d16dd09c89132a230bab36feef30de30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136394"
---
# <a name="vmlogofftype-enumeration"></a>Перечисление Вмлогоффтипе

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает, как завершить работу виртуальной машины.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**Вмлогофф, \_ Обычная**
</dt> <dd>

Выход из системы гостевой виртуальной машины был нормальным.

</dd> <dt>

<span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**Вмлогофф \_ принудительно**
</dt> <dd>

На гостевой виртуальной машине был принудительно выполнен выход из системы.

</dd> <dt>

<span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**Вмлогофф \_ внешний**
</dt> <dd>

Выход из системы гостевой виртуальной машины выполнен с помощью метода [**ивмгуестос:: logoff**](ivmguestos-logoff.md) .

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

[**Ивмвиртуалмачине:: Шутдовнактиононкуит**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

