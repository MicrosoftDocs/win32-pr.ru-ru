---
description: Метод Сетформат инициализирует блок формата.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Кмедиатипе. Сетформат, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99726a466b6bf273b654a5d459fa2391a75882f1adee64b981d91a514a988b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108454"
---
# <a name="cmediatypesetformat-method"></a>Кмедиатипе. Сетформат, метод

`SetFormat`Метод инициализирует блок формата.

## <a name="syntax"></a>Синтаксис


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пформат* 
</dt> <dd>

Указатель на блок памяти, который содержит блок формата.

</dd> <dt>

*length* 
</dt> <dd>

Длина блока формата в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **значение false** , если произошла ошибка.

## <a name="remarks"></a>Remarks

Этот метод выделяет память для блока формата и копирует буфер, указанный параметром *пформат* , в новый блок формата. Если тип мультимедиа уже содержит блок формата, старый он освобождается. Метод также задает элемент **кбформат** структуры **\_ \_ типа мультимедиа AM** .

Чтобы задать тип формата, вызовите метод [**кмедиатипе:: сетформаттипе**](cmediatype-setformattype.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




