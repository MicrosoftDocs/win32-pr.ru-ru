---
title: Внешнее событие Ончанжевиеверрор
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | Внешнее событие Ончанжевиеверрор
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- проигрыватель Windows Media события External. ончанжевиеверрор
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa1152c753501b2e2385de8c56af614d62cfb367fcca8468aaa032e9536e8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648834"
---
# <a name="externalonchangeviewerror-event"></a>Внешнее событие Ончанжевиеверрор

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Событие **ончанжевиеверрор** возникает, когда вызов метода [External. чанжевиев](external-changeview.md) приводит к ошибке.

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a>Возможные значения

это свойство только для записи, которое указывает имя функции в скрипте, проигрыватель Windows Media вызывается при возникновении события.

## <a name="parameters"></a>Параметры

Функция, обрабатывающая это событие, имеет следующие параметры.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*кадров*
</dt> <dd>

Код ошибки **HRESULT** , указывающий причину сбоя.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*либрарилокатионтипе*
</dt> <dd>

Та же строка, которая была передана в параметре **либрарилокатионтипе** объекта **чанжевиев**.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*либрарилокатионид*
</dt> <dd>

Строка сатвас, переданная в параметре **либрарилокатионид** объекта **чанжевиев**.

</dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Фильтрация*
</dt> <dd>

Та же строка, которая была передана в параметре **Filter** параметра **чанжевиев**.

</dd> <dt>

<span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*виевпарамс*
</dt> <dd>

Та же строка, которая была передана в параметре **виевпарамс** объекта **чанжевиев**.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Екстерналобжект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





