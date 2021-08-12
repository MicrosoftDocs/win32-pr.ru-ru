---
description: Функция обратного вызова, используемая для уведомления узла о завершении загрузки гистограммы.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadHistogramComplete\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5Callbacks:: Лоадхистограмкомплете'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A72DB49E-06C8-4061-9872-C4380D90EEB2
api_name:
- IPixEngine5Callbacks.LoadHistogramComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 329def1499fba39ff59842bd22d3beaf6fd3c4211050b785d5c774aaae6870fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282340"
---
# <a name="span-idvspixengineipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptrspanipixengine5callbacksloadhistogramcomplete-method"></a><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>Метод IPixEngine5Callbacks:: Лоадхистограмкомплете

Функция обратного вызова, используемая для уведомления узла о завершении загрузки гистограммы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Параметры

*отображения*   
Адрес данных гистограммы для загруженной гистограммы.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
