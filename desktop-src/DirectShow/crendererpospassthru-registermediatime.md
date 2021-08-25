---
description: Метод Регистермедиатиме кэширует метки времени из текущего образца.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Крендерерпоспасссру. Регистермедиатиме, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69688bb011fc8a75b0ec52effaef3afd7972fb7a198a4cdedf20c07a40c4fa7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054384"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Крендерерпоспасссру. Регистермедиатиме, метод (Ктлутил. h)

Метод **регистермедиатиме** кэширует метки времени из текущего образца.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают перечисленные в следующей таблице.



| Код возврата                                                                                                  | Описание                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                         | Успешно.<br/>                        |
| <dl> <dt>**\_ \_ \_ \_ не задано время в \_ подключении к VFW E Media**</dt> </dl> | Образец не имеет отметки времени.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод сохраняет метки времени из текущего образца. Метод [**крендерерпоспасссру:: жетмедиатиме**](crendererpospassthru-getmediatime.md) получает те же значения.

Фильтр должен вызывать этот метод для каждого получаемого примера. Метод перегружен, чтобы принять либо указатель на образец, либо сами значения меток времени.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




