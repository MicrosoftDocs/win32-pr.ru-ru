---
title: ЕКУАЛИЗЕРСЕТТИНГС. Спеакерсизе
description: Атрибут Спеакерсизе указывает или получает номер индекса текущего размера динамика.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- Проигрыватель Windows Media ЕКУАЛИЗЕРСЕТТИНГС. Спеакерсизе
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694930"
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



 

## <a name="remarks"></a>Комментарии

Понятное имя размера динамика можно получить с помощью атрибута **куррентспеакернаме** .

Этот атрибут пропускается, если **енханцедаудио** имеет значение false.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Куррентспеакернаме**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Енханцедаудио**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





