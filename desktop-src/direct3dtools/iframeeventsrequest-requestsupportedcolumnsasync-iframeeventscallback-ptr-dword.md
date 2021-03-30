---
description: Асинхронный запрос для получения сведений о том, какие столбцы (поля) Этот тип запроса событий фрейма поддерживает.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestSupportedColumnsAsync\_IFrameEventsCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамивентсрекуест:: Рекуестсуппортедколумнсасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8F8ED8F7-F764-4CC8-891B-F0582F6B1337
api_name:
- IFrameEventsRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 13d4c797e338f6b0901781760a39511a1f136174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806197"
---
# <a name="span-idvspixengineiframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dwordspaniframeeventsrequestrequestsupportedcolumnsasync-method"></a><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>Метод Ифрамивентсрекуест:: Рекуестсуппортедколумнсасинк

Асинхронный запрос для получения сведений о том, какие столбцы (поля) Этот тип запроса событий фрейма поддерживает.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestSupportedColumnsAsync(
   IFrameEventsCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a>Параметры

*рекуесткаллбакк*   
Адрес обратного вызова, используемый для уведомления узла о результатах.

*прогрессинтервалмсекс*   
Не используется.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ифрамивентсрекуест**](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
