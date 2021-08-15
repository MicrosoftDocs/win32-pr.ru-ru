---
description: Метод Инсертспаце разделяет все объекты, существующие в указанное время, и вставляет между ними пробелы.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'Метод Иамтимелинетракк:: Инсертспаце (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a51e89a72d813e1f5a9c1c05b1a46b6674906284b61b4036c164af87af9a4559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399181"
---
# <a name="iamtimelinetrackinsertspace-method"></a>Метод Иамтимелинетракк:: Инсертспаце

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`InsertSpace`Метод разделяет все объекты, существующие в указанное время, и вставляет между ними пробелы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ртстарт* 
</dt> <dd>

Время, когда нужно создать разбиение, и начальную точку вставленного пространства в единицах измерения 100-наносекундных.

</dd> <dt>

*ртенд* 
</dt> <dd>

Конечная точка вставленного пространства в единицах измерения 100-наносекундных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные возвращаемые значения включают следующее.



| Код возврата                                                                                   | Описание                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | В указанное время нет объектов.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый аргумент.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                        |



 

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

[**Интерфейс Иамтимелинетракк**](iamtimelinetrack.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




