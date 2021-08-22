---
title: THEME. Савепреференце
description: Метод Савепреференце сохраняет предпочтение в реестре.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- проигрыватель Windows Media THEME. савепреференце
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d5f9edca154ff6402028ba873c1643e330ab316a54a63f14fa4f9b5bdb244483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134547"
---
# <a name="themesavepreference"></a>THEME. Савепреференце

Метод **савепреференце** сохраняет предпочтение в реестре.

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*секэй*
</dt> <dd>

**Строка** , указывающая ключ значения предпочтения для сохранения.

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*Значение типа представляющее*
</dt> <dd>

**Строка** , указывающая значение для сохранения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

предпочтение — это пара "ключ-значение", которая может храниться в реестре для сохранения сведений о состоянии проигрыватель Windows Media между запусками. эта функция может использоваться, например, для сохранения параметров настройки, чтобы их не нужно было повторно указывать при каждом запуске проигрыватель Windows Media.

Параметры не шифруются и поэтому не являются безопасным методом для сохранения данных. Не используйте настройки для хранения частных данных.

## <a name="examples"></a>Примеры


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> <dt>

[**THEME. Лоадпреференце**](theme-loadpreference.md)
</dt> </dl>

 

 





