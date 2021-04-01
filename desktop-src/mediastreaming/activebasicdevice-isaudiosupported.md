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
ms.openlocfilehash: 66058da9dcdbac0ed1100b0ef21a4ed530d45a68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071999"
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

 

