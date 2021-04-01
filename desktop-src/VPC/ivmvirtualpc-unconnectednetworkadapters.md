---
title: Свойство Унконнектеднетворкадаптерс Ивмвиртуалпк (Впккоминтерфацес. h)
description: Возвращает перечисляемую коллекцию неподключенных сетевых интерфейсов.
ms.assetid: 2d95f289-083a-4388-b842-0a11b4e1a06f
keywords:
- Унконнектеднетворкадаптерс свойство Virtual PC
- Унконнектеднетворкадаптерс свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Унконнектеднетворкадаптерс
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnconnectedNetworkAdapters
- IVMVirtualPC.get_UnconnectedNetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0694c6c5ce782e05ca322ba57f4ce7aaf5f708d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071750"
---
# <a name="ivmvirtualpcunconnectednetworkadapters-property"></a>Свойство Ивмвиртуалпк:: Унконнектеднетворкадаптерс

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает перечисляемую коллекцию неподключенных сетевых интерфейсов.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_UnconnectedNetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **unconnectedNetworkAdapterCollection
);
```



## <a name="property-value"></a>Значение свойства

Коллекция неподключенных объектов [**ивмнетворкадаптер**](ivmnetworkadapter.md) . См. [**ивмнетворкадаптерколлектион**](ivmnetworkadaptercollection.md).

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

 

