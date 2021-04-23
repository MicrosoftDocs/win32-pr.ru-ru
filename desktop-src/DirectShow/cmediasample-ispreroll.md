---
description: 'Метод Испреролл определяет, является ли этот пример примером предобразца. Образец не должен отображаться. Этот метод реализует метод Имедиасампле:: Испреролл.'
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Кмедиасампле. Испреролл, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665213"
---
# <a name="cmediasampleispreroll-method"></a><span data-ttu-id="93e94-105">Кмедиасампле. Испреролл, метод</span><span class="sxs-lookup"><span data-stu-id="93e94-105">CMediaSample.IsPreroll method</span></span>

<span data-ttu-id="93e94-106">`IsPreroll`Метод определяет, является ли этот пример примером предобразца.</span><span class="sxs-lookup"><span data-stu-id="93e94-106">The `IsPreroll` method determines if this sample is a preroll sample.</span></span> <span data-ttu-id="93e94-107">Образец не должен отображаться.</span><span class="sxs-lookup"><span data-stu-id="93e94-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="93e94-108">Этот метод реализует метод [**имедиасампле:: испреролл**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .</span><span class="sxs-lookup"><span data-stu-id="93e94-108">This method implements the [**IMediaSample::IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e94-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93e94-109">Syntax</span></span>


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a><span data-ttu-id="93e94-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="93e94-110">Parameters</span></span>

<span data-ttu-id="93e94-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="93e94-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93e94-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93e94-112">Return value</span></span>

<span data-ttu-id="93e94-113">Возвращает значение \_ ОК, если образец является примером, и \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="93e94-113">Returns S\_OK if the sample is a preroll sample, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="93e94-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93e94-114">Remarks</span></span>

<span data-ttu-id="93e94-115">Значение этого свойства указывается в переменной члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) .</span><span class="sxs-lookup"><span data-stu-id="93e94-115">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e94-116">Требования</span><span class="sxs-lookup"><span data-stu-id="93e94-116">Requirements</span></span>



| <span data-ttu-id="93e94-117">Требование</span><span class="sxs-lookup"><span data-stu-id="93e94-117">Requirement</span></span> | <span data-ttu-id="93e94-118">Значение</span><span class="sxs-lookup"><span data-stu-id="93e94-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e94-119">Header</span><span class="sxs-lookup"><span data-stu-id="93e94-119">Header</span></span><br/>  | <dl> <span data-ttu-id="93e94-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93e94-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="93e94-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="93e94-121">Library</span></span><br/> | <dl> <span data-ttu-id="93e94-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="93e94-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e94-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93e94-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e94-124">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="93e94-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




