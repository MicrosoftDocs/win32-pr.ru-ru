---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Вмсдкидл. h)
description: Переход от исчезания к цвету разрешается из изображения в кадр сплошного цвета.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694920"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a>ВМТ \_ видеоимаже \_ Переход \_ \_ к \_ цвету

Переход от исчезания к цвету разрешается из изображения в кадр сплошного цвета.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.



| Параметр         | Член структуры | Описание                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Красный               | **fEffectPara0** | Красное значение цвета фона. Задайте значение в диапазоне от 0 до 255.                                                                                                                                                     |
| Зеленый             | **fEffectPara1** | Зеленое значение цвета фона. Задайте значение в диапазоне от 0 до 255.                                                                                                                                                   |
| Синий              | **fEffectPara2** | Синее значение цвета фона. Задайте значение в диапазоне от 0 до 255.                                                                                                                                                    |
| Вес фона | **fEffectPara3** | Вес цвета фона. Этот параметр выражает процентный показатель цвета фона в наборе в виде десятичного значения. Например, для смешения цвета фона с 30%, установив для изображения 70% набора значение 0,30. |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





