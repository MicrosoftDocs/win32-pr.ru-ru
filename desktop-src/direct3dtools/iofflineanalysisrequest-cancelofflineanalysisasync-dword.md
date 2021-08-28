---
description: Запросы на отмену автономного анализа в запросе автономного анализа.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_CancelOfflineAnalysisAsync\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иоффлинеаналисисрекуест:: Канцелоффлинеаналисисасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 20107890-DF7B-4483-9D2C-1D9164366504
api_name:
- IOfflineAnalysisRequest.CancelOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 759210c31112dd19400709aa603b01b0cae3da0f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623750"
---
# <a name="span-idvspixengineiofflineanalysisrequest_cancelofflineanalysisasync_dwordspaniofflineanalysisrequestcancelofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>Метод Иоффлинеаналисисрекуест:: Канцелоффлинеаналисисасинк

Запросы на отмену автономного анализа в запросе автономного анализа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CancelOfflineAnalysisAsync(
   DWORD cookie
);
```

## <a name="parameters"></a>Параметры

*"*   
Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иоффлинеаналисисрекуест**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
