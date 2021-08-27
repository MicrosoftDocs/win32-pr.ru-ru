---
description: Запросы на создание инструкций трассировки шейдера в отладочном запросе. Отладка на основе трассировки происходит в ЦП (деформацию), а не на GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IDebugShaderRequest2:: Женератеинструктионс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3af0e624435c03416db0bf8d74bc3aa8418ae78
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625160"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>Метод IDebugShaderRequest2:: Женератеинструктионс

Запросы на создание инструкций трассировки шейдера в отладочном запросе. Отладка на основе трассировки происходит в ЦП (деформацию), а не на GPU.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a>Параметры

*ерроркаллбакк*   
Адрес обратного вызова для ошибок, которые могут возникнуть при создании инструкций трассировки шейдера.

*рекуестинфо*   
Адрес структуры Дебугшадеррекуестинфо, описывающей запрошенное событие/вершина или пиксель.

*ппикселхистори*   
Адрес результатов журнала пикселей, используемый для поиска связанного пикселя для отладки. Применяется только при отладке шейдера пикселей.

*пкаллбакк*   
Адрес обратного вызова, используемый для уведомления узла о результатах.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
