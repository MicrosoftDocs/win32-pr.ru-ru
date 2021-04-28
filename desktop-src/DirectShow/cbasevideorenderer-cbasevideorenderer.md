---
description: Метод конструктора Кбасевидеорендерер. Кбасевидеорендерер.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Конструктор Кбасевидеорендерер. Кбасевидеорендерер (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095842"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="1e810-103">Кбасевидеорендерер. Кбасевидеорендерер, конструктор</span><span class="sxs-lookup"><span data-stu-id="1e810-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="1e810-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="1e810-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e810-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e810-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="1e810-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e810-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e810-107">*рендеркласс*</span><span class="sxs-lookup"><span data-stu-id="1e810-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="1e810-108">Идентификатор класса для этого модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="1e810-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="1e810-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="1e810-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1e810-110">Указатель на описание, используемое в целях отладки.</span><span class="sxs-lookup"><span data-stu-id="1e810-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="1e810-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="1e810-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1e810-112">Указатель на обобщенный объект Owner.</span><span class="sxs-lookup"><span data-stu-id="1e810-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="1e810-113">*фр*</span><span class="sxs-lookup"><span data-stu-id="1e810-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1e810-114">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e810-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e810-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1e810-115">Requirements</span></span>



| <span data-ttu-id="1e810-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1e810-116">Requirement</span></span> | <span data-ttu-id="1e810-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1e810-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e810-118">Header</span><span class="sxs-lookup"><span data-stu-id="1e810-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1e810-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e810-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1e810-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e810-120">Library</span></span><br/> | <dl> <span data-ttu-id="1e810-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1e810-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e810-122">См. также</span><span class="sxs-lookup"><span data-stu-id="1e810-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e810-123">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="1e810-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




