---
title: Перечисление Вмендпоинттипе (Впккоминтерфацес. h)
description: Указывает тип конечной точки.
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- Перечисление Вмендпоинттипе Virtual PC
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912eb43147af03dd2b9923c4bdb778044f40d023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891861"
---
# <a name="vmendpointtype-enumeration"></a>Перечисление Вмендпоинттипе

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает тип конечной точки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**Вмендпоинт \_ помощью канала NamedPipe**
</dt> <dd>

Сторона размещения.

</dd> <dt>

<span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**Вмендпоинт \_ tcpip**
</dt> <dd>

Сторона виртуальной машины.

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

[**Ивмвиртуалмачине:: Старткоммуникатиончаннел**](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

