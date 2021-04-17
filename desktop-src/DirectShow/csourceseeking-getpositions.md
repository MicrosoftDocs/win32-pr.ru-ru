---
description: 'Метод Disposition извлекает текущую и заданную позиции. Этот метод реализует метод Имедиасикинг:: Disposition.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Метод Ксаурцесикинг. Disposition (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657502"
---
# <a name="csourceseekinggetpositions-method"></a><span data-ttu-id="6e8cd-104">Метод Ксаурцесикинг. Disposition</span><span class="sxs-lookup"><span data-stu-id="6e8cd-104">CSourceSeeking.GetPositions method</span></span>

<span data-ttu-id="6e8cd-105">`GetPositions`Метод извлекает текущую и заданную позиции.</span><span class="sxs-lookup"><span data-stu-id="6e8cd-105">The `GetPositions` method retrieves the current position and the stop position.</span></span> <span data-ttu-id="6e8cd-106">Этот метод реализует метод [**имедиасикинг:: Disposition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="6e8cd-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e8cd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e8cd-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="6e8cd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e8cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e8cd-109">*пкуррент*</span><span class="sxs-lookup"><span data-stu-id="6e8cd-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="6e8cd-110">Указатель на переменную, которая получает начальную точку.</span><span class="sxs-lookup"><span data-stu-id="6e8cd-110">Pointer to a variable that receives the start position.</span></span>

</dd> <dt>

<span data-ttu-id="6e8cd-111">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="6e8cd-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="6e8cd-112">Указатель на переменную, которая получает точку окончания.</span><span class="sxs-lookup"><span data-stu-id="6e8cd-112">Pointer to a variable that receives the stop position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e8cd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e8cd-113">Return value</span></span>

<span data-ttu-id="6e8cd-114">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6e8cd-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e8cd-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e8cd-115">Remarks</span></span>

<span data-ttu-id="6e8cd-116">Для параметра *пкуррент* этот метод возвращает значение переменной члена [**ксаурцесикинг:: m \_ ртстарт**](csourceseeking-m-rtstart.md) , которая представляет последнее время поиска, а не текущее положение потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="6e8cd-116">For the *pCurrent* parameter, this method returns the value of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) member variable, which represents the latest seek time, not the current streaming position.</span></span> <span data-ttu-id="6e8cd-117">Однако когда приложение вызывает **имедиасикинг:: Disposition** через диспетчер графа фильтров, значения обычно берутся из фильтра модуля подготовки отчетов, а не из фильтра источника.</span><span class="sxs-lookup"><span data-stu-id="6e8cd-117">However, when an application calls **IMediaSeeking::GetPositions** through the filter graph manager, the values typically come from a renderer filter, not a source filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e8cd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6e8cd-118">Requirements</span></span>



| <span data-ttu-id="6e8cd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6e8cd-119">Requirement</span></span> | <span data-ttu-id="6e8cd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6e8cd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8cd-121">Header</span><span class="sxs-lookup"><span data-stu-id="6e8cd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6e8cd-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e8cd-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6e8cd-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6e8cd-123">Library</span></span><br/> | <dl> <span data-ttu-id="6e8cd-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6e8cd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e8cd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e8cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e8cd-126">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="6e8cd-126">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




