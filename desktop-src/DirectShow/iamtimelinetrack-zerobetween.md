---
description: Метод Зеробетвин удаляет все данные из трассировки в указанное время. Этот метод разделяет все объекты, охватывающие указанный диапазон времени, и удаляет части, попадающие в диапазон.
ms.assetid: df173a3c-147b-4f2d-9bcb-a8c2873f5420
title: 'Метод Иамтимелинетракк:: Зеробетвин (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b5ec57833ed34a432988c42351a333362168112174cccd7a989e0c2e1bddd694
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982904"
---
# <a name="iamtimelinetrackzerobetween-method"></a>Метод Иамтимелинетракк:: Зеробетвин

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`ZeroBetween`Метод удаляет все данные из трассировки в указанное время. Этот метод разделяет все объекты, охватывающие указанный диапазон времени, и удаляет части, попадающие в диапазон.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ZeroBetween(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ртстарт* 
</dt> <dd>

Начало диапазона для очистки, в единицах 100-наносекундных.

</dd> <dt>

*ртенд* 
</dt> <dd>

Конец диапазона, который необходимо очистить, в единицах 100-наносекундных.

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

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелинетракк**](iamtimelinetrack.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




