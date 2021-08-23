---
title: External. Аддтобаскет, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Аддтобаскет, метод
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- проигрыватель Windows Media метода аддтобаскет
- проигрыватель Windows Media метода аддтобаскет, внешний класс
- внешний класс проигрыватель Windows Media, метод аддтобаскет
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f51cfc3df641b02a5aa3a0869e810f318357dd70ba67acb3ec2310f8a5a355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650014"
---
# <a name="externaladdtobasket-method"></a>External. Аддтобаскет, метод

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

метод **аддтобаскет** добавляет элементы мультимедиа на панель списка (также называемую корзиной) в проигрыватель Windows Media.

## <a name="syntax"></a>Синтаксис


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ViewType* \[ окне\]
</dt> <dd>

**Строка** , указывающая тип элемента, добавляемого на панель списка. Вызывающий объект должен присвоить этому параметру одну из следующих [констант расположения библиотеки](library-location-constants.md):

кплистид

кптраккид

кпалбумид

кпартист

кпженреид

кпалбумсубженреид

кпрадиоид

</dd> <dt>

*Виевидс* \[ окне\]
</dt> <dd>

**Строка** , содержащая идентификаторы, разделенные точками с запятой, для элементов, добавляемых на панель списка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Екстерналобжект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Баскеттитле**](external-baskettitle.md)
</dt> </dl>

 

 





