---
description: 'Метод FixTimes2 Округляет указанное время начала и окончания до ближайших границ фрейма, как определено параметром частоты кадров родительской группы. Этот метод эквивалентен Иамтимелинеобж:: Фикстимес, но принимает значения РЕФТИМЕ.'
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'Метод Иамтимелинеобж:: FixTimes2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74890c2b094172ac3ced0c9fd192a755d051b56df22301b4d64d9003eaa74e9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400909"
---
# <a name="iamtimelineobjfixtimes2-method"></a>Метод Иамтимелинеобж:: FixTimes2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`FixTimes2`Метод Округляет указанное время начала и окончания до ближайших границ фрейма, как определено параметром частоты кадров родительской группы. Этот метод эквивалентен [**иамтимелинеобж:: фикстимес**](iamtimelineobj-fixtimes.md), но принимает значения [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстарт* 
</dt> <dd>

Указатель на переменную, содержащую время начала в секундах. Если вызов будет выполнен, для этой переменной задается округленное время.

</dd> <dt>

*пстоп* 
</dt> <dd>

Указатель на переменную, содержащую время окончания (в секундах). Если вызов будет выполнен, для этой переменной задается округленное время.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК в случае успеха или E \_ нотинтри, если объект не является частью группы.

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелинеобж**](iamtimelineobj.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




