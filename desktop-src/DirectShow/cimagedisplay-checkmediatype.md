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
ms.openlocfilehash: 6bad6a7242ba110ad3916d08070eef40a8fa1d5d658ea366732e14a1cd107d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087394"
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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




