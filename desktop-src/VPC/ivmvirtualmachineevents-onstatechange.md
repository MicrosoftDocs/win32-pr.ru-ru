---
title: Метод Ивмвиртуалмачинивентс Онстатечанже (Впккоминтерфацес. h)
description: Получает уведомление о том, что состояние виртуальной машины изменилось. | Метод Ивмвиртуалмачинивентс Онстатечанже (Впккоминтерфацес. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- Метод Онстатечанже Virtual PC
- Метод Онстатечанже Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онстатечанже
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353822"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a>Метод Ивмвиртуалмачинивентс:: Онстатечанже

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает уведомление о том, что состояние виртуальной машины изменилось.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*виртуалмачинестате* \[ окне\]
</dt> <dd>

Новое состояние виртуальной машины. Список значений см. в разделе [**вмвмстате**](vmvmstate.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод вызывается при изменении состояния этой виртуальной машины. Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии вмвиртуалмачинивент StateChanged, исходящем от [**ивмвиртуалмачине**](ivmvirtualmachine.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачинивентс**](ivmvirtualmachineevents.md)
</dt> </dl>

 

