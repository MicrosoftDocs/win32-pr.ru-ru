---
title: Свойство Исимажесуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживает ли устройство изображения.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- API потоковой передачи мультимедиа свойства Исимажесуппортед
- API потоковой передачи мультимедиа свойства Исимажесуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Исимажесуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a147c5156f07c6cc6461cafcf8dc778013a7eb3048d1428f854b844d24f5642a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236715"
---
# <a name="activebasicdeviceisimagesupported-property"></a>Свойство Активебасикдевице:: Исимажесуппортед

Возвращает значение, указывающее, поддерживает ли устройство изображения.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Значение свойства

Указатель на **логическое значение** , указывающее, поддерживает ли устройство изображения.

**значение true** , если устройство поддерживает образы; в противном случае — **значение false**.

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

 

