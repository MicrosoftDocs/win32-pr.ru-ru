---
description: Метод Сетмедиатипефорвб задает тип носителя группы для клиентов автоматизации.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'Метод Иамтимелинеграуп:: Сетмедиатипефорвб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ea47e4edcdfc58e38e61a9f92eb5afac0092ab0cb445f6ff73471e1b65b1480b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905044"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a>Метод Иамтимелинеграуп:: Сетмедиатипефорвб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetMediaTypeForVB`Метод задает тип носителя группы для клиентов автоматизации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Val* \[ окне\]
</dt> <dd>

Значение, указывающее тип носителя. Установите значение 0 для параметра видео или 1 для звукового сигнала.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод предназначен для клиентов автоматизации. Для приложений C++ используйте метод [**иамтимелинеграуп:: сетмедиатипе**](iamtimelinegroup-setmediatype.md) .

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

[**Интерфейс Иамтимелинеграуп**](iamtimelinegroup.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




