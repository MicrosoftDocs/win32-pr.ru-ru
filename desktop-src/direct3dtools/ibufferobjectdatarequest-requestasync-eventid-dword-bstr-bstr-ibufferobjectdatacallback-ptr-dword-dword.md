---
description: Запросы на получение необработанного содержимого объекта (буфер, текстура, представление целевого объекта прорисовки и т. д.).
MS-HAID: vspixengine.IBufferObjectDataRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_BSTR\_IBufferObjectDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ибуфферобжектдатарекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 899954DC-6196-4F79-AFB4-5E692DAA03EC
api_name:
- IBufferObjectDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 97d35f656f373f2f0040d49a78a2c0d376bc4266
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139766"
---
# <a name="span-idvspixengineibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dwordspanibufferobjectdatarequestrequestasync-method"></a><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>Метод Ибуфферобжектдатарекуест:: Рекуестасинк

Запросы на получение необработанного содержимого объекта (буфер, текстура, представление целевого объекта прорисовки и т. д.)

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   BSTR                        Format,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a>Параметры

*1008*   
Указанное событие для сопоставления содержимого буфера с (например, целевой объект прорисовки может измениться со временем).

*рекуестеддатауид*   
Адрес указанного объекта.

*File*   
Строка COM, содержащая путь к файлу, в который записываются результаты.

*Формат*   
В настоящий момент не используется. Строка COM, указывающая формат вывода.

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

[**ибуфферобжектдатарекуест**](/windows/desktop/direct3dtools/ibufferobjectdatarequest)

 

 
