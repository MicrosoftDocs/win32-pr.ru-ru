---
title: External. Аддтобаскет, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Аддтобаскет, метод
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- Аддтобаскет метод Windows Media Player
- Аддтобаскет метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Аддтобаскет
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
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695209"
---
# <a name="externaladdtobasket-method"></a>External. Аддтобаскет, метод

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **аддтобаскет** добавляет элементы мультимедиа на панель списка (также называемую корзиной) в проигрывателе Windows Media.

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Екстерналобжект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Баскеттитле**](external-baskettitle.md)
</dt> </dl>

 

 





