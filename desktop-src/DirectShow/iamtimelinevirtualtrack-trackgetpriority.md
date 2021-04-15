---
description: Метод Траккжетприорити извлекает уровень приоритета объекта.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'Метод Иамтимелиневиртуалтракк:: Траккжетприорити (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689280"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a>Метод Иамтимелиневиртуалтракк:: Траккжетприорити

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`TrackGetPriority`Метод получает уровень приоритета объекта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пприорити* 
</dt> <dd>

Указатель на переменную, которая получает уровень приоритета. Если объект не является частью временной шкалы, для него устанавливается значение – 1.

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

[**Интерфейс Иамтимелиневиртуалтракк**](iamtimelinevirtualtrack.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




