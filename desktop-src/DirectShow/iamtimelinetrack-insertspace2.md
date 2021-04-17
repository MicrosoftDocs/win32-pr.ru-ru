---
description: 'Метод InsertSpace2 разделяет все объекты, существующие в указанное время, и вставляет между ними пробелы. Этот метод эквивалентен Иамтимелинетракк:: Инсертспаце, но принимает значения РЕФТИМЕ.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'Метод Иамтимелинетракк:: InsertSpace2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685232"
---
# <a name="iamtimelinetrackinsertspace2-method"></a>Метод Иамтимелинетракк:: InsertSpace2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`InsertSpace2`Метод разделяет все объекты, существующие в указанное время, и вставляет между ними пробелы. Этот метод эквивалентен [**иамтимелинетракк:: инсертспаце**](iamtimelinetrack-insertspace.md), но принимает значения [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ртстарт* 
</dt> <dd>

Время, когда нужно создать разбиение, и начальную точку вставленного пространства в секундах.

</dd> <dt>

*ртенд* 
</dt> <dd>

Конечная точка вставленного пространства в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные возвращаемые значения включают следующее.



| Код возврата                                                                                   | Описание                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | В указанное время нет объектов.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый аргумент.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                        |



 

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

[**Интерфейс Иамтимелинетракк**](iamtimelinetrack.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




