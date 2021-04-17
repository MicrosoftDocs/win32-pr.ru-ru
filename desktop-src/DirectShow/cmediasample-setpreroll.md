---
description: 'Метод Сетпреролл указывает, является ли этот пример примером предобразца. Образец не должен отображаться. Этот метод реализует метод Имедиасампле:: Сетпреролл.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Кмедиасампле. Сетпреролл, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674978"
---
# <a name="cmediasamplesetpreroll-method"></a><span data-ttu-id="eb22f-105">Кмедиасампле. Сетпреролл, метод</span><span class="sxs-lookup"><span data-stu-id="eb22f-105">CMediaSample.SetPreroll method</span></span>

<span data-ttu-id="eb22f-106">`SetPreroll`Метод указывает, является ли этот пример примером предобразца.</span><span class="sxs-lookup"><span data-stu-id="eb22f-106">The `SetPreroll` method specifies whether this sample is a preroll sample.</span></span> <span data-ttu-id="eb22f-107">Образец не должен отображаться.</span><span class="sxs-lookup"><span data-stu-id="eb22f-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="eb22f-108">Этот метод реализует метод [**имедиасампле:: сетпреролл**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .</span><span class="sxs-lookup"><span data-stu-id="eb22f-108">This method implements the [**IMediaSample::SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb22f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb22f-109">Syntax</span></span>


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="eb22f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb22f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb22f-111">*биспреролл*</span><span class="sxs-lookup"><span data-stu-id="eb22f-111">*bIsPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="eb22f-112">Логическое значение, указывающее, является ли этот пример примером.</span><span class="sxs-lookup"><span data-stu-id="eb22f-112">Boolean value that specifies whether this is a preroll sample.</span></span> <span data-ttu-id="eb22f-113">Если **значение равно true**, это пример предобразца.</span><span class="sxs-lookup"><span data-stu-id="eb22f-113">If **TRUE**, this is a preroll sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb22f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb22f-114">Return value</span></span>

<span data-ttu-id="eb22f-115">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="eb22f-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb22f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb22f-116">Remarks</span></span>

<span data-ttu-id="eb22f-117">Этот метод обновляет переменную члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает свойство "предвращение".</span><span class="sxs-lookup"><span data-stu-id="eb22f-117">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the preroll property.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb22f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="eb22f-118">Requirements</span></span>



| <span data-ttu-id="eb22f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="eb22f-119">Requirement</span></span> | <span data-ttu-id="eb22f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="eb22f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb22f-121">Header</span><span class="sxs-lookup"><span data-stu-id="eb22f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="eb22f-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb22f-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb22f-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb22f-123">Library</span></span><br/> | <dl> <span data-ttu-id="eb22f-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="eb22f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb22f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb22f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb22f-126">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="eb22f-126">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




