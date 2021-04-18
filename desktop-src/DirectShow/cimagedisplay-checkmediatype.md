---
description: Метод Чеккмедиатипе определяет, совместим ли предложенный тип мультимедиа с форматом вывода.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Цимажедисплай. Чеккмедиатипе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656947"
---
# <a name="cimagedisplaycheckmediatype-method"></a>Цимажедисплай. Чеккмедиатипе, метод

`CheckMediaType`Метод определяет, совместим ли предложенный тип мультимедиа с форматом вывода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмтин* 
</dt> <dd>

Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                  | Описание                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**\_Ошибка E**</dt> </dl>       | Недопустимый тип носителя.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый тип носителя.<br/>           |
| <dl> <dt>**\_ОК**</dt> </dl>         | Тип мультимедиа является совместимым.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




