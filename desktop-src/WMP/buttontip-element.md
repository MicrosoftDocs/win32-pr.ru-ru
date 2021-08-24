---
title: Буттонтип, элемент
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Буттонтип, элемент
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- проигрыватель Windows Media элемента буттонтип
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7fb4a162a8e77fea7548265825af6c6cbda75dbafadf05fe32cb664c4d563f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764304"
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

Этот элемент является необязательным для каждого экземпляра **ServiceTask1**, **ServiceTask2** или **ServiceTask3**. если этот элемент не указан, проигрыватель Windows Media использует текст кнопки в качестве значения по умолчанию.

> [!Note]  
> в проигрыватель Windows Media 10 есть три области задач, в которых интернет-магазин может отображать свои веб-страницы. Интернет-магазин может использовать одну, две или все три области задач. проигрыватель Windows Media 11 имеет только одну область задач, которую пользователь может просматривать, щелкнув вкладку **интернет-магазины** . проигрыватель Windows Media 11 не учитывает элементы **ServiceTask2** и **ServiceTask3** .

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 10 или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





