---
description: Метод GetTypeInfo извлекает сведения о типе для объекта, который затем можно использовать для получения сведений о типе для интерфейса.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Кмедиапоситион. GetTypeInfo, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669226"
---
# <a name="cmediapositiongettypeinfo-method"></a>Кмедиапоситион. GetTypeInfo, метод

`GetTypeInfo`Метод получает сведения о типе для объекта, который затем можно использовать для получения сведений о типе для интерфейса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*итинфо* 
</dt> <dd>

Возвращаемые сведения о типе. Должен равняться нулю.

</dd> <dt>

*lcid* 
</dt> <dd>

Идентификатор языкового стандарта.

</dd> <dt>

*пптинфо* 
</dt> <dd>

Адрес переменной, получающей указатель **ITypeInfo** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                             | Описание                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                    | Успешно.<br/>                            |
| <dl> <dt>**\_указатель E**</dt> </dl>               | **Пустой** аргумент указателя.<br/>          |
| <dl> <dt>**Введите \_ E \_ елементнотфаунд**</dt> </dl> | Параметр *итинфо* не равен нулю.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиапоситион**](cmediaposition.md)
</dt> </dl>

 

 




