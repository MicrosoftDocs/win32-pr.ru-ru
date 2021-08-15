---
title: ЕКУАЛИЗЕРСЕТТИНГС. Спеакерсизе
description: Атрибут Спеакерсизе указывает или получает номер индекса текущего размера динамика.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- екуализерсеттингс. спеакерсизе проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d289a89a22e8c10cf669e9b55fc304826acb3ce0f72468f725e7d5fae0dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748652"
---
# <a name="equalizersettingsspeakersize"></a>ЕКУАЛИЗЕРСЕТТИНГС. Спеакерсизе

Атрибут **спеакерсизе** указывает или получает номер индекса текущего размера динамика.

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (длинное), содержащим одно из следующих значений.



| Значение | Описание                              |
|-------|------------------------------------------|
| 0     | Текущие динамики — наушники.     |
| 1     | Текущие динамики имеют нормальный размер. |
| 2     | Текущие динамики имеют большой размер.          |



 

## <a name="remarks"></a>Remarks

Понятное имя размера динамика можно получить с помощью атрибута **куррентспеакернаме** .

Этот атрибут пропускается, если **енханцедаудио** имеет значение false.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Куррентспеакернаме**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Енханцедаудио**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





