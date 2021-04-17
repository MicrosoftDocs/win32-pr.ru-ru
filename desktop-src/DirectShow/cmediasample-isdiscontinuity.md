---
description: 'Метод Исдисконтинуити определяет, представляет ли этот образец разрыв в потоке данных. Этот метод реализует метод Имедиасампле:: Исдисконтинуити.'
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Кмедиасампле. Исдисконтинуити, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665214"
---
# <a name="cmediasampleisdiscontinuity-method"></a><span data-ttu-id="52124-104">Кмедиасампле. Исдисконтинуити, метод</span><span class="sxs-lookup"><span data-stu-id="52124-104">CMediaSample.IsDiscontinuity method</span></span>

<span data-ttu-id="52124-105">`IsDiscontinuity`Метод определяет, представляет ли этот образец разрыв в потоке данных.</span><span class="sxs-lookup"><span data-stu-id="52124-105">The `IsDiscontinuity` method determines if this sample represents a break in the data stream.</span></span> <span data-ttu-id="52124-106">Этот метод реализует метод [**имедиасампле:: исдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="52124-106">This method implements the [**IMediaSample::IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="52124-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52124-107">Syntax</span></span>


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a><span data-ttu-id="52124-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52124-108">Parameters</span></span>

<span data-ttu-id="52124-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="52124-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52124-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52124-110">Return value</span></span>

<span data-ttu-id="52124-111">Возвращает \_ значение ОК, если образец является перерывом в потоке данных, и \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="52124-111">Returns S\_OK if the sample is a break in the data stream, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="52124-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52124-112">Remarks</span></span>

<span data-ttu-id="52124-113">Значение этого свойства указывается в переменной члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) .</span><span class="sxs-lookup"><span data-stu-id="52124-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="52124-114">Требования</span><span class="sxs-lookup"><span data-stu-id="52124-114">Requirements</span></span>



| <span data-ttu-id="52124-115">Требование</span><span class="sxs-lookup"><span data-stu-id="52124-115">Requirement</span></span> | <span data-ttu-id="52124-116">Значение</span><span class="sxs-lookup"><span data-stu-id="52124-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52124-117">Header</span><span class="sxs-lookup"><span data-stu-id="52124-117">Header</span></span><br/>  | <dl> <span data-ttu-id="52124-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52124-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="52124-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52124-119">Library</span></span><br/> | <dl> <span data-ttu-id="52124-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="52124-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52124-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52124-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52124-122">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="52124-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




