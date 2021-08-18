---
title: Метод Ивмвиртуалмачинивентс Онконфигуратиончанжед (Впккоминтерфацес. h)
description: Получает уведомление о том, что значение в конфигурации этой виртуальной машины изменилось.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Метод Онконфигуратиончанжед Virtual PC
- Метод Онконфигуратиончанжед Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онконфигуратиончанжед
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ca4d3b72d9cd2b06db2ca7b7b65e0c63795a4db0e52ccd9b76a62ff8b192e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056642"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a>Метод Ивмвиртуалмачинивентс:: Онконфигуратиончанжед

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает уведомление о том, что значение в конфигурации этой виртуальной машины изменилось.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*configKey* \[ окне\]
</dt> <dd>

Значение в изменяемой конфигурации.

</dd> <dt>

*конфигдата* \[ окне\]
</dt> <dd>

Новое значение для конфигурации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод вызывается при изменении конфигурации для этой виртуальной машины. Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии вмвиртуалмачинивент конфигуратиончанжед, исходящем от [**ивмвиртуалмачине**](ivmvirtualmachine.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачинивентс**](ivmvirtualmachineevents.md)
</dt> </dl>

 

