---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Вмсдкидл. h)
description: При переходе типа "звезда" новый образ отображается на пять звездочек внутри рамки.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7524e51908f7d941aa04b138cc67ba6c4ab6a2a8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479500"
---
# <a name="wmt_videoimage_transition_star"></a>ВМТ \_ видеоимаже \_ 1-2-3 \_

При переходе типа "звезда" новый образ отображается на пять звездочек внутри рамки.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.




| Параметр | Член структуры | Описание | 
|-----------|------------------|-------------|
| Центр по оси X | <strong>fEffectPara0</strong> | Координата по оси X относительно видеокадра центра звезды. | 
| Центр по оси Y | <strong>fEffectPara1</strong> | Координата по оси Y относительно видеокадра центра звезды. | 
| Радиус. | <strong>fEffectPara2</strong> | Радиус (в пикселях) круга, определяемый точками звезды. | 
| Композиция | <strong>fEffectPara3</strong> | Задайте одно из следующих значений:<ul><li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li><li>1 — задает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li></ul> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





