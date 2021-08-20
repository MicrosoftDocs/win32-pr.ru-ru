---
title: Свойство Исвидеосуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживает ли устройство видео.
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- API потоковой передачи мультимедиа свойства Исвидеосуппортед
- API потоковой передачи мультимедиа свойства Исвидеосуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Исвидеосуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bb115aad422546746a44824c847bd0ae80c188264e8539e569a26e16eefa93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972523"
---
# <a name="activebasicdeviceisvideosupported-property"></a>Свойство Активебасикдевице:: Исвидеосуппортед

Возвращает значение, указывающее, поддерживает ли устройство видео.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Значение свойства

Указатель на **логическое значение** , указывающее, поддерживает ли устройство видео.

**значение true** , если устройство поддерживает видео; в противном случае — **значение false**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Плайтодевице. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Плайтодевице. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

