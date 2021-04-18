---
description: Метод Сетпоинтер задает указатель на буфер памяти.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Кмедиасампле. Сетпоинтер, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674981"
---
# <a name="cmediasamplesetpointer-method"></a>Кмедиасампле. Сетпоинтер, метод

`SetPointer`Метод задает указатель на буфер памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ptr* 
</dt> <dd>

Указатель на буфер памяти, выделенный вызывающей стороной размера *кбитес*.

</dd> <dt>

*кбитес* 
</dt> <dd>

Длина буфера в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод позволяет распределительу установить новый указатель для образца.

Этот метод недоступен через интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Объект, создающий образец, может получить доступ к этому методу (через **кмедиасампле**), но другие объекты не могут.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




