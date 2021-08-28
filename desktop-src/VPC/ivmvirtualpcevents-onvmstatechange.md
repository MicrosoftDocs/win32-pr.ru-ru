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
ms.openlocfilehash: f63516e80ce4f3b830229fdb4cd574e95378c0569a4855a73c1c528af2ec8b48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032984"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>Метод Ивмвиртуалпцевентс:: Онвмстатечанже

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

## <a name="remarks"></a>Remarks

Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о событии **вмвиртуалпцевент \_ вмстатечанжед** , исходящем от [**ивмвиртуалпк**](ivmvirtualpc.md). Чтобы отслеживать определенную виртуальную машину, используйте метод [**ивмвиртуалмачинивентс:: онстатечанже**](ivmvirtualmachineevents-onstatechange.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмвиртуалпцевентс определяется как efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмвиртуалпцевентс**](ivmvirtualpcevents.md)
</dt> </dl>

 

