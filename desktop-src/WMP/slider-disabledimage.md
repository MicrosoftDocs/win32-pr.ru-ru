---
title: ПОЛЗУНок. Дисабледимаже
description: Атрибут Дисабледимаже указывает или получает изображение ползунка, используемого при отключенном элементе управления "ползунок".
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- проигрыватель Windows Media SLIDER. дисабледимаже
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 596afbed41fa1a864d8ed4e5fd217cb4856a716623ad2a60db080b3e965ab48d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123074"
---
# <a name="sliderdisabledimage"></a>ПОЛЗУНок. Дисабледимаже

Атрибут **дисабледимаже** указывает или получает изображение ползунка, используемого при отключенном элементе управления "ползунок".

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.

## <a name="remarks"></a>Remarks

**Дисабледимаже** является необязательным. Если он не указан, **фоновый** режим используется для всех отключенных состояний. Если элемент управления "ползунок" отключен, изображение переднего плана не отображается.

Поддерживаются форматы BMP, JPG, PNG и GIF (не включая анимированные GIF).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> <dt>

[**ПОЛЗУНок. backgroundImage**](slider-backgroundimage.md)
</dt> </dl>

 

 





