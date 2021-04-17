---
description: Обратный вызов, уведомляющий узел о том, какие этапы конвейера используются вызовом Draw запроса связана.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажескаллбакк:: Жетсуппортедстажес'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c55c7f8bfa6b5b69ea2a46dd6023021a6b4ab6c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537004"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>Метод Ипипелинестажескаллбакк:: Жетсуппортедстажес

Обратный вызов, уведомляющий узел о том, какие этапы конвейера используются вызовом Draw запроса связана.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a>Параметры

*нумколумнс*   
Число возвращенных стадий.

*count0 \_ пстажес*   
Этапы конвейера.

*свапчаинвидс*   
Ширина цепочки подкачки, связана с вызовом Draw. Используется при запросе изображений предварительного просмотра конвейера.

*свапчаинхеигхт*   
Высота цепочки подкачки, связана с вызовом Draw. Используется при запросе изображений предварительного просмотра конвейера.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипипелинестажескаллбакк**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
