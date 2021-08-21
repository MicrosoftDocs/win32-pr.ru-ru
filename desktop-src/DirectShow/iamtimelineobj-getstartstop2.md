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
ms.openlocfilehash: 1ff1644c2ba83848d0c9efa1b850a65aa8cfd1de1607a9fa0cabbab39579e0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155455"
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



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелинеобж**](iamtimelineobj.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




