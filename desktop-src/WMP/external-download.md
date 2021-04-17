---
title: Метод external. download
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод download инициирует загрузку набора элементов мультимедиа.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- Загрузка метода Windows Media Player
- метод загрузки Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод download
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694503"
---
# <a name="externaldownload-method"></a>Метод external. download

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **download** инициирует загрузку набора элементов мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тип* \[ окне\]
</dt> <dd>

[Константа расположения библиотеки](library-location-constants.md) , указывающая тип загружаемого элемента. Например, Кптраккид указывает, что необходимо загрузить одну или несколько дорожек.

</dd> <dt>

*Идентификаторы* \[ окне\]
</dt> <dd>

**Строка** , содержащая идентификаторы (разделенные точками с запятой) загружаемых элементов мультимедиа.

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

[**Загрузка мультимедийного содержимого**](downloading-media-content.md)
</dt> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Купить**](external-buy.md)
</dt> <dt>

[**Ивмпконтентпартнер::D гружать**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





