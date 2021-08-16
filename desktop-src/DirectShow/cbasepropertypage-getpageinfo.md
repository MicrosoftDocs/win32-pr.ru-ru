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
ms.openlocfilehash: badb0678faa85b70dfa848bba7538319b905feea440339e24285f3d64b59d61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823164"
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
| Заголовок<br/>  | <dl> <dt>кпроп. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




