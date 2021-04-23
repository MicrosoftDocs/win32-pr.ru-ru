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
ms.openlocfilehash: e9c1bc2f6b3f885159f21cd7e644545d7639d6b3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537547"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span data-ttu-id="1a0e0-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>Метод IDebugShaderRequest2:: Женератеинструктионс</span><span class="sxs-lookup"><span data-stu-id="1a0e0-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2::GenerateInstructions method</span></span>

<span data-ttu-id="1a0e0-105">Запросы на создание инструкций трассировки шейдера в отладочном запросе.</span><span class="sxs-lookup"><span data-stu-id="1a0e0-105">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="1a0e0-106">Отладка на основе трассировки происходит в ЦП (деформацию), а не на GPU.</span><span class="sxs-lookup"><span data-stu-id="1a0e0-106">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a0e0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a0e0-107">Syntax</span></span>


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="1a0e0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a0e0-108">Parameters</span></span>

<span data-ttu-id="1a0e0-109">*ерроркаллбакк* </span><span class="sxs-lookup"><span data-stu-id="1a0e0-109">*errorCallback* </span></span>  
<span data-ttu-id="1a0e0-110">Адрес обратного вызова для ошибок, которые могут возникнуть при создании инструкций трассировки шейдера.</span><span class="sxs-lookup"><span data-stu-id="1a0e0-110">The address of a callback for errors that might occur while generating shader trace instructions.</span></span>

<span data-ttu-id="1a0e0-111">*рекуестинфо* </span><span class="sxs-lookup"><span data-stu-id="1a0e0-111">*requestInfo* </span></span>  
<span data-ttu-id="1a0e0-112">Адрес структуры Дебугшадеррекуестинфо, описывающей запрошенное событие/вершина или пиксель.</span><span class="sxs-lookup"><span data-stu-id="1a0e0-112">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="1a0e0-113">*ппикселхистори* </span><span class="sxs-lookup"><span data-stu-id="1a0e0-113">*pPixelHistory* </span></span>  
<span data-ttu-id="1a0e0-114">Адрес результатов журнала пикселей, используемый для поиска связанного пикселя для отладки.</span><span class="sxs-lookup"><span data-stu-id="1a0e0-114">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="1a0e0-115">Применяется только при отладке шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="1a0e0-115">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="1a0e0-116">*пкаллбакк* </span><span class="sxs-lookup"><span data-stu-id="1a0e0-116">*pCallback* </span></span>  
<span data-ttu-id="1a0e0-117">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="1a0e0-117">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a0e0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a0e0-118">Return value</span></span>

<span data-ttu-id="1a0e0-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1a0e0-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a0e0-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a0e0-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a0e0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1a0e0-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1a0e0-122">Header</span><span class="sxs-lookup"><span data-stu-id="1a0e0-122">Header</span></span></p></td><td><span data-ttu-id="1a0e0-123">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="1a0e0-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1a0e0-124"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="1a0e0-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1a0e0-125">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="1a0e0-125">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
