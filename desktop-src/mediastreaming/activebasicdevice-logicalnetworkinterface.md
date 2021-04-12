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
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415384"
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

 

