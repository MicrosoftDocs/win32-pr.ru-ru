---
description: Функция обратного вызова, используемая для уведомления узла о завершении загрузки гистограммы.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadHistogramComplete\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5Callbacks:: Лоадхистограмкомплете'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A72DB49E-06C8-4061-9872-C4380D90EEB2
api_name:
- IPixEngine5Callbacks.LoadHistogramComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0e468422f722a8bd549d63f34225833462856b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682282"
---
# <a name="span-idvspixengineipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptrspanipixengine5callbacksloadhistogramcomplete-method"></a><span data-ttu-id="01506-103"><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>Метод IPixEngine5Callbacks:: Лоадхистограмкомплете</span><span class="sxs-lookup"><span data-stu-id="01506-103"><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadHistogramComplete method</span></span>

<span data-ttu-id="01506-104">Функция обратного вызова, используемая для уведомления узла о завершении загрузки гистограммы.</span><span class="sxs-lookup"><span data-stu-id="01506-104">A callback function used to notify the host when a histogram load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="01506-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01506-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="01506-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01506-106">Parameters</span></span>

<span data-ttu-id="01506-107">*отображения* </span><span class="sxs-lookup"><span data-stu-id="01506-107">*histogram* </span></span>  
<span data-ttu-id="01506-108">Адрес данных гистограммы для загруженной гистограммы.</span><span class="sxs-lookup"><span data-stu-id="01506-108">The address of histogram data for the loaded histogram.</span></span>

## <a name="return-value"></a><span data-ttu-id="01506-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01506-109">Return value</span></span>

<span data-ttu-id="01506-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="01506-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01506-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01506-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="01506-112">Требования</span><span class="sxs-lookup"><span data-stu-id="01506-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="01506-113">Header</span><span class="sxs-lookup"><span data-stu-id="01506-113">Header</span></span></p></td><td><span data-ttu-id="01506-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="01506-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="01506-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="01506-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="01506-116">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="01506-116">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
