---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Вмсдкидл. h)
description: Переход ромба открывает новый образ в ромбе.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38731c93ae9ada520f286ae1662d45ec95d399d4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473500"
---
# <a name="wmt_videoimage_transition_diamond"></a>ВМТ \_ видеоимаже \_ Переход \_ ромб

Переход ромба открывает новый образ в ромбе.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.




| Параметр | Член структуры | Описание | 
|-----------|------------------|-------------|
| Центр по оси X | <strong>fEffectPara0</strong> | Координата по оси X относительно видеокадра центра ромба. | 
| Центр по оси Y | <strong>fEffectPara1</strong> | Координата по оси Y относительно видеокадра центра ромба. | 
| Ширина | <strong>fEffectPara2</strong> | Ширина ромба в пикселях. | 
| Высота | <strong>fEffectPara3</strong> | Высота ромба в пикселях. | 
| Композиция | <strong>fEffectPara4</strong> | Задайте одно из следующих значений:<ul><li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li><li>1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li></ul> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





