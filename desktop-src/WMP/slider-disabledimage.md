---
title: ПОЛЗУНок. Дисабледимаже
description: Атрибут Дисабледимаже указывает или получает изображение ползунка, используемого при отключенном элементе управления "ползунок".
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- ПОЛЗУНок. Дисабледимаже Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1b90dcbd551ca0f8bb332f858eac0b69c46733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657112"
---
# <a name="sliderdisabledimage"></a>ПОЛЗУНок. Дисабледимаже

Атрибут **дисабледимаже** указывает или получает изображение ползунка, используемого при отключенном элементе управления "ползунок".

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.

## <a name="remarks"></a>Комментарии

**Дисабледимаже** является необязательным. Если он не указан, **фоновый** режим используется для всех отключенных состояний. Если элемент управления "ползунок" отключен, изображение переднего плана не отображается.

Поддерживаются форматы BMP, JPG, PNG и GIF (не включая анимированные GIF).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> <dt>

[**ПОЛЗУНок. backgroundImage**](slider-backgroundimage.md)
</dt> </dl>

 

 





