---
description: 'Метод ZeroBetween2 удаляет все данные из трассировки в указанное время. Этот метод эквивалентен Иамтимелинетракк:: Зеробетвин, но принимает значения РЕФТИМЕ.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'Метод Иамтимелинетракк:: ZeroBetween2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72ea9d96be976f1b09e1cdc9721eb5eebe7adce2905d7a028d70a9ff50ff58bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952783"
---
# <a name="iamtimelinetrackzerobetween2-method"></a>Метод Иамтимелинетракк:: ZeroBetween2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`ZeroBetween2`Метод удаляет все данные из трассировки в указанное время. Этот метод эквивалентен [**иамтимелинетракк:: зеробетвин**](iamtimelinetrack-zerobetween.md), но принимает значения [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ртстарт* 
</dt> <dd>

Начало диапазона для очистки в секундах.

</dd> <dt>

*ртенд* 
</dt> <dd>

Конец диапазона для очистки, в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                             | Описание                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Диапазон времени превышает все, что находится в дорожке.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                                             |



 

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

[**Интерфейс Иамтимелинетракк**](iamtimelinetrack.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




