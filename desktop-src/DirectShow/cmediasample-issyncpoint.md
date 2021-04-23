---
description: 'Метод Иссинкпоинт определяет, является ли начало образца точкой синхронизации. Этот метод реализует метод Имедиасампле:: Иссинкпоинт.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Кмедиасампле. Иссинкпоинт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665212"
---
# <a name="cmediasampleissyncpoint-method"></a><span data-ttu-id="4abc9-104">Кмедиасампле. Иссинкпоинт, метод</span><span class="sxs-lookup"><span data-stu-id="4abc9-104">CMediaSample.IsSyncPoint method</span></span>

<span data-ttu-id="4abc9-105">`IsSyncPoint`Метод определяет, является ли начало образца точкой синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4abc9-105">The `IsSyncPoint` method determines if the beginning of the sample is a synchronization point.</span></span> <span data-ttu-id="4abc9-106">Этот метод реализует метод [**имедиасампле:: иссинкпоинт**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="4abc9-106">This method implements the [**IMediaSample::IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4abc9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4abc9-107">Syntax</span></span>


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a><span data-ttu-id="4abc9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4abc9-108">Parameters</span></span>

<span data-ttu-id="4abc9-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4abc9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4abc9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4abc9-110">Return value</span></span>

<span data-ttu-id="4abc9-111">Возвращает \_ значение ОК, если образец является точкой синхронизации, или \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4abc9-111">Returns S\_OK if the sample is a synchronization point, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4abc9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4abc9-112">Remarks</span></span>

<span data-ttu-id="4abc9-113">Значение этого свойства указывается в переменной члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) .</span><span class="sxs-lookup"><span data-stu-id="4abc9-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4abc9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4abc9-114">Requirements</span></span>



| <span data-ttu-id="4abc9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4abc9-115">Requirement</span></span> | <span data-ttu-id="4abc9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4abc9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4abc9-117">Header</span><span class="sxs-lookup"><span data-stu-id="4abc9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4abc9-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4abc9-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4abc9-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4abc9-119">Library</span></span><br/> | <dl> <span data-ttu-id="4abc9-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4abc9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4abc9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4abc9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abc9-122">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="4abc9-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




