---
description: Метод Жетстартстоп извлекает значения времени начала и окончания объекта относительно родителя объекта.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'Метод Иамтимелинеобж:: Жетстартстоп (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685396"
---
# <a name="iamtimelineobjgetstartstop-method"></a>Метод Иамтимелинеобж:: Жетстартстоп

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetStartStop`Метод получает значения времени начала и окончания объекта относительно родителя объекта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстарт* 
</dt> <dd>

Получает время начала (в 100-наносекундных единицах).

</dd> <dt>

*пстоп* 
</dt> <dd>

Получает время окончания в 100-наносекундных единицах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Композиции, группы и дорожки всегда имеют время начала 0.

Во время подготовки к просмотру DES округляет время начала и окончания объекта до ближайшей границы фрейма. Однако DES не перезаписывает время объекта. При изменении частоты кадров группы округленные значения всегда вычисляются исходя из исходного времени. Для получения дополнительных сведений о [времени в службах редактирования DirectShow](time-in-directshow-editing-services.md).

Чтобы определить время начала и окончания в готовом к просмотре проекте, передайте значения, возвращаемые методом, в `GetStartStop` метод [**иамтимелинеобж:: фикстимес**](iamtimelineobj-fixtimes.md) .

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

 

 




