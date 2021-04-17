---
description: Асинхронный запрос для получения сводных сведений о журнале графики.
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исуммарирекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A33798E3-7332-4582-A7B1-B0F9FB694872
api_name:
- ISummaryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c716545de275250efcae56a6be39c8b620ed014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710650"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>Метод Исуммарирекуест:: Рекуестасинк

Асинхронный запрос для получения сводных сведений о журнале графики.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestAsync(
   iSummaryCallback * requestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a>Параметры

*рекуесткаллбакк*   
Адрес обратного вызова, используемый для уведомления узла о результатах.

*рекуесткукие*   
Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.

*прогрессинтервалмсекс*   
Не используется.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**исуммарирекуест**](/windows/desktop/direct3dtools/isummaryrequest)

 

 
