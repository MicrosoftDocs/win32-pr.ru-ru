---
description: Асинхронный запрос на получение изображений предварительного просмотра для окна "Этапы графического конвейера".
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажесрекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 62211a838470807d674671cb8b8ff886d62a4408
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626830"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>Метод Ипипелинестажесрекуест:: Рекуестасинк

Асинхронный запрос на получение изображений предварительного просмотра для окна "Этапы графического конвейера".

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a>Параметры

*1008*   
Идентификатор события графики, для которого запрашиваются изображения.

*нумстажес*   
Число стадий конвейера, для которых запрашиваются образы.

*count1 \_ стажеидс*   
Идентификаторы этапов конвейера, для которых запрашиваются образы.

*Ширина*   
Ширина запрошенных изображений.

*равно*   
Высота запрошенных изображений.

*рекуесткаллбакк*   
Адрес обратного вызова, используемый для уведомления узла о результатах.

*жетмешдата*   
значение true, чтобы вернуть данные сетки; в противном случае — false.

*рекуесткукие*   
Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.

*прогрессинтервалмсекс*   
Не используется.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипипелинестажесрекуест**](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
