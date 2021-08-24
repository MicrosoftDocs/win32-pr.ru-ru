---
description: Метод INSERT добавляет объект Кдеферредкомманд в очередь.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Метод Ккмдкуеуе. Insert (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90e2bab4a3545e8a02315155ad4a477511ecf961c93a511ccba268b7fde7dd0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757324"
---
# <a name="ccmdqueueinsert-method"></a>Ккмдкуеуе. INSERT, метод

`Insert`Метод добавляет объект [**кдеферредкомманд**](cdeferredcommand.md) в очередь.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pCmd* 
</dt> <dd>

Указатель на объект **кдеферредкомманд** для добавления в очередь.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК в реализации по умолчанию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




