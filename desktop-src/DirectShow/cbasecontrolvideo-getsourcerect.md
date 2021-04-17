---
description: Метод Жетсаурцерект извлекает исходный прямоугольник. Это внутренний метод.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Кбасеконтролвидео. Жетсаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e57a5beda7b147e952ecbb26c96df5f7e372e6d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685406"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a><span data-ttu-id="29201-104">Кбасеконтролвидео. Жетсаурцерект, метод</span><span class="sxs-lookup"><span data-stu-id="29201-104">CBaseControlVideo.GetSourceRect method</span></span>

<span data-ttu-id="29201-105">`GetSourceRect`Метод получает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="29201-105">The `GetSourceRect` method retrieves the source rectangle.</span></span> <span data-ttu-id="29201-106">Это внутренний метод.</span><span class="sxs-lookup"><span data-stu-id="29201-106">This is an internal method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29201-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29201-107">Syntax</span></span>


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="29201-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="29201-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29201-109">*псаурцерект*</span><span class="sxs-lookup"><span data-stu-id="29201-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="29201-110">Указатель на полученный исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="29201-110">Pointer to the retrieved source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29201-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29201-111">Return value</span></span>

<span data-ttu-id="29201-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29201-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29201-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29201-113">Remarks</span></span>

<span data-ttu-id="29201-114">Эта функция члена должна быть переопределена в производном классе для возврата исходного прямоугольника, удерживаемого модулем подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="29201-114">This member function must be overridden in the derived class to return the source rectangle held by the video renderer.</span></span> <span data-ttu-id="29201-115">Он вызывается из следующих функций-членов [**кбасеконтролвидео**](cbasecontrolvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="29201-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="29201-116">**Кбасеконтролвидео:: Жетсаурцепоситион**</span><span class="sxs-lookup"><span data-stu-id="29201-116">**CBaseControlVideo::GetSourcePosition**</span></span>](cbasecontrolvideo-getsourceposition.md)
-   [<span data-ttu-id="29201-117">**Кбасеконтролвидео::p UT \_ саурцелефт**</span><span class="sxs-lookup"><span data-stu-id="29201-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="29201-118">**Кбасеконтролвидео:: Get \_ саурцелефт**</span><span class="sxs-lookup"><span data-stu-id="29201-118">**CBaseControlVideo::get\_SourceLeft**</span></span>](cbasecontrolvideo-get-sourceleft.md)
-   [<span data-ttu-id="29201-119">**Кбасеконтролвидео::p UT \_ саурцевидс**</span><span class="sxs-lookup"><span data-stu-id="29201-119">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="29201-120">**Кбасеконтролвидео:: Get \_ саурцевидс**</span><span class="sxs-lookup"><span data-stu-id="29201-120">**CBaseControlVideo::get\_SourceWidth**</span></span>](cbasecontrolvideo-get-sourcewidth.md)
-   [<span data-ttu-id="29201-121">**Кбасеконтролвидео::p UT \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="29201-121">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="29201-122">**Кбасеконтролвидео:: Get \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="29201-122">**CBaseControlVideo::get\_SourceTop**</span></span>](cbasecontrolvideo-get-sourcetop.md)
-   [<span data-ttu-id="29201-123">**Кбасеконтролвидео::p UT \_ саурцехеигхт**</span><span class="sxs-lookup"><span data-stu-id="29201-123">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)
-   [<span data-ttu-id="29201-124">**Кбасеконтролвидео:: Get \_ саурцехеигхт**</span><span class="sxs-lookup"><span data-stu-id="29201-124">**CBaseControlVideo::get\_SourceHeight**</span></span>](cbasecontrolvideo-get-sourceheight.md)

<span data-ttu-id="29201-125">В следующем примере демонстрируется реализация этой функции в производном классе.</span><span class="sxs-lookup"><span data-stu-id="29201-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="29201-126">В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="29201-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="29201-127">Требования</span><span class="sxs-lookup"><span data-stu-id="29201-127">Requirements</span></span>



| <span data-ttu-id="29201-128">Требование</span><span class="sxs-lookup"><span data-stu-id="29201-128">Requirement</span></span> | <span data-ttu-id="29201-129">Значение</span><span class="sxs-lookup"><span data-stu-id="29201-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29201-130">Header</span><span class="sxs-lookup"><span data-stu-id="29201-130">Header</span></span><br/>  | <dl> <span data-ttu-id="29201-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29201-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="29201-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="29201-132">Library</span></span><br/> | <dl> <span data-ttu-id="29201-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="29201-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29201-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29201-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29201-135">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="29201-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




