---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Вмсдкидл. h)
description: Переход прямоугольника показывает новое изображение в прямоугольнике внутри фрейма.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8721455c09a263d9c856358d2ca55bb818ac48e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467401"
---
# <a name="wmt_videoimage_transition_rectangle"></a>\_ \_ прямоугольник перехода ВМТ \_ видеоимаже

Переход прямоугольника показывает новое изображение в прямоугольнике внутри фрейма.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.




| Параметр | Член структуры | Описание | 
|-----------|------------------|-------------|
| Центр по оси X | <strong>fEffectPara0</strong> | Координата по оси X относительно видеокадра центра прямоугольника. | 
| Центр по оси Y | <strong>fEffectPara1</strong> | Координата по оси Y относительно видеокадра центра прямоугольника. | 
| Ширина | <strong>fEffectPara2</strong> | Ширина прямоугольника в пикселях. | 
| Высота | <strong>fEffectPara3</strong> | Высота прямоугольника в пикселях. | 
| Композиция | <strong>fEffectPara4</strong> | Задайте одно из следующих значений:<ul><li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li><li>1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li></ul> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





