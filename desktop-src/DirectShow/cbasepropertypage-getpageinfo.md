---
description: 'Метод Жетпажеинфо извлекает сведения о странице свойств. Этот метод реализует метод Ипропертипаже:: Жетпажеинфо.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Кбасепропертипаже. Жетпажеинфо, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668993"
---
# <a name="cbasepropertypagegetpageinfo-method"></a>Кбасепропертипаже. Жетпажеинфо, метод

`GetPageInfo`Метод получает сведения о странице свойств. Этот метод реализует метод **ипропертипаже:: жетпажеинфо** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pPageInfo* 
</dt> <dd>

Указатель на структуру **проппажеинфо** , выделенную вызывающей стороной.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                   | Описание                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




