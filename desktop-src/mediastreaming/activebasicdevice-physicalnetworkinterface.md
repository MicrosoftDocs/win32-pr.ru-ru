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
ms.openlocfilehash: 5bd9eb004607d93b92d502d22b253258bf39e501969e6b3952a58b0a03a1eec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736210"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Плайтодевице. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Плайтодевице. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

