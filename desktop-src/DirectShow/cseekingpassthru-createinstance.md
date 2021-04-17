---
description: Метод CreateInstance создает экземпляр объекта. Этот метод поддерживает создание объекта с помощью фабрики классов. Дополнительные сведения см. в разделе Кфакторитемплате.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Метод Ксикингпасссру. CreateInstance (Сикпт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657272"
---
# <a name="cseekingpassthrucreateinstance-method"></a>Ксикингпасссру. CreateInstance, метод

`CreateInstance`Метод создает экземпляр объекта. Этот метод поддерживает создание объекта с помощью фабрики классов. Дополнительные сведения см. в разделе [**кфакторитемплате**](cfactorytemplate.md).

## <a name="syntax"></a>Синтаксис


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pUnk* 
</dt> <dd>

Указатель на владельца этого объекта. Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования. В противном случае присвойте этому параметру **значение NULL**.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на значение **HRESULT** . Не обрабатывается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на новый объект **ксикингпасссру** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Сикпт. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксикингпасссру**](cseekingpassthru.md)
</dt> </dl>

 

 




