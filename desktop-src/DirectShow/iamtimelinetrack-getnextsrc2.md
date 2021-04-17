---
description: 'Метод GetNextSrc2 ищет в дорожке следующий источник, который отображается в указанное время или позже. Этот метод эквивалентен Иамтимелинетракк:: Жетнекстсрк, но принимает значение РЕФТИМЕ.'
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'Метод Иамтимелинетракк:: GetNextSrc2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685242"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>Метод Иамтимелинетракк:: GetNextSrc2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetNextSrc2`Метод выполняет поиск следующего источника, который отображается в указанном времени или более поздней версии, в дорожке. Этот метод эквивалентен [**иамтимелинетракк:: жетнекстсрк**](iamtimelinetrack-getnextsrc.md), но принимает значение [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппсрк* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) исходного объекта.

</dd> <dt>

*\Sub* 
</dt> <dd>

В поле входные данные содержит время начала поиска в секундах. Если метод получает источник, ему присваивается значение времени окончания источника. Если метод не получает источник, значение станет недопустимым и приложение не должно его использовать.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК, если метод получает источник, или \_ false в противном случае.

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

 

 




