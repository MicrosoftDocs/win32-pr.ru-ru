---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Вмсдкидл. h)
description: Переход на слайд показывает новое изображение путем перемещения старого изображения из рамки.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9866706528cab038042adc8d098743ce6588c805
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476340"
---
# <a name="wmt_videoimage_transition_slide"></a>\_ \_ слайд перехода ВМТ \_ видеоимаже

Переход на слайд показывает новое изображение путем перемещения старого изображения из рамки.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.




| Параметр | Член структуры | Описание | 
|-----------|------------------|-------------|
| Расстояние | <strong>fEffectPara0</strong> | Расстояние (в пикселях), в котором старое изображение слайдов выходит за пределы рамки. | 
| Направление | <strong>fEffectPara1</strong> | Направление, в котором слайды старого изображения. Задайте одно из следующих значений:<br /><ul><li>0 — слайд справа.</li><li>1 — слайд слева.</li><li>2. Проведите вверх.</li><li>3. Проведите вниз.</li></ul> | 
| Композиция | <strong>fEffectPara2</strong> | Задайте одно из следующих значений:<ul><li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li><li>1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li></ul> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





