---
description: 'Метод Сетдисконтинуити указывает, представляет ли этот образец разрыв в потоке данных. Этот метод реализует метод Имедиасампле:: Сетдисконтинуити.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Кмедиасампле. Сетдисконтинуити, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674986"
---
# <a name="cmediasamplesetdiscontinuity-method"></a><span data-ttu-id="885a6-104">Кмедиасампле. Сетдисконтинуити, метод</span><span class="sxs-lookup"><span data-stu-id="885a6-104">CMediaSample.SetDiscontinuity method</span></span>

<span data-ttu-id="885a6-105">`SetDiscontinuity`Метод указывает, представляет ли этот образец разрыв в потоке данных.</span><span class="sxs-lookup"><span data-stu-id="885a6-105">The `SetDiscontinuity` method specifies whether this sample represents a break in the data stream.</span></span> <span data-ttu-id="885a6-106">Этот метод реализует метод [**имедиасампле:: сетдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="885a6-106">This method implements the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="885a6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="885a6-107">Syntax</span></span>


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a><span data-ttu-id="885a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="885a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="885a6-109">*бдисконт*</span><span class="sxs-lookup"><span data-stu-id="885a6-109">*bDiscont*</span></span> 
</dt> <dd>

<span data-ttu-id="885a6-110">Логическое значение, указывающее, является ли этот пример ненепрерывным.</span><span class="sxs-lookup"><span data-stu-id="885a6-110">Boolean value that specifies whether this sample is a discontinuity.</span></span> <span data-ttu-id="885a6-111">Если **значение — true**, пример носителя не помещается в предыдущий пример.</span><span class="sxs-lookup"><span data-stu-id="885a6-111">If **TRUE**, the media sample is discontinuous with the previous sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="885a6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="885a6-112">Return value</span></span>

<span data-ttu-id="885a6-113">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="885a6-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="885a6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="885a6-114">Remarks</span></span>

<span data-ttu-id="885a6-115">Этот метод обновляет переменную члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает свойство ненепрерывности.</span><span class="sxs-lookup"><span data-stu-id="885a6-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the discontinuity property.</span></span>

## <a name="requirements"></a><span data-ttu-id="885a6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="885a6-116">Requirements</span></span>



| <span data-ttu-id="885a6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="885a6-117">Requirement</span></span> | <span data-ttu-id="885a6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="885a6-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="885a6-119">Header</span><span class="sxs-lookup"><span data-stu-id="885a6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="885a6-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="885a6-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="885a6-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="885a6-121">Library</span></span><br/> | <dl> <span data-ttu-id="885a6-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="885a6-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="885a6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="885a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="885a6-124">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="885a6-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




