---
description: Запросы на отмену создания инструкций трассировки шейдера в отладочном запросе.
MS-HAID: vspixengine.IDebugShaderCancel\_CancelGenerate\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Идебугшадерканцел:: Канцелженерате'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10DA5080-3AA6-47AA-BFE7-774BC26C7F95
api_name:
- IDebugShaderCancel.CancelGenerate
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c2754f0d390960775b11ac5da121d5e6a20705a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701117"
---
# <a name="span-idvspixengineidebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptrspanidebugshadercancelcancelgenerate-method"></a><span data-ttu-id="c4b8b-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>Метод Идебугшадерканцел:: Канцелженерате</span><span class="sxs-lookup"><span data-stu-id="c4b8b-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>IDebugShaderCancel::CancelGenerate method</span></span>

<span data-ttu-id="c4b8b-104">Запросы на отмену создания инструкций трассировки шейдера в отладочном запросе.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-104">Requests to cancel generation of shader trace instructions in a debug request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b8b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4b8b-105">Syntax</span></span>


```C++
HRESULT CancelGenerate(
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory
);
```

## <a name="parameters"></a><span data-ttu-id="c4b8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4b8b-106">Parameters</span></span>

<span data-ttu-id="c4b8b-107">*рекуестинфо* </span><span class="sxs-lookup"><span data-stu-id="c4b8b-107">*requestInfo* </span></span>  
<span data-ttu-id="c4b8b-108">Адрес структуры Дебугшадеррекуестинфо, описывающей запрошенное событие/вершина или пиксель.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="c4b8b-109">*ппикселхистори* </span><span class="sxs-lookup"><span data-stu-id="c4b8b-109">*pPixelHistory* </span></span>  
<span data-ttu-id="c4b8b-110">Адрес результатов журнала пикселей, используемый для поиска связанного пикселя для отладки.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-110">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="c4b8b-111">Применяется только при отладке шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-111">Only applies when debugging a pixel shader.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4b8b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4b8b-112">Return value</span></span>

<span data-ttu-id="c4b8b-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4b8b-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4b8b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4b8b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c4b8b-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c4b8b-116">Header</span><span class="sxs-lookup"><span data-stu-id="c4b8b-116">Header</span></span></p></td><td><span data-ttu-id="c4b8b-117">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="c4b8b-117">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c4b8b-118"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="c4b8b-118"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c4b8b-119">**идебугшадерканцел**</span><span class="sxs-lookup"><span data-stu-id="c4b8b-119">**IDebugShaderCancel**</span></span>](/windows/desktop/direct3dtools/idebugshadercancel)

 

 
