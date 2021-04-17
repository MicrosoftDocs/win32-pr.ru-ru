---
title: Метод external. reкупает
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Purchase инициирует покупку набора элементов мультимедиа.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- Купить метод проигрыватель Windows Media Player
- Купить метод проигрыватель Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод "Купить"
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695099"
---
# <a name="externalbuy-method"></a>Метод external. reкупает

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **Purchase** инициирует покупку набора элементов мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ViewType* \[ окне\]
</dt> <dd>

**Строка** , указывающая тип покупаемого элемента. Вызывающий объект должен присвоить этому параметру одну из следующих [констант расположения библиотеки](library-location-constants.md):

кплистид

кптраккид

кпалбумид

</dd> <dt>

*Виевидс* \[ окне\]
</dt> <dd>

**Строка** , содержащая идентификаторы (разделенные точками с запятой) для покупаемых элементов.

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

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Внешняя. download**](external-download.md)
</dt> <dt>

[**Ивмпконтентпартнер:: Купить**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**Приобретение мультимедийного содержимого**](purchasing-media-content.md)
</dt> </dl>

 

 





