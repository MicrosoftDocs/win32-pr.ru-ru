---
description: Метод Сетсаурцерект задает текущий исходный видеопрямоугольник (чистый виртуальный). Это внутренняя функция-член, которая вызывается при изменении исходного прямоугольника.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Кбасеконтролвидео. Сетсаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669237"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a><span data-ttu-id="81640-104">Кбасеконтролвидео. Сетсаурцерект, метод</span><span class="sxs-lookup"><span data-stu-id="81640-104">CBaseControlVideo.SetSourceRect method</span></span>

<span data-ttu-id="81640-105">`SetSourceRect`Метод задает текущий исходный видеопрямоугольник (чистый виртуальный).</span><span class="sxs-lookup"><span data-stu-id="81640-105">The `SetSourceRect` method sets the current source video rectangle (pure virtual).</span></span> <span data-ttu-id="81640-106">Это внутренняя функция-член, которая вызывается при изменении исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="81640-106">This is an internal member function that gets called when the source rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="81640-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81640-107">Syntax</span></span>


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="81640-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="81640-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81640-109">*псаурцерект*</span><span class="sxs-lookup"><span data-stu-id="81640-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="81640-110">Указатель на исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="81640-110">Pointer to the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81640-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81640-111">Return value</span></span>

<span data-ttu-id="81640-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81640-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81640-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81640-113">Remarks</span></span>

<span data-ttu-id="81640-114">Производные классы должны переопределять эту функцию члена, чтобы иметь представление об изменении исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="81640-114">Derived classes should override this member function to know when the source rectangle changes.</span></span> <span data-ttu-id="81640-115">Он вызывается из следующих функций-членов.</span><span class="sxs-lookup"><span data-stu-id="81640-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="81640-116">**Кбасеконтролвидео:: Сетсаурцепоситион**</span><span class="sxs-lookup"><span data-stu-id="81640-116">**CBaseControlVideo::SetSourcePosition**</span></span>](cbasecontrolvideo-setsourceposition.md)
-   [<span data-ttu-id="81640-117">**Кбасеконтролвидео::p UT \_ саурцелефт**</span><span class="sxs-lookup"><span data-stu-id="81640-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="81640-118">**Кбасеконтролвидео::p UT \_ саурцевидс**</span><span class="sxs-lookup"><span data-stu-id="81640-118">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="81640-119">**Кбасеконтролвидео::p UT \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="81640-119">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="81640-120">**Кбасеконтролвидео::p UT \_ саурцехеигхт**</span><span class="sxs-lookup"><span data-stu-id="81640-120">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)

<span data-ttu-id="81640-121">В следующем примере демонстрируется реализация этой функции в производном классе.</span><span class="sxs-lookup"><span data-stu-id="81640-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="81640-122">В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="81640-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="81640-123">Требования</span><span class="sxs-lookup"><span data-stu-id="81640-123">Requirements</span></span>



| <span data-ttu-id="81640-124">Требование</span><span class="sxs-lookup"><span data-stu-id="81640-124">Requirement</span></span> | <span data-ttu-id="81640-125">Значение</span><span class="sxs-lookup"><span data-stu-id="81640-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81640-126">Header</span><span class="sxs-lookup"><span data-stu-id="81640-126">Header</span></span><br/>  | <dl> <span data-ttu-id="81640-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81640-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81640-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81640-128">Library</span></span><br/> | <dl> <span data-ttu-id="81640-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="81640-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81640-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81640-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81640-131">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="81640-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




