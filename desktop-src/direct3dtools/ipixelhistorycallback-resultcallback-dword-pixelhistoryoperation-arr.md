---
description: Обратный вызов, уведомляющий узел о результатах запроса журнала пикселей.
MS-HAID: vspixengine.IPixelHistoryCallback\_ResultCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипикселхисторикаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1F7D0EA5-402A-49C4-A83E-91596AE9536B
api_name:
- IPixelHistoryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c5af9e88bde60121e8cbc78863b631c4cd41305
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622370"
---
# <a name="span-idvspixengineipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arrspanipixelhistorycallbackresultcallback-method"></a><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>Метод Ипикселхисторикаллбакк:: Ресулткаллбакк

Обратный вызов, уведомляющий узел о результатах запроса журнала пикселей.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_pixelHistoryOperation
);
```

## <a name="parameters"></a>Параметры

*расчета*   
Число результатов.

*count0 \_ пикселхисторйоператион*   
Результаты.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипикселхисторикаллбакк**](/windows/desktop/direct3dtools/ipixelhistorycallback)

 

 
