---
description: 'Метод Сетдефаултфпс задает частоту выходного кадра по умолчанию в кадрах в секунду. Группы используют это значение в качестве частоты кадров по умолчанию. Чтобы задать частоту кадров группы, вызовите метод Иамтимелинеграуп:: Сетаутпутфпс в группе.'
ms.assetid: a164f4b9-fbed-45ea-9156-cc64f0b21423
title: 'Метод Иамтимелине:: Сетдефаултфпс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d98b4ea7a69f527f0a79ddbe559d3602afecd06e4728da23ef3627ed7a313a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052814"
---
# <a name="iamtimelinesetdefaultfps-method"></a>Метод Иамтимелине:: Сетдефаултфпс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetDefaultFPS`Метод задает частоту выходного кадра по умолчанию в кадрах в секунду. Группы используют это значение в качестве частоты кадров по умолчанию. Чтобы задать частоту кадров группы, вызовите метод [**иамтимелинеграуп:: сетаутпутфпс**](iamtimelinegroup-setoutputfps.md) в группе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Кадры в секунду* 
</dt> <dd>

Частота кадров по умолчанию в кадрах в секунду.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелине**](iamtimeline.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




