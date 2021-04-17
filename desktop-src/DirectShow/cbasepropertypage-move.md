---
description: 'Метод Move размещает и изменяет размер диалогового окна. Этот метод реализует метод Ипропертипаже:: Move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Метод Кбасепропертипаже. Move (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668760"
---
# <a name="cbasepropertypagemove-method"></a>Кбасепропертипаже. Move, метод

`Move`Метод размещает и изменяет размер диалогового окна. Этот метод реализует метод **ипропертипаже:: Move** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прект* 
</dt> <dd>

Указатель на структуру **Rect** , содержащую сведения о размещении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                  | Описание                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Успешно.<br/>                   |
| <dl> <dt>**\_указатель E**</dt> </dl>    | **Пустой** аргумент указателя.<br/> |
| <dl> <dt>**\_непредвиденная E**</dt> </dl> | Непредвиденный сбой.<br/>        |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




