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
ms.openlocfilehash: af6747eb9ed39a973d795d8701fd9d7afd1b88e9d0b0db577de6a8e963b840bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634354"
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

*указатель* 
</dt> <dd>

Указатель на буфер памяти, выделенный вызывающей стороной размера *кбитес*.

</dd> <dt>

*кбитес* 
</dt> <dd>

Длина буфера в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод позволяет распределительу установить новый указатель для образца.

Этот метод недоступен через интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Объект, создающий образец, может получить доступ к этому методу (через **кмедиасампле**), но другие объекты не могут.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




