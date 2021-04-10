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
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140074"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**идебугшадеррекуест**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
