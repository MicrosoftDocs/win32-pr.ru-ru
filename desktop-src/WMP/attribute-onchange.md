---
title: attribute_onchange
description: Когда атрибут обложки изменяет значение, возникает событие, которое может быть обработано обработчиком событий. Имя обработчика событий — это имя атрибута, за которым следует символ подчеркивания и \ 0034; OnChange \ 0034;, например \ 0034; значение \_ onChange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange проигрыватель Windows Media
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698838"
---
# <a name="attribute_onchange"></a>атрибут \_ onChange

Когда атрибут обложки изменяет значение, возникает событие, которое может быть обработано обработчиком событий. Имя обработчика событий — это имя атрибута, за которым следует символ подчеркивания и "OnChange", например "значение \_ onChange".

``` syntax
        attribute_onchange
```

## <a name="examples"></a>Примеры


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 70 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Обработчики событий окружения**](ambient-event-handlers.md)
</dt> </dl>

 

 





