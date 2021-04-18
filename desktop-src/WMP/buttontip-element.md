---
title: Буттонтип, элемент
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Буттонтип, элемент
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Проигрыватель Windows Media, элемент Буттонтип
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694561"
---
# <a name="buttontip-element"></a>Буттонтип, элемент

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Элемент **буттонтип** задает текстовую строку, отображаемую при наведении пользователем на кнопку области задач.

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элемент                                              |
|-----------------|------------------------------------------------------|
| Родительские элементы | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Дочерние элементы  | Нет                                                 |



 

## <a name="remarks"></a>Remarks

Этот элемент является необязательным для каждого экземпляра **ServiceTask1**, **ServiceTask2** или **ServiceTask3**. Если этот элемент не указан, проигрыватель Windows Media использует текст кнопки в качестве значения по умолчанию.

> [!Note]  
> Проигрыватель Windows Media 10 содержит три области задач, в которых Интернет-магазин может отображать свои веб-страницы. Интернет-магазин может использовать одну, две или все три области задач. Проигрыватель Windows Media 11 имеет только одну область задач, которую пользователь может просматривать, щелкнув вкладку **Интернет-магазины** . проигрыватель Windows Media 11 игнорирует элементы **ServiceTask2** и **ServiceTask3** .

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 10 или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





