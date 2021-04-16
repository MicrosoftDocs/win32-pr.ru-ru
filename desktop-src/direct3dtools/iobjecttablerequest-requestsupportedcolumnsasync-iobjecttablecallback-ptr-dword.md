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
ms.openlocfilehash: 6773a69061e7a17d2271e1a53f89f6f2def1a6c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538213"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иобжекттаблерекуест**](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
