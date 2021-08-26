---
description: Метод Шаулдупдате определяет, требуется ли создать новую палитру.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Цимажепалетте. Шаулдупдате, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c7897e14aec690ec67451fe868b5352e99c9bd513c8c182a47556fe075cffb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916034"
---
# <a name="cimagepaletteshouldupdate-method"></a>Цимажепалетте. Шаулдупдате, метод

`ShouldUpdate`Метод определяет, нужно ли создавать новую палитру.

## <a name="syntax"></a>Синтаксис


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пневинфо* 
</dt> <dd>

Указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , содержащую новую таблицу цветов.

</dd> <dt>

*полдинфо* 
</dt> <dd>

Указатель на структуру **видеоинфохеадер** , содержащую старую таблицу цветов. Этот параметр может принимать значение **NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если требуется обновить палитру, или **значение false** в противном случае.

## <a name="remarks"></a>Remarks

-   Если ни одна из структур **видеоинфохеадер** не содержит таблицу цветов, метод возвращает **значение false**.
-   Если только одна структура содержит таблицу цветов или если *полдинфо* имеет **значение NULL**, метод возвращает **значение true**.
-   Если обе структуры содержат таблицы цветов, а записи цветов совпадают, метод возвращает **значение false**.
-   Если обе структуры содержат таблицы цветов, но записи цветов не совпадают, метод возвращает **значение true**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Цимажепалетте**](cimagepalette.md)
</dt> </dl>

 

 




