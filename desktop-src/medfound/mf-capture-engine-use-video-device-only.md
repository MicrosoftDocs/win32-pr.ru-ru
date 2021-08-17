---
description: Указывает, будет ли подсистема захвата записывать видео, но не аудио.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: Атрибут MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd8dd903c4c56b52bf82a97b28edd5148e3c091788376f1ef460047b7f609b51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973973"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>\_Запись MF \_ Engine \_ использовать \_ \_ атрибут " \_ только видео устройства"

Указывает, будет ли подсистема захвата записывать видео, но не аудио.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Если этот атрибут имеет **значение true**, подсистема захвата не выбирает или не использует устройство аудиозаписи. Присвойте этому атрибуту **значение true** , если хотите записывать видео без звука. Значение по умолчанию — **FALSE**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                         |
| Заголовок<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




