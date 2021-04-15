---
description: Предоставляет доступ к открытым свойствам и методам объекта.
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Метод Кмедиаконтрол. Invoke (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b9a29d163180ffc609ca44f2bbbfb2870c5faef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675627"
---
# <a name="cmediacontrolinvoke-method"></a>Кмедиаконтрол. Invoke, метод

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

Идентификатор элемента. Чтобы получить идентификатор диспетчеризации, используйте [**кмедиаконтрол:: GetIdsOfNames**](cmediacontrol-getidsofnames.md) или документацию объекта.

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

Флаги, описывающие контекст `CMediaControl::Invoke` вызова.

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

Возвращает \_ \_ значение ункновнинтерфаце E, если *RIID* не является IID \_ null. Возвращает один из кодов ошибок из [**кмедиаконтрол:: GetTypeInfo**](cmediacontrol-gettypeinfo.md) , если вызов завершается с ошибкой. В противном случае возвращает **значение HRESULT** из вызова **IDispatch:: Invoke**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиаконтрол**](cmediacontrol.md)
</dt> </dl>

 

 




