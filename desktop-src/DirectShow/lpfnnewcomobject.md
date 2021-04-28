---
description: Указатель функции Лпфнневкомобжект — указатель на функцию, которая создает экземпляр объекта.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Указатель функции Лпфнневкомобжект (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: f3ea5bc172bc22f7aa9dce1f348bba552520565f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116532"
---
# <a name="lpfnnewcomobject-function-pointer"></a>Указатель функции Лпфнневкомобжект

Указатель на функцию, которая создает экземпляр объекта.

## <a name="syntax"></a>Синтаксис


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пункаутер* 
</dt> <dd>

Указатель на интерфейс **IUnknown** объекта, который выполняет статистическую обработку нового объекта, если он имеется. Этот указатель может иметь **значение NULL**.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на значение **HRESULT** . Если конструктор завершается неудачно, этот параметр получает код ошибки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на новый экземпляр объекта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кфакторитемплате**](cfactorytemplate.md)
</dt> </dl>

 

 




