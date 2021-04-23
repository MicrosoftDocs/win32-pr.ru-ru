---
description: Запросы на отладку шейдера на GPU (динамическая Отладка) и ЦП (Отладка на основе трассировки).
MS-HAID: vspixengine.IDebugLiveShaderRequest\_BeginDebugLiveShader\_DebugShaderRequestInfo\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Идебугливешадеррекуест:: Бегиндебугливешадер'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 805B2B68-C251-4192-85A3-F857B3F204C7
api_name:
- IDebugLiveShaderRequest.BeginDebugLiveShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b09bff6a414df620e06263e13d94c2f39e36903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806214"
---
# <a name="span-idvspixengineidebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptrspanidebugliveshaderrequestbegindebugliveshader-method"></a><span data-ttu-id="24200-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>Метод Идебугливешадеррекуест:: Бегиндебугливешадер</span><span class="sxs-lookup"><span data-stu-id="24200-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest::BeginDebugLiveShader method</span></span>

<span data-ttu-id="24200-104">Запросы на отладку шейдера на GPU (динамическая Отладка) и ЦП (Отладка на основе трассировки).</span><span class="sxs-lookup"><span data-stu-id="24200-104">Requests to debug a shader on the GPU (live debugging) vs CPU (trace-based debugging).</span></span>

## <a name="syntax"></a><span data-ttu-id="24200-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24200-105">Syntax</span></span>


```C++
HRESULT BeginDebugLiveShader(
   DebugShaderRequestInfo * requestInfo
);
```

## <a name="parameters"></a><span data-ttu-id="24200-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="24200-106">Parameters</span></span>

<span data-ttu-id="24200-107">*рекуестинфо* </span><span class="sxs-lookup"><span data-stu-id="24200-107">*requestInfo* </span></span>  
<span data-ttu-id="24200-108">Адрес структуры Дебугшадеррекуестинфо, описывающей запрошенное событие/вершина или пиксель.</span><span class="sxs-lookup"><span data-stu-id="24200-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

## <a name="return-value"></a><span data-ttu-id="24200-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24200-109">Return value</span></span>

<span data-ttu-id="24200-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="24200-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24200-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24200-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="24200-112">Требования</span><span class="sxs-lookup"><span data-stu-id="24200-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="24200-113">Header</span><span class="sxs-lookup"><span data-stu-id="24200-113">Header</span></span></p></td><td><span data-ttu-id="24200-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="24200-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="24200-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="24200-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="24200-116">**идебугливешадеррекуест**</span><span class="sxs-lookup"><span data-stu-id="24200-116">**IDebugLiveShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugliveshaderrequest)

 

 
