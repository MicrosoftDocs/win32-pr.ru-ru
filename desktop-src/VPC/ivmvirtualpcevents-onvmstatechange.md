---
title: Метод Ивмвиртуалпцевентс Онвмстатечанже (Впккоминтерфацес. h)
description: Получает уведомление о том, что состояние виртуальной машины изменилось. | Метод Ивмвиртуалпцевентс Онвмстатечанже (Впккоминтерфацес. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Метод Онвмстатечанже Virtual PC
- Метод Онвмстатечанже Virtual PC, интерфейс Ивмвиртуалпцевентс
- Ивмвиртуалпцевентс интерфейс Virtual PC, метод Онвмстатечанже
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694007"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>Метод Ивмвиртуалпцевентс:: Онвмстатечанже

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает уведомление о том, что состояние виртуальной машины изменилось.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*виртуалмачинеконфиг* \[ окне\]
</dt> <dd>

Имя виртуальной машины.

</dd> <dt>

*виртуалмачинестате* \[ окне\]
</dt> <dd>

Новое состояние виртуальной машины.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о событии **вмвиртуалпцевент \_ вмстатечанжед** , исходящем от [**ивмвиртуалпк**](ivmvirtualpc.md). Чтобы отслеживать определенную виртуальную машину, используйте метод [**ивмвиртуалмачинивентс:: онстатечанже**](ivmvirtualmachineevents-onstatechange.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмвиртуалпцевентс определяется как efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалпцевентс**](ivmvirtualpcevents.md)
</dt> </dl>

 

