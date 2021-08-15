---
title: Свойство Логикалнетворкинтерфаце Активебасикдевице (Плайтодевице. h)
description: Возвращает идентификатор логического сетевого интерфейса.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- API потоковой передачи мультимедиа свойства Логикалнетворкинтерфаце
- API потоковой передачи мультимедиа свойства Логикалнетворкинтерфаце, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Логикалнетворкинтерфаце
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ee3e2b23a43e29daf2438cee517220f895ad601607dbdc6a61497f8ef1afa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736390"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a>Свойство Активебасикдевице:: Логикалнетворкинтерфаце

Возвращает идентификатор логического сетевого интерфейса.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Значение свойства

Указатель на **идентификатор GUID** , указывающий идентификатор логического сетевого интерфейса.

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

 

