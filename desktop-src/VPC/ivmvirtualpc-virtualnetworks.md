---
title: Свойство VirtualNetworks Ивмвиртуалпк (Впккоминтерфацес. h)
description: Извлекает перечисляемую коллекцию виртуальных сетей.
ms.assetid: 88c68178-0399-44cd-8145-1f2e4d6ac632
keywords:
- VirtualNetworks свойство Virtual PC
- VirtualNetworks свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство VirtualNetworks
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualNetworks
- IVMVirtualPC.get_VirtualNetworks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2ea97a7d9bb65bb41842ca028ded88f9a26b63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137670"
---
# <a name="ivmvirtualpcvirtualnetworks-property"></a>Свойство Ивмвиртуалпк:: VirtualNetworks

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает перечисляемую коллекцию виртуальных сетей.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_VirtualNetworks(
  [out, retval] IVMVirtualNetworkCollection **virtualNetworkCollection
);
```



## <a name="property-value"></a>Значение свойства

Коллекция объектов [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) . См. [**ивмвиртуалнетворкколлектион**](ivmvirtualnetworkcollection.md).

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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалпк**](ivmvirtualpc.md)
</dt> </dl>

 

