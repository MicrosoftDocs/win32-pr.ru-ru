---
title: Хтмлвиев, элемент
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Элемент Хтмлвиев указывает базовый URL-адрес веб-страницы Хтмлвиев.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Проигрыватель Windows Media, элемент Хтмлвиев
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695014"
---
# <a name="htmlview-element"></a>Хтмлвиев, элемент

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Элемент **хтмлвиев** указывает базовый URL-адрес веб-страницы хтмлвиев.

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Атрибуты

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (обязательно)
</dt> <dd>

Базовый URL-адрес веб-страницы Хтмлвиев, отображаемой проигрывателем Windows Media.

</dd> </dl>

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элемент         |
|-----------------|-----------------|
| Родительские элементы | **ServiceInfo** |
| Дочерние элементы  | Нет            |



 

## <a name="remarks"></a>Remarks

Этот элемент можно использовать для интеграции функции Хтмлвиев с вашим Интернет-магазином. Если домен URL-адреса, указанного в текущем интернет-магазине, соответствует одному для веб-страницы Хтмлвиев, переключиться на **Воспроизведение выполняется** без вмешательства пользователя и отображения содержимого хтмлвиев. В противном случае проигрыватель Windows Media запрашивает у пользователя разрешение на отображение содержимого Хтмлвиев.

Например, если URL-адрес веб-страницы Хтмлвиев имеет значение https://www.proseware.com/html/HTMLView.htm , а URL-адрес для атрибута **BaseURL** указан как https://www.proseware.com , то веб-страница хтмлвиев отображается без запроса пользователя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 10 или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Отображение веб-страниц в проигрывателе Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**PARAM, элемент**](param-element.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





