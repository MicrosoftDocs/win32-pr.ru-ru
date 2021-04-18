---
description: Метод Жеттипеинфокаунт извлекает количество интерфейсов сведений о типе, предоставляемых объектом.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Кбаседиспатч. Жеттипеинфокаунт, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39c5b78181f5f26fb5f57831345bb6345a26da85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657301"
---
# <a name="cbasedispatchgettypeinfocount-method"></a>Кбаседиспатч. Жеттипеинфокаунт, метод

`GetTypeInfoCount`Метод получает количество интерфейсов сведений о типе, предоставляемых объектом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пктинфо* 
</dt> <dd>

Указатель на переменную, которая получает количество интерфейсов типа данных, предоставленных объектом. При возврате из метода значение равно 1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений.



| Код возврата                                                                               | Описание                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Успешно.<br/>                   |
| <dl> <dt>**\_указатель E**</dt> </dl> | **Пустой** аргумент указателя.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаседиспатч**](cbasedispatch.md)
</dt> </dl>

 

 




