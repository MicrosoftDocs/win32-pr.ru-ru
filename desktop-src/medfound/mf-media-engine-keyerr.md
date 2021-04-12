---
description: Определяет коды ошибок ключа носителя для механизма мультимедиа.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: Перечисление MF_MEDIA_ENGINE_KEYERR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351345"
---
# <a name="mf_media_engine_keyerr-enumeration"></a>\_ \_ Перечисление кэйерр для механизма передачи мультимедиа MF \_

Определяет коды ошибок ключа носителя для механизма мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ медиаенгине \_ кэйерр \_ неизвестный**
</dt> <dd>

Произошла неизвестная ошибка.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**\_клиент MF медиаенгине \_ кэйерр \_**
</dt> <dd>

Произошла ошибка клиента.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**\_Служба MF медиаенгине \_ кэйерр \_**
</dt> <dd>

Произошла ошибка службы.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**\_ \_ выходные данные MF медиаенгине кэйерр \_**
</dt> <dd>

Произошла ошибка в выходных данных.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ медиаенгине \_ кэйерр \_ хардваречанже** 
</dt> <dd>

Произошла ошибка, связанная с изменением оборудования.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**\_медиаенгине \_ кэйерр, \_ домен**
</dt> <dd>

Произошла ошибка в домене.

</dd> </dl>

## <a name="remarks"></a>Комментарии

**MF \_ MEDIA \_ Engine \_ кэйерр** используется с параметром *Code* [**имфмедиакэйсессионнотифи:: кэйеррор**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) и значением *Code* , возвращенным методом [**имфмедиакэйсессион::-Error**](imfmediakeysession-geterror.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




