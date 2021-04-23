---
description: Запросы на запуск отладки указанного списка инструкций.
MS-HAID: vspixengine.IDebugShaderRequest2\_BeginDebugShader\_IPixErrorCallback\_ptr\_DWORD\_BYTE\_arr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IDebugShaderRequest2:: Бегиндебугшадер'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B454D673-C14F-4A8F-9DA7-2C47510BE5DA
api_name:
- IDebugShaderRequest2.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39f6749a233140b745097bc1270963e50d0f11fb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140071"
---
# <a name="span-idvspixengineidebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptrspanidebugshaderrequest2begindebugshader-method"></a><span data-ttu-id="457df-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>Метод IDebugShaderRequest2:: Бегиндебугшадер</span><span class="sxs-lookup"><span data-stu-id="457df-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2::BeginDebugShader method</span></span>

<span data-ttu-id="457df-104">Запросы на запуск отладки указанного списка инструкций.</span><span class="sxs-lookup"><span data-stu-id="457df-104">Requests to start debugging the specified list of instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="457df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="457df-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback * errorCallback,
   DWORD               instructionStreamSize,
   BYTE []             count1_instructionStream,
   DWORD *             pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="457df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="457df-106">Parameters</span></span>

<span data-ttu-id="457df-107">*ерроркаллбакк* </span><span class="sxs-lookup"><span data-stu-id="457df-107">*errorCallback* </span></span>  
<span data-ttu-id="457df-108">Адрес обратного вызова для ошибок, которые могут возникнуть во время отладки.</span><span class="sxs-lookup"><span data-stu-id="457df-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="457df-109">*инструктионстреамсизе* </span><span class="sxs-lookup"><span data-stu-id="457df-109">*instructionStreamSize* </span></span>  
<span data-ttu-id="457df-110">Количество инструкций в потоке инструкций.</span><span class="sxs-lookup"><span data-stu-id="457df-110">The number of instructions in the instruction stream.</span></span>

<span data-ttu-id="457df-111">*count1 \_ инструктионстреам* </span><span class="sxs-lookup"><span data-stu-id="457df-111">*count1\_instructionStream* </span></span>  
<span data-ttu-id="457df-112">Указанный поток инструкций.</span><span class="sxs-lookup"><span data-stu-id="457df-112">The specified instruction stream.</span></span>

<span data-ttu-id="457df-113">*пдевице* </span><span class="sxs-lookup"><span data-stu-id="457df-113">*pDevice* </span></span>  
<span data-ttu-id="457df-114">Адрес, который необходимо передать модулю отладки для взаимодействия с этим сеансом отладки (реадпроцессмемори отладчика по этому адресу).</span><span class="sxs-lookup"><span data-stu-id="457df-114">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="457df-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="457df-115">Return value</span></span>

<span data-ttu-id="457df-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="457df-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="457df-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="457df-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="457df-118">Требования</span><span class="sxs-lookup"><span data-stu-id="457df-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="457df-119">Header</span><span class="sxs-lookup"><span data-stu-id="457df-119">Header</span></span></p></td><td><span data-ttu-id="457df-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="457df-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="457df-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="457df-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="457df-122">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="457df-122">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
