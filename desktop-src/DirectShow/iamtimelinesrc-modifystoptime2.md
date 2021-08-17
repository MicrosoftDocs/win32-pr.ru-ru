---
description: 'Метод ModifyStopTime2 задает время окончания. Этот метод эквивалентен Иамтимелинесрк:: Модифистоптиме, но принимает значение РЕФТИМЕ.'
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'Метод Иамтимелинесрк:: ModifyStopTime2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa2ec7a019200f91c9fb2a894c978ce93896926024f55efb229c7e5fde6fbe85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952813"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a>Метод Иамтимелинесрк:: ModifyStopTime2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`ModifyStopTime2`Метод задает время окончания. Этот метод эквивалентен [**иамтимелинесрк:: модифистоптиме**](iamtimelinesrc-modifystoptime.md), но принимает значение [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Остановить* 
</dt> <dd>

Новое время окончания в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение \_ ОК, если успешно, или E \_ INVALIDARG, если указанное время недопустимо.

## <a name="remarks"></a>Remarks

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

[**Интерфейс Иамтимелинесрк**](iamtimelinesrc.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




