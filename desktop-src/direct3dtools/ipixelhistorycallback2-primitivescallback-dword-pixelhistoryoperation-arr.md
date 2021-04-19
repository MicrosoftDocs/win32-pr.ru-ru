---
description: Обратный вызов, уведомляющий узел о том, что сведения о операции примитива журнала пикселей возвращены связанным запросом.
MS-HAID: vspixengine.IPixelHistoryCallback2\_PrimitivesCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryCallback2: метод:P Римитивескаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2A67EC3B-72F2-4347-AD23-961CDE0D456F
api_name:
- IPixelHistoryCallback2.PrimitivesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8512bde1acd96ebbe132eeb91872d04ce043b44f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537922"
---
# <a name="span-idvspixengineipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arrspanipixelhistorycallback2primitivescallback-method"></a><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2: метод:P Римитивескаллбакк

Обратный вызов, уведомляющий узел о том, что сведения о операции примитива журнала пикселей возвращены связанным запросом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PrimitivesCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_primitives
);
```

## <a name="parameters"></a>Параметры

*расчета*   
Число примитивов.

*\_примитивы count0*   
Примитивы.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixelHistoryCallback2**](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
