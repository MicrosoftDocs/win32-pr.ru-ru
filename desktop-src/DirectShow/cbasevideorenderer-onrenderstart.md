---
description: Метод Онрендерстарт задает сведения для подготовки к просмотру.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Кбасевидеорендерер. Онрендерстарт, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675011"
---
# <a name="cbasevideorendereronrenderstart-method"></a><span data-ttu-id="675f1-103">Кбасевидеорендерер. Онрендерстарт, метод</span><span class="sxs-lookup"><span data-stu-id="675f1-103">CBaseVideoRenderer.OnRenderStart method</span></span>

<span data-ttu-id="675f1-104">`OnRenderStart`Метод задает сведения для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="675f1-104">The `OnRenderStart` method sets information for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="675f1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="675f1-105">Syntax</span></span>


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="675f1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="675f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="675f1-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="675f1-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="675f1-108">Указатель на пример носителя.</span><span class="sxs-lookup"><span data-stu-id="675f1-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="675f1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="675f1-109">Return value</span></span>

<span data-ttu-id="675f1-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="675f1-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="675f1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="675f1-111">Remarks</span></span>

<span data-ttu-id="675f1-112">Эта функция-член получает текущее время часов из системы и сохраняет ее в переменной-члене, используемой при завершении рисования.</span><span class="sxs-lookup"><span data-stu-id="675f1-112">This member function retrieves the current clock time from the system and stores it in a member variable to be used when the drawing is complete.</span></span> <span data-ttu-id="675f1-113">Функция также выполняет ведение журнала производительности.</span><span class="sxs-lookup"><span data-stu-id="675f1-113">The function also performs performance logging.</span></span> <span data-ttu-id="675f1-114">Эту функцию члена следует вызывать непосредственно перед началом рисования.</span><span class="sxs-lookup"><span data-stu-id="675f1-114">This member function should be called just before drawing starts.</span></span>

<span data-ttu-id="675f1-115">Эта функция члена переопределяет [**кбасерендерер:: онрендерстарт**](cbaserenderer-onrenderstart.md).</span><span class="sxs-lookup"><span data-stu-id="675f1-115">This member function overrides [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="675f1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="675f1-116">Requirements</span></span>



| <span data-ttu-id="675f1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="675f1-117">Requirement</span></span> | <span data-ttu-id="675f1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="675f1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="675f1-119">Header</span><span class="sxs-lookup"><span data-stu-id="675f1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="675f1-120"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="675f1-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="675f1-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="675f1-121">Library</span></span><br/> | <dl> <span data-ttu-id="675f1-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="675f1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="675f1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="675f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="675f1-124">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="675f1-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




