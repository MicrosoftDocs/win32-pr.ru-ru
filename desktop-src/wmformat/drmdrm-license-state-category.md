---
title: Перечисление DRM_LICENSE_STATE_CATEGORY (Вмдрмсдк. h)
description: '\_ \_ \_ Тип перечисления Категория состояния лицензии DRM определяет тип ограничения лицензии, описываемого \_ \_ \_ структурой данных состояния лицензии DRM.'
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- Формат Windows Media DRM_LICENSE_STATE_CATEGORY перечисления
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b8724526142236b70faade68bf7d3ca358eb3f3810cae73f58adde17f25a0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591574"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>Перечисление DRM_LICENSE_STATE_CATEGORY (Вмдрмсдк. h)

Тип **перечисления \_ \_ \_ Категория состояния лицензии DRM** определяет тип ограничения лицензии, описываемого структурой [**\_ \_ \_ данных состояния лицензии DRM**](drmdrm-license-state-data.md) .

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
} DRM_LICENSE_STATE_CATEGORY;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**\_ \_ \_ неправильное состояние \_ лицензии WM DRM**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , запрещено.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_ \_ \_ УНЛИМ состояния лицензии WM \_ DRM**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено без ограничений.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено, но только заданное число раз.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ из**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено после даты установки.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ до**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено до даты установки.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ с \_ до**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено между двумя датами набора.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM \_ из**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено, но только заданное число раз после даты установки.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM \_ до**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено, но только заданное число раз до даты установки.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ число состояний лицензий WM DRM \_ \_ \_ от \_ до**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено, но только заданное число раз между двумя датами набора.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_ \_ срок действия лицензии WM DRM \_ \_ \_ после \_ фирстусе**
</dt> <dd>

Указывает, что действие, для которого были получены **\_ \_ \_ данные о состоянии лицензии DRM** , разрешено в течение заданного интервала времени, начиная с первого использования действия.

</dd> </dl>

## <a name="remarks"></a>Remarks

Отсутствует.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Типы перечислений**](drm-enumeration-types.md)
</dt> </dl>

 

 





