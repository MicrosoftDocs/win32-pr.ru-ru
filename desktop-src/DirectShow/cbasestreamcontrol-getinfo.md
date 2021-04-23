---
description: Метод "info" извлекает сведения о текущих параметрах управления потоком, включая время начала и окончания. Этот метод реализует метод Иамстреамконтрол::/info.
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Метод Кбасестреамконтрол. info (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669131"
---
# <a name="cbasestreamcontrolgetinfo-method"></a><span data-ttu-id="2ce4b-104">Кбасестреамконтрол. info, метод</span><span class="sxs-lookup"><span data-stu-id="2ce4b-104">CBaseStreamControl.GetInfo method</span></span>

<span data-ttu-id="2ce4b-105">`GetInfo`Метод получает сведения о текущих параметрах управления потоком, включая время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="2ce4b-105">The `GetInfo` method retrieves information about the current stream-control settings, including the start and stop times.</span></span> <span data-ttu-id="2ce4b-106">Этот метод реализует метод [**иамстреамконтрол::/info**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="2ce4b-106">This method implements the [**IAMStreamControl::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce4b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ce4b-107">Syntax</span></span>


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2ce4b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ce4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce4b-109">*пинфо*</span><span class="sxs-lookup"><span data-stu-id="2ce4b-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2ce4b-110">Указатель на структуру [**\_ \_ сведений о потоке AM**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) , выделенную вызывающей стороной, которая получает текущие параметры управления потоком.</span><span class="sxs-lookup"><span data-stu-id="2ce4b-110">Pointer to an [**AM\_STREAM\_INFO**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) structure, allocated by the caller, that receives the current stream-control settings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce4b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ce4b-111">Return value</span></span>

<span data-ttu-id="2ce4b-112">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="2ce4b-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce4b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2ce4b-113">Requirements</span></span>



| <span data-ttu-id="2ce4b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2ce4b-114">Requirement</span></span> | <span data-ttu-id="2ce4b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2ce4b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce4b-116">Header</span><span class="sxs-lookup"><span data-stu-id="2ce4b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2ce4b-117"><dt>Стрмктл. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce4b-117"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2ce4b-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ce4b-118">Library</span></span><br/> | <dl> <span data-ttu-id="2ce4b-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce4b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce4b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ce4b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce4b-121">**Класс Кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="2ce4b-121">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




