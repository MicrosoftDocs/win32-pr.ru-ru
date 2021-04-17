---
title: Внешнее событие Ончанжевиевонлинелистеррор
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | Внешнее событие Ончанжевиевонлинелистеррор
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Проигрыватель Windows Media для события external. Ончанжевиевонлинелистеррор
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698884"
---
# <a name="externalonchangeviewonlinelisterror-event"></a>Внешнее событие Ончанжевиевонлинелистеррор

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Событие **ончанжевиевонлинелистеррор** возникает, когда вызов метода [External. чанжевиевонлинелист](external-changeviewonlinelist.md) приводит к ошибке.

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a>Возможные значения

Это свойство только для записи, которое указывает имя функции в скрипте, которое вызывает проигрыватель Windows Media при возникновении события.

## <a name="parameters"></a>Параметры

Функция, обрабатывающая эту ошибку, имеет следующие параметры.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*кадров*
</dt> <dd>

Код ошибки **HRESULT** , указывающий причину сбоя.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*либрарилокатионтипе*
</dt> <dd>

Та же строка, которая была передана в параметре **либрарилокатионтипе** объекта **чанжевиевонлинелист**.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*либрарилокатионид*
</dt> <dd>

Та же строка, которая была передана в параметре **либрарилокатионид** объекта **чанжевиевонлинелист**.

</dd> <dt>

<span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*
</dt> <dd>

Та же строка, которая была передана в параметре **params** объекта **чанжевиевонлинелист**.

</dd> <dt>

<span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*
</dt> <dd>

Та же строка, которая была передана в параметре **FriendlyName** параметра **чанжевиевонлинелист**.

</dd> <dt>

<span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*листтипе*
</dt> <dd>

Та же строка, которая была передана в параметре **листтипе** объекта **чанжевиевонлинелист**.

</dd> <dt>

<span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*
</dt> <dd>

Та же строка, которая была передана в параметре **ViewMode** объекта **чанжевиевонлинелист**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





