---
title: Перечисление WMT_RIGHTS (Вмдрмсдк. h)
description: Определяет права, которые могут быть указаны в лицензии DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- Формат Windows Media WMT_RIGHTS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704047"
---
# <a name="wmt_rights-enumeration"></a>\_Перечисление прав ВМТ

Тип **перечисления \_ Rights ВМТ** определяет права, которые могут быть указаны в лицензии DRM.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**\_Воспроизведение ВМТ вправо \_**
</dt> <dd>

Указывает право на воспроизведение содержимого без ограничений.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**ВМТ \_ правую \_ копию \_ на \_ устройство, отличное от \_ SDMI \_**
</dt> <dd>

Указывает право на копирование содержимого на устройство, не соответствующее инициативе защиты цифровой музыки (SDMI).

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**ВМТ \_ правую \_ копию \_ на \_ компакт-диск**
</dt> <dd>

Указывает право на копирование содержимого на компакт-диск.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**\_Копировать ВМТ \_ вправо \_ на \_ \_ устройство SDMI**
</dt> <dd>

Указывает право на копирование содержимого на устройство, совместимое с SDMI.

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**ВМТ \_ прямо в \_ один \_ раз**
</dt> <dd>

Указывает право на воспроизведение содержимого только один раз.

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**ВМТ, \_ право на \_ Сохранение \_ \_ защищенного потока**
</dt> <dd>

Указывает право на сохранение содержимого с сервера.

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**ВМТ \_ правая \_ копия**
</dt> <dd>

Указывает право на копирование содержимого. Windows Media DRM 10 регулирует устройства, на которых можно скопировать содержимое, с помощью уровней защиты выходных данных (Оплс).

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**ВМТ в \_ прямом \_ сотрудничестве \_**
</dt> <dd>

Указывает право на воспроизведение содержимого в рамках интерактивного сценария, в котором несколько участников могут добавлять песни из коллекции в общий список воспроизведения.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**ВМТ \_ правый \_ SDMI \_**
</dt> <dd>

Зарезервировано для последующего использования. Не используйте.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**ВМТ \_ \_ SDMI \_ номорекопиес**
</dt> <dd>

Зарезервировано для последующего использования. Не используйте.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эти значения являются битовыми флагами, поэтому один или несколько можно задать, объединив их с оператором побитового **или** .

При использовании Windows Media DRM 10 **ВМТ \_ \_ Копировать \_ на устройство, \_ не \_ \_** использующее SDMI, **ВМТ \_ правую \_ копию \_ на SDMI- \_ \_ устройство**, а **ВМТ \_ право \_ Копировать \_ на \_ CD** заменяется **ВМТ \_ правой \_ копией**. Ограничения на устройства, на которые может копироваться содержимое, указываются с помощью уровней защиты выходных данных (Оплс).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Типы перечислений**](drm-enumeration-types.md)
</dt> </dl>

 

 





