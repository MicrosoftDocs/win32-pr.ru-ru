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
ms.openlocfilehash: cc86d50c5692f48c7fb00b45228b13c88c96137473cee3609013f782a0a2d7ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502844"
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

## <a name="remarks"></a>Remarks

Переопределите этот метод, если требуется предоставить сочетания клавиш для страницы свойств.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>кпроп. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




