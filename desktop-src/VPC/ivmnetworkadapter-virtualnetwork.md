---
title: Свойство VirtualNetwork Ивмнетворкадаптер (Впккоминтерфацес. h)
description: Извлекает виртуальную сеть, к которой подключен сетевой интерфейс.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork свойство Virtual PC
- VirtualNetwork свойство Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, свойство VirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1bc3a3d58553d403f5e0ca6a8decbcbd3369b48450e9ec190b2f42f83de57e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136617"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a>Свойство Ивмнетворкадаптер:: VirtualNetwork

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает виртуальную сеть, к которой подключен сетевой интерфейс.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Значение свойства

Интерфейс [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) , представляющий виртуальную сеть, к которой подключен этот виртуальный сетевой интерфейс.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                                       | Значение                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                                          | Операция выполнена успешно.<br/>                                                  |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>                            | Параметр имеет **значение NULL**.<br/>                                                     |
| <dl> <dt>С \_ ЛОЖЬ</dt> <dt>1</dt> </dl>                                       | Этот сетевой интерфейс не подключен и не подключен к виртуальной сети.<br/> |
| <dl> <dt>Виртуальная машина \_ E \_ Недопустимый \_ \_ \_ идентификатор виртуальной сети</dt> <dt>0xA00400702</dt> </dl> | Этот интерфейс подключен к виртуальной сети с недопустимым ИДЕНТИФИКАТОРом.<br/>           |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl>                    | Произошла непредвиденная ошибка.<br/>                                              |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмнетворкадаптер**](ivmnetworkadapter.md)
</dt> </dl>

 

