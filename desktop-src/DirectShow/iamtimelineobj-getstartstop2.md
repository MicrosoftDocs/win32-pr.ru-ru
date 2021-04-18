---
description: 'Метод GetStartStop2 извлекает значения времени начала и окончания объекта относительно родителя объекта. Этот метод эквивалентен Иамтимелинеобж:: Жетстартстоп, но принимает значения РЕФТИМЕ.'
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'Метод Иамтимелинеобж:: GetStartStop2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685395"
---
# <a name="iamtimelineobjgetstartstop2-method"></a>Метод Иамтимелинеобж:: GetStartStop2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetStartStop2`Метод получает значения времени начала и окончания объекта относительно родителя объекта. Этот метод эквивалентен [**иамтимелинеобж:: жетстартстоп**](iamtimelineobj-getstartstop.md), но принимает значения [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстарт* 
</dt> <dd>

Получает время начала в секундах.

</dd> <dt>

*пстоп* 
</dt> <dd>

Получает время окончания в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелинеобж**](iamtimelineobj.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




