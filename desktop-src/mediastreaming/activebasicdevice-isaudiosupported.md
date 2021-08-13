---
title: Свойство Исаудиосуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживает ли устройство аудио.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- API потоковой передачи мультимедиа свойства Исаудиосуппортед
- API потоковой передачи мультимедиа свойства Исаудиосуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Исаудиосуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20125114b6cd134d153ad6425af5af410faf524714a2e505a37fbf57dcda21e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462431"
---
# <a name="activebasicdeviceisaudiosupported-property"></a>Свойство Активебасикдевице:: Исаудиосуппортед

Возвращает значение, указывающее, поддерживает ли устройство аудио.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Значение свойства

Указатель на **логическое значение** , указывающее, поддерживает ли устройство аудио.

**значение true** , если устройство поддерживает аудио; в противном случае — **значение false**.

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

 

