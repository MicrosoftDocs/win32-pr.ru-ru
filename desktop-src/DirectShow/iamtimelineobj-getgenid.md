---
description: Метод Жетженид извлекает созданный идентификатор объекта. Идентификатор является зарезервированным числом; приложения не должны его использовать.
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'Метод Иамтимелинеобж:: Жетженид (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3497777d25c9a81d4334f1979ce33f351111ed4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679667"
---
# <a name="iamtimelineobjgetgenid-method"></a>Метод Иамтимелинеобж:: Жетженид

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetGenID`Метод получает созданный идентификатор объекта. Идентификатор является зарезервированным числом; приложения не должны его использовать.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pVal* 
</dt> <dd>

Получает созданный идентификатор.

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

 

 




