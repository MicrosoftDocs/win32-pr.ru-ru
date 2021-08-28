---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Вмсдкидл. h)
description: Переход на страницу преобразует старое изображение с помощью отражения страницы и раскрывает новый рисунок под ним.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfa69988f5b5414eac3e27b3371bca0e0a28810
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474980"
---
# <a name="wmt_videoimage_transition_page_roll"></a>ВМТ \_ видеоимаже \_ Переход \_ на \_ пробную страницу

Переход на страницу преобразует старое изображение с помощью отражения страницы и раскрывает новый рисунок под ним.

## <a name="parameters"></a>Параметры

В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.




| Параметр | Член структуры | Описание | 
|-----------|------------------|-------------|
| Радиус. | <strong>fEffectPara0</strong> | Радиус рулона на странице. | 
| Расстояние | <strong>fEffectPara1</strong> | Объем нового изображения, отображаемого в пикселях в виде постраничного развертывания. | 
| Направление | <strong>fEffectPara2</strong> | Угол или сторона видеокадра, из которого поступает страница. Задайте одно из следующих значений:<br /><ul><li>0 слева</li><li>1-правая сторона</li><li>2 — снизу</li><li>3 — сверху</li><li>4. левый нижний угол</li><li>5-нижний правый угол</li><li>6-верхний левый угол</li><li>7-верхний правый угол</li></ul> | 
| Композиция | <strong>fEffectPara3</strong> | Задайте одно из следующих значений:<ul><li>0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</li><li>1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</li></ul> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмсдкидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Переходы по изображениям видео**](video-image-transitions.md)
</dt> </dl>

 

 





