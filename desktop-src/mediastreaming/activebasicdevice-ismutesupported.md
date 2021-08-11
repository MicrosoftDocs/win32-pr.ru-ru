---
title: Свойство Исмутесуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживает ли устройство отключение звука.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- API потоковой передачи мультимедиа свойства Исмутесуппортед
- API потоковой передачи мультимедиа свойства Исмутесуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Исмутесуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fad8352504a6c950bb76206f05c77c5baa9f3baed2f1144a1d6c165e380a4b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236652"
---
# <a name="activebasicdeviceismutesupported-property"></a>Свойство Активебасикдевице:: Исмутесуппортед

Возвращает значение, указывающее, поддерживает ли устройство отключение звука.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Значение свойства

Указатель на **логическое значение** , указывающее, поддерживает ли устройство озвучивание звука.

**значение true** , если устройство поддерживает выключение звука; в противном случае — **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Плайтодевице. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Плайтодевице. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

