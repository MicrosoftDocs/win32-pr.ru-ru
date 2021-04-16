---
description: 'Метод TranslateAccelerator указывает странице свойств обработать нажатие клавиши. Этот метод реализует метод Ипропертипаже:: TranslateAccelerator.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: Кбасепропертипаже. TranslateAccelerator, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656897"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a>Кбасепропертипаже. TranslateAccelerator, метод

`TranslateAccelerator`Метод указывает странице свойств обработать нажатие клавиши. Этот метод реализует метод **ипропертипаже:: TranslateAccelerator** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпмсг* 
</dt> <dd>

Указатель на структуру **MSG** , описывающую нажатие клавиши для обработки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает E \_ нотимпл.

## <a name="remarks"></a>Комментарии

Переопределите этот метод, если требуется предоставить сочетания клавиш для страницы свойств.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




