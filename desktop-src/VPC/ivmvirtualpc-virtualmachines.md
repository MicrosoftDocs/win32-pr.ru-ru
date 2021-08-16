---
title: Свойство VirtualMachines Ивмвиртуалпк (Впккоминтерфацес. h)
description: Извлекает перечисляемую коллекцию виртуальных машин.
ms.assetid: 9e8dcd65-7cf8-4cdd-a412-62cbb96eb8ec
keywords:
- VirtualMachines свойство Virtual PC
- VirtualMachines свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство VirtualMachines
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualMachines
- IVMVirtualPC.get_VirtualMachines
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346b4c2235ebef41e6361828dcba8d53f2246211b2dd569b6e91cb724631b227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998494"
---
# <a name="ivmvirtualpcvirtualmachines-property"></a>Свойство Ивмвиртуалпк:: VirtualMachines

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает перечисляемую коллекцию виртуальных машин.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_VirtualMachines(
  [out, retval] IVMVirtualMachineCollection **virtualMachineCollection
);
```



## <a name="property-value"></a>Значение свойства

Коллекция объектов [**ивмвиртуалмачине**](ivmvirtualmachine.md) . См. [**ивмвиртуалмачинеколлектион**](ivmvirtualmachinecollection.md).

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                                           | Значение                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                                              | Операция выполнена успешно.<br/>                                                        |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>                                | Параметр имеет **значение NULL**.<br/>                                                           |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl>                        | Произошла непредвиденная ошибка.<br/>                                                    |
| <dl> <dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt> </dl> | Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалпк**](ivmvirtualpc.md)
</dt> </dl>

 

