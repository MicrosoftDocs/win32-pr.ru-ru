---
description: 'Ксаурцесикинг. capabilities-метод — метод capabilities извлекает все возможности поиска в потоке. Этот метод реализует метод Имедиасикинг:: Capabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Метод Ксаурцесикинг. Capabilities (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96e3a637673a91ebc98e48777b8f42bdcbf02654a0c264037a66b4121f5b80ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054344"
---
# <a name="csourceseekinggetcapabilities-method"></a>Ксаурцесикинг. capabilities, метод

`GetCapabilities`Метод извлекает все возможности поиска в потоке. Этот метод реализует метод [**имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкапабилитиес* 
</dt> <dd>

Указатель на переменную, которая получает побитовую комбинацию флагов [**\_ \_ поиска \_ возможностей**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.



| Код возврата                                                                               | Описание                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl> | Значение указателя **null**<br/> |



 

## <a name="remarks"></a>Remarks

Возможности поиска задаются переменной члена [**ксаурцесикинг:: m \_ двсикингкапс**](csourceseeking-m-dwseekingcaps.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




