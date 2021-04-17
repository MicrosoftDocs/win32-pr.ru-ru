---
title: THEME. Лоадпреференце
description: Метод Лоадпреференце загружает предпочтение из реестра.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- Проигрыватель Windows Media THEME. Лоадпреференце
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680090"
---
# <a name="themeloadpreference"></a>THEME. Лоадпреференце

Метод **лоадпреференце** загружает предпочтение из реестра.

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*секэй*
</dt> <dd>

**Строка** , указывающая ключ значения предпочтения для загрузки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку**.

## <a name="remarks"></a>Комментарии

Предпочтение — это пара "ключ-значение", которая может храниться в реестре для сохранения сведений о состоянии проигрывателя Windows Media между запусками. Эта функция может использоваться, например, для сохранения параметров настройки, чтобы их не нужно было повторно указывать каждый раз при запуске проигрывателя Windows Media.

Параметры не шифруются и поэтому не являются безопасным методом для сохранения данных. Не используйте настройки для хранения частных данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> <dt>

[**THEME. Савепреференце**](theme-savepreference.md)
</dt> </dl>

 

 





