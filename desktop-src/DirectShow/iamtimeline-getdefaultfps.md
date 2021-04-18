---
description: 'Метод Жетдефаултфпс извлекает частоту кадров вывода по умолчанию в кадрах в секунду (кадров/с). Группы используют это значение в качестве частоты кадров по умолчанию. Чтобы задать частоту кадров группы, вызовите метод Иамтимелинеграуп:: Сетаутпутфпс в группе.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'Метод Иамтимелине:: Жетдефаултфпс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675382"
---
# <a name="iamtimelinegetdefaultfps-method"></a>Метод Иамтимелине:: Жетдефаултфпс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetDefaultFPS`Метод извлекает частоту выходного кадра по умолчанию в кадрах в секунду (кадров/с). Группы используют это значение в качестве частоты кадров по умолчанию. Чтобы задать частоту кадров группы, вызовите метод [**иамтимелинеграуп:: сетаутпутфпс**](iamtimelinegroup-setoutputfps.md) в группе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфпс* 
</dt> <dd>

Получает частоту кадров по умолчанию в кадрах в секунду.

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

[**Интерфейс Иамтимелине**](iamtimeline.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




