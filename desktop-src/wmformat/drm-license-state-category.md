---
title: Перечисление DRM_LICENSE_STATE_CATEGORY (Дрмекстерналс. h)
description: '\_ \_ \_ Тип перечисления Категория состояния лицензии DRM определяет категории для строк лицензии DRM, которые отображаются для пользователя.'
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- Формат Windows Media DRM_LICENSE_STATE_CATEGORY перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40763ec7f610073784e3bd1516d4c955abcd65b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491835"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>Перечисление DRM_LICENSE_STATE_CATEGORY (Дрмекстерналс. h)

Тип **перечисления \_ \_ \_ Категория состояния лицензии DRM** определяет категории для строк [*лицензии*](wmformat-glossary.md) DRM, которые отображаются для пользователя.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum DRM_LICENSE_STATE_CATEGORY { 
  WM_DRM_LICENSE_STATE_NORIGHT                    = 0,
  WM_DRM_LICENSE_STATE_UNLIM,
  WM_DRM_LICENSE_STATE_COUNT,
  WM_DRM_LICENSE_STATE_FROM,
  WM_DRM_LICENSE_STATE_UNTIL,
  WM_DRM_LICENSE_STATE_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM,
  WM_DRM_LICENSE_STATE_COUNT_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**\_ \_ \_ неправильное состояние \_ лицензии WM DRM**
</dt> <dd>

Указывает, что строка примет форму "Воспроизведение запрещено".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_ \_ \_ УНЛИМ состояния лицензии WM \_ DRM**
</dt> <dd>

Указывает, что строка будет иметь форму "воспроизведение неограниченна".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM**
</dt> <dd>

Указывает, что строка примет форму "воспроизведение допустима 5 раз".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ из**
</dt> <dd>

Указывает, что строка примет форму "воспроизведение допустимого из 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ до**
</dt> <dd>

Указывает, что строка примет вид "допустимое воспроизведение до 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ с \_ до**
</dt> <dd>

Указывает, что строка примет форму "воспроизведение допустимого из 5/12 в 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM \_ из**
</dt> <dd>

Указывает, что строка примет форму «воспроизведение допустимого воспроизведения 5 раз с 5/12 по 9/12».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM \_ до**
</dt> <dd>

Указывает, что строка примет форму «воспроизведение допустимого воспроизведения 5 раз до 7/12/00».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ число состояний лицензий WM DRM \_ \_ \_ от \_ до**
</dt> <dd>

Указывает, что строка примет форму «воспроизведение допустимого воспроизведения 5 раз с 5/12 по 9/12».

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_ \_ срок действия лицензии WM DRM \_ \_ \_ после \_ фирстусе**
</dt> <dd>

Указывает, что строка примет форму "воспроизведение допустимого в течение 24 часов после первого использования".

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление указывает категорию для каждой возможной отображаемой выходной строки. Он является членом структуры [**данных о \_ \_ состоянии лицензии \_ DRM**](drm-license-state-data.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                      |
| Версия<br/>                  | Пакет SDK для Windows Media Format 7 или более поздние версии пакета SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Дрмекстерналс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





