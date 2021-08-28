---
description: Запрашивает запуск сеанса отладки шейдера для указанного этапа конвейера, точки или вершины, если применимо, событие и кадр.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Идебугшадеррекуест:: Бегиндебугшадер'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 20e9667ba0c0d4d36175cd9694c2e6b57d192fab
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629858"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>Метод Идебугшадеррекуест:: Бегиндебугшадер

Запрашивает запуск сеанса отладки шейдера для указанного этапа конвейера, точки или вершины, если применимо, событие и кадр.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a>Параметры

*ерроркаллбакк*   
Адрес обратного вызова для ошибок, которые могут возникнуть во время отладки.

*1008*   
Указанное событие.

*фраменумбер*   
Указанный кадр.

*положений*   
Указанная вершина. Применяется только при отладке шейдера вершин.

*растров*   
Указанный пиксель. Применяется только при отладке шейдера пикселей.

*Backstage*   
Указанная стадия конвейера.

*ппикселхистори*   
Адрес результатов журнала пикселей, используемый для поиска связанного пикселя для отладки. Применяется только при отладке шейдера пикселей.

*пдевице*   
Адрес, который необходимо передать модулю отладки для взаимодействия с этим сеансом отладки (реадпроцессмемори отладчика по этому адресу).

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**идебугшадеррекуест**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
