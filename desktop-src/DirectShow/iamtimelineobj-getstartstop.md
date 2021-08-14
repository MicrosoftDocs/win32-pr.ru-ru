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
ms.openlocfilehash: d808d7ac2ee3b6c1cbeddc39c730fc38b7032bde86ce726af03379d71241679c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400790"
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

## <a name="remarks"></a>Remarks

Композиции, группы и дорожки всегда имеют время начала 0.

Во время подготовки к просмотру DES округляет время начала и окончания объекта до ближайшей границы фрейма. Однако DES не перезаписывает время объекта. При изменении частоты кадров группы округленные значения всегда вычисляются исходя из исходного времени. дополнительные сведения см. [в подDirectShow службы правки](time-in-directshow-editing-services.md).

Чтобы определить время начала и окончания в готовом к просмотре проекте, передайте значения, возвращаемые методом, в `GetStartStop` метод [**иамтимелинеобж:: фикстимес**](iamtimelineobj-fixtimes.md) .

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

[**Интерфейс Иамтимелинеобж**](iamtimelineobj.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




