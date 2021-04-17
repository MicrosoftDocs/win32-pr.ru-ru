---
description: Функция обратного вызова, используемая для уведомления узла о сводных данных журнала графики.
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исуммарикаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710651"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>Метод Исуммарикаллбакк:: Ресулткаллбакк

Функция обратного вызова, используемая для уведомления узла о сводных данных журнала графики.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a>Параметры

*расчета*   
Число возвращаемых элементов сводных данных.

*count0 \_ суммаритем*   
Элементы сводных данных (пары «ключ-значение»).

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**исуммарикаллбакк**](/windows/desktop/direct3dtools/isummarycallback)

 

 
