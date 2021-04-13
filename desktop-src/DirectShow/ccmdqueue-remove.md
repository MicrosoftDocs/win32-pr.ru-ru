---
description: Метод Remove удаляет объект Кдеферредкомманд из очереди.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Метод Ккмдкуеуе. Remove (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657969"
---
# <a name="ccmdqueueremove-method"></a>Ккмдкуеуе. Remove, метод

`Remove`Метод удаляет объект [**кдеферредкомманд**](cdeferredcommand.md) из очереди.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pCmd* 
</dt> <dd>

Указатель на объект **кдеферредкомманд** , который необходимо удалить из очереди.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает VFW \_ E \_ не \_ найден, если объект не найден в очереди. В противном случае возвращается значение S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




