---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Вмсдкидл. h)
description: При заполнении V новый рисунок отображается в треугольнике, который начинается с одной стороны рамки.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbf032700959dd21a560b879357de2800ac657b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466161"
---
# <a name="wmt_videoimage_transition_filled_v"></a>ВМТ \_ видеоимаже \_ Переход \_ заполнен \_ V

При заполнении V новый рисунок отображается в треугольнике, который начинается с одной стороны рамки.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.




| Параметр | Член структуры | Описание | 
|-----------|------------------|-------------|
| Ширина | <strong>fEffectPara0</strong> | Ширина заполненной V в пикселях. | 
| Высота | <strong>fEffectPara1</strong> | Высота заполненной V в пикселях. | 
| Направление | <strong>fEffectPara2</strong> | Направление, с которого происходит заполнение V. Задайте одно из следующих значений:<br /><ul><li>0 — переход с левой стороны рамки.</li><li>1 — переход с правой стороны рамки.</li><li>2 — переходит от нижней части рамки.</li><li>3 — переходит от верхней части рамки.</li></ul> | 
| Композиция | <strong>fEffectPara3</strong> | Задайте одно из следующих значений:<ul><li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li><li>1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li></ul> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





