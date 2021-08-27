---
description: Запросы на получение сведений о столбцах (полях), поддерживаемых типом запроса этой таблицы объектов.
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иобжекттаблерекуест:: Рекуестсуппортедколумнсасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bfdf3b488296cf0092f59d4b944c39e00df45e31
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629587"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>Метод Иобжекттаблерекуест:: Рекуестсуппортедколумнсасинк

Запросы на получение сведений о столбцах (полях), поддерживаемых типом запроса этой таблицы объектов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иобжекттаблерекуест**](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
