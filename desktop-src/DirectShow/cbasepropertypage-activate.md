---
description: 'Метод Activate создает окно диалогового окна. Этот метод реализует метод Ипропертипаже:: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Метод Кбасепропертипаже. Activate (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b525eb16f534f0da8c847f50365c43124cb9e37d89f16629842fa202925a0674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108524"
---
# <a name="cbasepropertypageactivate-method"></a>Кбасепропертипаже. Activate, метод

`Activate`Метод создает окно диалогового окна. Этот метод реализует метод **ипропертипаже:: Activate** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвндпарент* 
</dt> <dd>

Обработано с родительским окном диалогового окна.

</dd> <dt>

*прект* 
</dt> <dd>

Указатель на структуру **Rect** , которая содержит сведения о размещении для диалогового окна.

</dd> <dt>

*фмодал* 
</dt> <dd>

Логическое значение, указывающее, является ли фрейм диалогового окна модальным (**true**) или немодальным (**false**).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                   | Описание                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>       |
| <dl> <dt>**\_указатель E**</dt> </dl>     | **Пустой** аргумент указателя.<br/> |
| <dl> <dt>**\_непредвиденная E**</dt> </dl>  | Непредвиденный сбой.<br/>        |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>кпроп. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> <dt>

[**Кбасепропертипаже:: OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




