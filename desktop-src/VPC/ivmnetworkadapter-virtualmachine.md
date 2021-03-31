---
title: Свойство VirtualMachine Ивмнетворкадаптер (Впккоминтерфацес. h)
description: Извлекает виртуальную машину, связанную с этим сетевым интерфейсом.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- VirtualMachine свойство Virtual PC
- VirtualMachine свойство Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, свойство VirtualMachine
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071063"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a>Свойство Ивмнетворкадаптер:: VirtualMachine

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает виртуальную машину, связанную с этим сетевым интерфейсом.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a>Значение свойства

Интерфейс [**ивмвиртуалмачине**](ivmvirtualmachine.md) , представляющий виртуальную машину.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>        |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>           |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Не удается найти виртуальную машину.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>    |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмнетворкадаптер**](ivmnetworkadapter.md)
</dt> </dl>

 

