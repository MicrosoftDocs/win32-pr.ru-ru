---
description: Сохраняет данные фильтра в заданном потоке.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Метод Кперсистстреам. Save (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668666"
---
# <a name="cpersiststreamsave-method"></a>Кперсистстреам. Save, метод

Сохраняет данные фильтра в заданном потоке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстм* 
</dt> <dd>

Указатель на поток, в который должны быть сохранены данные.

</dd> <dt>

*фклеардирти* 
</dt> <dd>

Флаг, указывающий, следует ли сбрасывать флаг "грязный" текущего потока; **Значение true** означает сброс. (Если метод вызывается как часть операции сохранения, значение обычно равно **true**; при вызове как часть операции сохранения как значение обычно равно **false**.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод **IPersistStream:: Save** . Он вызывает **вритеинт** с версией программного обеспечения, [**вызывает Кперсистстреам:: вритетостреам**](cpersiststream-writetostream.md) с потоком в *пстм* и сбрасывает **mPS \_ фдирти**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пстреам. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




