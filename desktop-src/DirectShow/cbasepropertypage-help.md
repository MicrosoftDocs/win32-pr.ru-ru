---
description: 'Метод Help вызывает справку страницы свойств. Этот метод реализует метод Ипропертипаже:: Help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Метод Кбасепропертипаже. Help (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668990"
---
# <a name="cbasepropertypagehelp-method"></a>Кбасепропертипаже. Help, метод

`Help`Метод вызывает справку страницы свойств. Этот метод реализует метод **ипропертипаже:: Help** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсзелпдир* 
</dt> <dd>

Указатель на строку в ключе **хелпдир** в СВЕДЕНИЯх CLSID на странице свойств в реестре.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает E \_ нотимпл.

## <a name="remarks"></a>Комментарии

В базовом классе метод всегда возвращает E \_ нотимпл. При сбое метода кадр вызывает **ипропертипаже:: жетпажеинфо** , чтобы получить имя файла справки и идентификатор контекста. По умолчанию они имеют **значение NULL**. Чтобы обеспечить помощь, производный класс может переопределить либо метод, `Help` либо метод [**кбасепропертипаже:: жетпажеинфо**](cbasepropertypage-getpageinfo.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




