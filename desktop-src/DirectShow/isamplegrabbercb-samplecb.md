---
description: Метод Самплекб — это метод обратного вызова, который получает указатель на пример носителя.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'Метод Исамплеграбберкб:: Самплекб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e98377050ec98cdccaedd54119afb6cdaccbaee56256f1406bb190d3ea875bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817516"
---
# <a name="isamplegrabbercbsamplecb-method"></a>Метод Исамплеграбберкб:: Самплекб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SampleCB`Метод является методом обратного вызова, который получает указатель на пример носителя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*самплетиме* 
</dt> <dd>

Время начала выборки в секундах.

</dd> <dt>

*псампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение \_ ОК в случае успеха или код ошибки **HRESULT** в противном случае.

## <a name="remarks"></a>Remarks

Чтобы настроить обратный вызов, вызовите [**исамплеграббер:: сеткаллбакк**](isamplegrabber-setcallback.md).

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> <dt>

[**Интерфейс Исамплеграбберкб**](isamplegrabbercb.md)
</dt> </dl>

 

 




