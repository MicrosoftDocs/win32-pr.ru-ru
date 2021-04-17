---
description: Метод конструктора.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Конструктор Кбасерендерер. Кбасерендерер (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41f8d7f9681a64f58413aea2fd8717320278f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657484"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="a8845-103">Кбасерендерер. Кбасерендерер, конструктор</span><span class="sxs-lookup"><span data-stu-id="a8845-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="a8845-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="a8845-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8845-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8845-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="a8845-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8845-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8845-107">*рендеркласс*</span><span class="sxs-lookup"><span data-stu-id="a8845-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="a8845-108">Идентификатор класса модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="a8845-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="a8845-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="a8845-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a8845-110">Указатель на строку, содержащую имя фильтра, для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="a8845-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="a8845-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="a8845-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a8845-112">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="a8845-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="a8845-113">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="a8845-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="a8845-114">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a8845-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a8845-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="a8845-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="a8845-116">Получает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8845-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="a8845-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="a8845-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="a8845-118">Разрешение таймера.</span><span class="sxs-lookup"><span data-stu-id="a8845-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8845-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a8845-119">Requirements</span></span>



| <span data-ttu-id="a8845-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a8845-120">Requirement</span></span> | <span data-ttu-id="a8845-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a8845-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8845-122">Header</span><span class="sxs-lookup"><span data-stu-id="a8845-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a8845-123"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8845-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8845-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a8845-124">Library</span></span><br/> | <dl> <span data-ttu-id="a8845-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a8845-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8845-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8845-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8845-127">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="a8845-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




