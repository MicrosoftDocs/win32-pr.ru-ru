---
title: Метод Ивмнетворкадаптер Детачфромвиртуалнетворк (Впккоминтерфацес. h)
description: Отключает сетевой интерфейс от своей виртуальной сети.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- Метод Детачфромвиртуалнетворк Virtual PC
- Метод Детачфромвиртуалнетворк Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, метод Детачфромвиртуалнетворк
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d5046844764fe9e9eb6552fe1a04b6140201b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415680"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a>Ивмнетворкадаптер: метод:D Етачфромвиртуалнетворк

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Отключает сетевой интерфейс от своей виртуальной сети.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Возвращаемый код и значение                                                                                                                                                 | Описание                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



 

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

 

