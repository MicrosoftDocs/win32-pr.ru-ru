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
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span data-ttu-id="70196-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>Метод Идебугшадеррекуест:: Бегиндебугшадер</span><span class="sxs-lookup"><span data-stu-id="70196-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest::BeginDebugShader method</span></span>

<span data-ttu-id="70196-104">Запрашивает запуск сеанса отладки шейдера для указанного этапа конвейера, точки или вершины, если применимо, событие и кадр.</span><span class="sxs-lookup"><span data-stu-id="70196-104">Requests to start a shader debugging session for the specified pipeline stage, pixel/vertex if applicable, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="70196-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70196-105">Syntax</span></span>


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

## <a name="parameters"></a><span data-ttu-id="70196-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70196-106">Parameters</span></span>

<span data-ttu-id="70196-107">*ерроркаллбакк* </span><span class="sxs-lookup"><span data-stu-id="70196-107">*errorCallback* </span></span>  
<span data-ttu-id="70196-108">Адрес обратного вызова для ошибок, которые могут возникнуть во время отладки.</span><span class="sxs-lookup"><span data-stu-id="70196-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="70196-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="70196-109">*eventID* </span></span>  
<span data-ttu-id="70196-110">Указанное событие.</span><span class="sxs-lookup"><span data-stu-id="70196-110">The specified event.</span></span>

<span data-ttu-id="70196-111">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="70196-111">*frameNumber* </span></span>  
<span data-ttu-id="70196-112">Указанный кадр.</span><span class="sxs-lookup"><span data-stu-id="70196-112">The specified frame.</span></span>

<span data-ttu-id="70196-113">*положений* </span><span class="sxs-lookup"><span data-stu-id="70196-113">*vertex* </span></span>  
<span data-ttu-id="70196-114">Указанная вершина.</span><span class="sxs-lookup"><span data-stu-id="70196-114">The specified vertex.</span></span> <span data-ttu-id="70196-115">Применяется только при отладке шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="70196-115">Only applies when debugging a vertex shader.</span></span>

<span data-ttu-id="70196-116">*растров* </span><span class="sxs-lookup"><span data-stu-id="70196-116">*pixel* </span></span>  
<span data-ttu-id="70196-117">Указанный пиксель.</span><span class="sxs-lookup"><span data-stu-id="70196-117">The specified pixel.</span></span> <span data-ttu-id="70196-118">Применяется только при отладке шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="70196-118">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="70196-119">*Backstage* </span><span class="sxs-lookup"><span data-stu-id="70196-119">*stage* </span></span>  
<span data-ttu-id="70196-120">Указанная стадия конвейера.</span><span class="sxs-lookup"><span data-stu-id="70196-120">The specified pipeline stage.</span></span>

<span data-ttu-id="70196-121">*ппикселхистори* </span><span class="sxs-lookup"><span data-stu-id="70196-121">*pPixelHistory* </span></span>  
<span data-ttu-id="70196-122">Адрес результатов журнала пикселей, используемый для поиска связанного пикселя для отладки.</span><span class="sxs-lookup"><span data-stu-id="70196-122">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="70196-123">Применяется только при отладке шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="70196-123">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="70196-124">*пдевице* </span><span class="sxs-lookup"><span data-stu-id="70196-124">*pDevice* </span></span>  
<span data-ttu-id="70196-125">Адрес, который необходимо передать модулю отладки для взаимодействия с этим сеансом отладки (реадпроцессмемори отладчика по этому адресу).</span><span class="sxs-lookup"><span data-stu-id="70196-125">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="70196-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70196-126">Return value</span></span>

<span data-ttu-id="70196-127">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="70196-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="70196-128">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70196-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="70196-129">Требования</span><span class="sxs-lookup"><span data-stu-id="70196-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="70196-130">Header</span><span class="sxs-lookup"><span data-stu-id="70196-130">Header</span></span></p></td><td><span data-ttu-id="70196-131">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="70196-131">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="70196-132"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="70196-132"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="70196-133">**идебугшадеррекуест**</span><span class="sxs-lookup"><span data-stu-id="70196-133">**IDebugShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
