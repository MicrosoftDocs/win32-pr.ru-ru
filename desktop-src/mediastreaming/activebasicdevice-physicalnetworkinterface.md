---
title: Свойство Фисикалнетворкинтерфаце Активебасикдевице (Плайтодевице. h)
description: Возвращает идентификатор физического сетевого интерфейса.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- API потоковой передачи мультимедиа свойства Фисикалнетворкинтерфаце
- API потоковой передачи мультимедиа свойства Фисикалнетворкинтерфаце, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Фисикалнетворкинтерфаце
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491259"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a>Активебасикдевице: свойство Хисикалнетворкинтерфаце:P

Возвращает идентификатор физического сетевого интерфейса.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Значение свойства

Указатель на **идентификатор GUID** , указывающий идентификатор физического сетевого интерфейса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Плайтодевице. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Плайтодевице. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

