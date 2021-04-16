---
title: Элемент Navigate
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Элемент Navigate указывает URL-адрес, используемый вызовами метода external. Навигатетаскпанеурл.
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- Навигация по элементу проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648737"
---
# <a name="navigate-element"></a>Элемент Navigate

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Элемент **navigate** указывает URL-адрес, используемый вызовами метода **External. навигатетаскпанеурл**.

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Атрибуты



| Термин                                                                                                                                             | Описание                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (обязательно)<br/> | Полный URL-адрес веб-страницы, к которой осуществляется переход. **Навигатетаскпанеурл** может добавлять строку запроса к этому URL-адресу.<br/> |



 

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элемент         |
|-----------------|-----------------|
| Родительские элементы | **ServiceInfo** |
| Дочерние элементы  | Нет            |



 

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

[**External. Навигатетаскпанеурл**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





