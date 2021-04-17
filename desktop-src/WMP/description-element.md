---
title: Элемент Description
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Description, элемент
ms.assetid: 4d9ff447-e5a4-46b1-b599-87202077abfb
keywords:
- Элемент Description. проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Description Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4318a7936f4713d3ff89a2fa73731eea0cdd97db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694760"
---
# <a name="description-element"></a>Элемент Description

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Элемент **Description** указывает маркетинговое описание Интернет-магазина, которое отображается при первом запуске пользователя с установкой проигрывателя Windows Media.

``` syntax
<Description>
    text string
</Description>
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элемент         |
|-----------------|-----------------|
| Родительские элементы | **ServiceInfo** |
| Дочерние элементы  | Нет            |



 

## <a name="remarks"></a>Remarks

Длина описания должна быть меньше или равна 255 символам.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





