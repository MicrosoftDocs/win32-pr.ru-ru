---
description: Функция обратного вызова, используемая для уведомления узла о завершении считывания значения шаг текселя.
MS-HAID: vspixengine.IPixEngine5Callbacks\_ReadTexelValueComplete\_UINT\_BSTR\_arr\_double\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5Callbacks:: Реадтекселвалуекомплете'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAC08D8-0E4F-40B5-B91C-5C9159665C96
api_name:
- IPixEngine5Callbacks.ReadTexelValueComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7069d286cf65d87ba7bf4c576de3692b2a51d1a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537577"
---
# <a name="span-idvspixengineipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arrspanipixengine5callbacksreadtexelvaluecomplete-method"></a><span data-ttu-id="c1611-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>Метод IPixEngine5Callbacks:: Реадтекселвалуекомплете</span><span class="sxs-lookup"><span data-stu-id="c1611-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>IPixEngine5Callbacks::ReadTexelValueComplete method</span></span>

<span data-ttu-id="c1611-104">Функция обратного вызова, используемая для уведомления узла о завершении считывания значения шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="c1611-104">A callback function used to notify the host when a texel value read has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1611-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1611-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueComplete(
   UINT      numChannels,
   BSTR []   count0_channelNames,
   double [] count0_channelValues
);
```

## <a name="parameters"></a><span data-ttu-id="c1611-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1611-106">Parameters</span></span>

<span data-ttu-id="c1611-107">*нумчаннелс* </span><span class="sxs-lookup"><span data-stu-id="c1611-107">*numChannels* </span></span>  
<span data-ttu-id="c1611-108">Число каналов, которые имеет шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="c1611-108">The number of channels the texel has.</span></span>

<span data-ttu-id="c1611-109">*count0 \_ чаннелнамес* </span><span class="sxs-lookup"><span data-stu-id="c1611-109">*count0\_channelNames* </span></span>  
<span data-ttu-id="c1611-110">Строки COM, содержащие имена каналов.</span><span class="sxs-lookup"><span data-stu-id="c1611-110">COM strings containing the names of the channels.</span></span>

<span data-ttu-id="c1611-111">*count0 \_ чаннелвалуес* </span><span class="sxs-lookup"><span data-stu-id="c1611-111">*count0\_channelValues* </span></span>  
<span data-ttu-id="c1611-112">Значения каналов.</span><span class="sxs-lookup"><span data-stu-id="c1611-112">The values of the channels.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1611-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1611-113">Return value</span></span>

<span data-ttu-id="c1611-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c1611-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c1611-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1611-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1611-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c1611-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c1611-117">Header</span><span class="sxs-lookup"><span data-stu-id="c1611-117">Header</span></span></p></td><td><span data-ttu-id="c1611-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="c1611-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c1611-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="c1611-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c1611-120">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="c1611-120">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
