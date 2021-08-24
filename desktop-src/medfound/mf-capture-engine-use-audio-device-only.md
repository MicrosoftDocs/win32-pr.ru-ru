---
description: Указывает, захватывает ли подсистема захвата аудио, но не видео.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: Атрибут MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c248923ae2dce7d5153f8e88cb8eef88d29ea3dbf6ce5c94e4a8ee355af16c42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013354"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>\_Система записи \_ MF \_ использует \_ атрибут "только звуковое \_ устройство \_ "

Указывает, захватывает ли подсистема захвата аудио, но не видео.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Если этот атрибут имеет **значение true**, подсистема захвата не выбирает или не использует устройство видеозаписи. Присвойте этому атрибуту **значение true** , если хотите записывать звук без видео. Значение по умолчанию — **FALSE**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                         |
| Заголовок<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




