---
description: 'Метод Сетсинкпоинт указывает, является ли начало этого образца точкой синхронизации. Этот метод реализует метод Имедиасампле:: Сетсинкпоинт.'
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Кмедиасампле. Сетсинкпоинт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665195"
---
# <a name="cmediasamplesetsyncpoint-method"></a><span data-ttu-id="691bd-104">Кмедиасампле. Сетсинкпоинт, метод</span><span class="sxs-lookup"><span data-stu-id="691bd-104">CMediaSample.SetSyncPoint method</span></span>

<span data-ttu-id="691bd-105">`SetSyncPoint`Метод указывает, является ли начало этого образца точкой синхронизации.</span><span class="sxs-lookup"><span data-stu-id="691bd-105">The `SetSyncPoint` method specifies whether the beginning of this sample is a synchronization point.</span></span> <span data-ttu-id="691bd-106">Этот метод реализует метод [**имедиасампле:: сетсинкпоинт**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="691bd-106">This method implements the [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="691bd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="691bd-107">Syntax</span></span>


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a><span data-ttu-id="691bd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="691bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="691bd-109">*биссинкпоинт*</span><span class="sxs-lookup"><span data-stu-id="691bd-109">*bIsSyncPoint*</span></span> 
</dt> <dd>

<span data-ttu-id="691bd-110">Логическое значение, указывающее, является ли точка синхронизации.</span><span class="sxs-lookup"><span data-stu-id="691bd-110">Boolean value that specifies whether this is a synchronization point.</span></span> <span data-ttu-id="691bd-111">Если **значение равно true**, это точка синхронизации.</span><span class="sxs-lookup"><span data-stu-id="691bd-111">If **TRUE**, this is a synchronization point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="691bd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="691bd-112">Return value</span></span>

<span data-ttu-id="691bd-113">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="691bd-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="691bd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="691bd-114">Remarks</span></span>

<span data-ttu-id="691bd-115">Этот метод обновляет переменную-член [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает свойство точки синхронизации.</span><span class="sxs-lookup"><span data-stu-id="691bd-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the synchronization-point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="691bd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="691bd-116">Requirements</span></span>



| <span data-ttu-id="691bd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="691bd-117">Requirement</span></span> | <span data-ttu-id="691bd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="691bd-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="691bd-119">Header</span><span class="sxs-lookup"><span data-stu-id="691bd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="691bd-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="691bd-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="691bd-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="691bd-121">Library</span></span><br/> | <dl> <span data-ttu-id="691bd-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="691bd-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="691bd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="691bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="691bd-124">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="691bd-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




