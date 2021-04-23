---
description: Обратный вызов, уведомляющий узел о инструктрион данных, возвращаемых связанным запросом.
MS-HAID: vspixengine.IDebugShaderCallback\_ResultInstructions\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Идебугшадеркаллбакк:: Ресултинструктионс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 52440CE4-561C-4808-BE6A-B25A84BA5729
api_name:
- IDebugShaderCallback.ResultInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63dfd0e3b2b4ec7bd765e5fc0c85835f2a3ce102
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495216"
---
# <a name="span-idvspixengineidebugshadercallback_resultinstructions_dword_byte_arrspanidebugshadercallbackresultinstructions-method"></a><span data-ttu-id="73848-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>Метод Идебугшадеркаллбакк:: Ресултинструктионс</span><span class="sxs-lookup"><span data-stu-id="73848-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>IDebugShaderCallback::ResultInstructions method</span></span>

<span data-ttu-id="73848-104">Обратный вызов, уведомляющий узел о инструктрион данных, возвращаемых связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="73848-104">A callback that notifies the host of instructrion information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="73848-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73848-105">Syntax</span></span>


```C++
HRESULT ResultInstructions(
   DWORD   instructionStreamSize,
   BYTE [] count0_instructionStream
);
```

## <a name="parameters"></a><span data-ttu-id="73848-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73848-106">Parameters</span></span>

<span data-ttu-id="73848-107">*инструктионстреамсизе* </span><span class="sxs-lookup"><span data-stu-id="73848-107">*instructionStreamSize* </span></span>  
<span data-ttu-id="73848-108">Количество инструкций.</span><span class="sxs-lookup"><span data-stu-id="73848-108">The number of instructions.</span></span>

<span data-ttu-id="73848-109">*count0 \_ инструктионстреам* </span><span class="sxs-lookup"><span data-stu-id="73848-109">*count0\_instructionStream* </span></span>  
<span data-ttu-id="73848-110">Инструкции.</span><span class="sxs-lookup"><span data-stu-id="73848-110">The instructions.</span></span>

## <a name="return-value"></a><span data-ttu-id="73848-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73848-111">Return value</span></span>

<span data-ttu-id="73848-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="73848-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73848-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73848-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73848-114">Требования</span><span class="sxs-lookup"><span data-stu-id="73848-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="73848-115">Header</span><span class="sxs-lookup"><span data-stu-id="73848-115">Header</span></span></p></td><td><span data-ttu-id="73848-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="73848-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="73848-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="73848-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="73848-118">**идебугшадеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="73848-118">**IDebugShaderCallback**</span></span>](/windows/desktop/direct3dtools/idebugshadercallback)

 

 
