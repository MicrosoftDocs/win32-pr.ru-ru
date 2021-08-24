---
description: Возвращает максимальный размер в байтах, необходимый для текущего потока, включая номер версии.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Кперсистстреам. Жетсиземакс, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 746fb01102642f2d3e6b254ac741c284143aaecfd401fc220bf7a9d97d93e64e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813374"
---
# <a name="cpersiststreamgetsizemax-method"></a>Кперсистстреам. Жетсиземакс, метод

Возвращает максимальный размер в байтах, необходимый для текущего потока, включая номер версии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкбсизе* 
</dt> <dd>

Указатель на размер в байтах, необходимый для сохранения этого потока, включая номер версии.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод **IPersistStream:: жетсиземакс** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>пстреам. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




