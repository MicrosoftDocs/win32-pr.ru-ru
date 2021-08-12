---
description: Метод Кмедиаевент. Invoke — предоставляет доступ к свойствам и методам, предоставляемым объектом.
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: Метод Кмедиаевент. Invoke (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37fadefe3163ed4211b8112ec17cc1cfb3fb3625b4aba207db06a25de3e27b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655228"
---
# <a name="cmediaeventinvoke-method"></a>Кмедиаевент. Invoke, метод

Предоставляет доступ к открытым свойствам и методам объекта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*диспидмембер* 
</dt> <dd>

Идентификатор элемента. Чтобы получить идентификатор диспетчеризации, используйте [**кмедиаевент:: GetIdsOfNames**](cmediaevent-getidsofnames.md) или документацию объекта.

</dd> <dt>

*riid* 
</dt> <dd>

Зарезервировано для последующего использования. Должен иметь \_ значение IID null.

</dd> <dt>

*lcid* 
</dt> <dd>

Контекст языкового стандарта, в котором следует интерпретировать аргументы.

</dd> <dt>

*вфлагс* 
</dt> <dd>

Флаги, описывающие контекст `CMediaEvent::Invoke` вызова.

</dd> <dt>

*пдисппарамс* 
</dt> <dd>

Указатель на структуру, содержащую массив аргументов, массив идентификаторов диспетчеризации аргументов для именованных аргументов и количество элементов в массивах.

</dd> <dt>

*пварресулт* 
</dt> <dd>

Указатель на место хранения результата или **значение NULL** , если вызывающий объект не ждет результата.

</dd> <dt>

*пексцепинфо* 
</dt> <dd>

Указатель на структуру, содержащую сведения об исключении.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Указатель на индекс первого аргумента в массиве **rgvarg** структуры **DISPPARAMS** , который содержит ошибку. Дополнительные сведения о **DISPPARAMS** см. в разделе пакет SDK для платформы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ \_ значение ункновнинтерфаце E, если *RIID* не является IID \_ null. Возвращает один из кодов ошибок из [**кмедиаевент:: GetTypeInfo**](cmediaevent-gettypeinfo.md) , если вызов завершается с ошибкой. В противном случае возвращает **значение HRESULT** из вызова **IDispatch:: Invoke**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиаевент**](cmediaevent.md)
</dt> </dl>

 

 




