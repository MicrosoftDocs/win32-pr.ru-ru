---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Вмсдкидл. h)
description: Переход вставки показывает новый рисунок в прямоугольнике, который начинается с одного угла рамки.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47d53de99d3c6f6144755934989ca3958d28a23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476788"
---
# <a name="wmt_videoimage_transition_inset"></a>ВМТ \_ видеоимаже \_ перехода \_

Переход вставки показывает новый рисунок в прямоугольнике, который начинается с одного угла рамки.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.




| Параметр | Член структуры | Описание | 
|-----------|------------------|-------------|
| Ширина | <strong>fEffectPara0</strong> | Ширина отступа в пикселях. | 
| Высота | <strong>fEffectPara1</strong> | Высота отступа в пикселях. | 
| Направление | <strong>fEffectPara2</strong> | Угол, с которого начинается вставка. Задайте одно из следующих значений:<br /><ul><li>0-вниз слева</li><li>1 — нижний правый</li><li>2-верхний левый</li><li>3 — верхний правый</li></ul> | 
| Композиция | <strong>fEffectPara3</strong> | Задайте одно из следующих значений:<ul><li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li><li>1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li></ul> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





