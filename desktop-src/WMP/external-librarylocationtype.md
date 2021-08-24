---
title: External. Либрарилокатионтипе
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Либрарилокатионтипе
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- External. либрарилокатионтипе проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e254ce6258cf667884e2815508b413ed1455b1b6924bfebb4edc900da048c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736204"
---
# <a name="externallibrarylocationtype"></a>External. Либрарилокатионтипе

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

свойство **либрарилокатионтипе** извлекает [константу расположения библиотеки](library-location-constants.md) , которая указывает тип текущего представления в проигрыватель Windows Media.

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** только для чтения, содержащей одну из констант расположения библиотеки.

## <a name="remarks"></a>Remarks

Это свойство работает в сочетании со свойством [External. либрарилокатионид](external-librarylocationid.md) . Например, предположим, что **либрарилокатионтипе** равен кпалбумид, а **либрарилокатионид** равен 3. это означает, что в текущем представлении в проигрыватель Windows Media отображается альбом с идентификатором 3. дополнительные сведения о том, как проигрыватель Windows Media характеризует представления содержимого интернет-магазина, см. в разделе [расположение и выбранный элемент](location-and-selected-item.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Либрарилокатионид**](external-librarylocationid.md)
</dt> <dt>

[**Расположение и выбранный элемент**](location-and-selected-item.md)
</dt> </dl>

 

 





