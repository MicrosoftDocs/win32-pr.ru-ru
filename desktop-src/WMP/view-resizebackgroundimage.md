---
title: VIEW. Ресизебаккграундимаже
description: Атрибут Ресизебаккграундимаже указывает или получает значение, указывающее, можно ли изменить размер фонового изображения.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- Просмотреть. Ресизебаккграундимаже проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105714088"
---
# <a name="viewresizebackgroundimage"></a>VIEW. Ресизебаккграундимаже

Атрибут **ресизебаккграундимаже** указывает или получает значение, указывающее, можно ли изменить размер фонового изображения.

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **логическим значением** для чтения и записи.



| Значения | Описание                                      |
|--------|--------------------------------------------------|
| true   | Размер фонового изображения можно изменить.             |
| false  | По умолчанию. Размер фонового изображения не может быть изменен. |



 

## <a name="remarks"></a>Комментарии

Если задать для этого атрибута значение true, размер фонового изображения изменится в соответствии с текущими значениями атрибутов **Width** и **Height** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**VIEW, элемент**](view-element.md)
</dt> <dt>

[**Просмотр. backgroundImage**](view-backgroundimage.md)
</dt> </dl>

 

 





