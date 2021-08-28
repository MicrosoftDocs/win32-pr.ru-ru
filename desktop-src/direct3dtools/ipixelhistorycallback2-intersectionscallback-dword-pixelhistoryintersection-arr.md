---
description: Обратный вызов, уведомляющий узел о размещении сведений о пересечении журнала пикселей, возвращаемых запросом связана.
MS-HAID: vspixengine.IPixelHistoryCallback2\_IntersectionsCallback\_DWORD\_PixelHistoryIntersection\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixelHistoryCallback2:: Интерсектионскаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 478B2495-93E4-4BB1-BC86-802D2AFAF97D
api_name:
- IPixelHistoryCallback2.IntersectionsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a019a0000e21cc3a6036379b8a6e9908ea52fdbb
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624500"
---
# <a name="span-idvspixengineipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arrspanipixelhistorycallback2intersectionscallback-method"></a><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>Метод IPixelHistoryCallback2:: Интерсектионскаллбакк

Обратный вызов, уведомляющий узел о размещении сведений о пересечении журнала пикселей, возвращаемых запросом связана.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IntersectionsCallback(
   DWORD                       count,
   PixelHistoryIntersection [] count0_intersections
);
```

## <a name="parameters"></a>Параметры

*расчета*   
Число пересечения в журнале пикселей.

*\_пересечения count0*   
Пересечения с журналом пикселей.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixelHistoryCallback2**](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
