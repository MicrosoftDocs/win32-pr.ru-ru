---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Вмсдкидл. h)
description: Диагональный переход показывает новый рисунок вдоль диагональной линии, порожденной в одном углу рамки.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea028777580f7414a834a0aa3e73e18db607eccd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471990"
---
# <a name="wmt_videoimage_transition_diagonal"></a>ВМТ \_ видеоимаже \_ Переход по \_ диагонали

Диагональный переход показывает новый рисунок вдоль диагональной линии, порожденной в одном углу рамки.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.




| Параметр | Член структуры | Описание | 
|-----------|------------------|-------------|
| Ширина | <strong>fEffectPara0</strong> | Ширина диагональной секции в пикселях. | 
| Высота | <strong>fEffectPara1</strong> | Высота диагональной секции в пикселях. | 
| Направление | <strong>fEffectPara2</strong> | Определяет угол, с которого исходит переход. Задайте один из следующих элементов:<br /><ul><li>0-верхний правый</li><li>1-верхний левый</li><li>2-вниз справа</li><li>3-вниз слева</li></ul> | 
| Композиция | <strong>fEffectPara3</strong> | Задайте одно из следующих значений:<ul><li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li><li>1 — задает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li></ul> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





