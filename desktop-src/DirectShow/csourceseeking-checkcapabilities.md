---
description: 'Метод Чекккапабилитиес запрашивает, есть ли у потока указанные возможности поиска. Этот метод реализует метод Имедиасикинг:: Чекккапабилитиес.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Ксаурцесикинг. Чекккапабилитиес, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657028"
---
# <a name="csourceseekingcheckcapabilities-method"></a>Ксаурцесикинг. Чекккапабилитиес, метод

`CheckCapabilities`Метод запрашивает, имеет ли поток указанные возможности поиска. Этот метод реализует метод [**имедиасикинг:: чекккапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкапабилитиес* 
</dt> <dd>

Указатель на побитовую комбинацию одного или нескольких атрибутов [**\_ \_ \_ возможностей**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) поиска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.



| Код возврата                                                                               | Описание                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Существуют не все возможности в *пкапабилитиес* .<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>      | В *пкапабилитиес* есть все возможности.<br/>            |
| <dl> <dt>**\_указатель E**</dt> </dl> | **Пустой** аргумент указателя.<br/>                                  |



 

## <a name="remarks"></a>Комментарии

Как реализованный, этот метод проверяет значение *\* пкапабилитиес* на соответствие переменной члена [**ксаурцесикинг:: m \_ двсикингкапс**](csourceseeking-m-dwseekingcaps.md) . Однако он не устанавливает *\* пкапабилитиес* равным **m \_ двсикингкапс**, как описано в методе [**имедиасикинг:: чекккапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) . Кроме того, в случае, если ни одна из указанных возможностей не доступна, метод не возвращает значение E \_ Failed. Более полная реализация будет выглядеть следующим образом:


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




