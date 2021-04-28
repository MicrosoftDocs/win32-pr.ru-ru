---
description: 'Метод Ксаурцесикинг. дальнего действия. метод доступа к доступности извлекает диапазон времени, в течение которого поиск является эффективным. Этот метод реализует метод Имедиасикинг:: onavailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Метод Ксаурцесикинг. Available (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24bc667eec4f5b21c90415e4721aa8cf0a0ad4c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085242"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="578aa-104">Ксаурцесикинг. доступный метод</span><span class="sxs-lookup"><span data-stu-id="578aa-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="578aa-105">`GetAvailable`Метод извлекает диапазон времени, в котором поиск является эффективным.</span><span class="sxs-lookup"><span data-stu-id="578aa-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="578aa-106">Этот метод реализует метод [**имедиасикинг:: onavailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="578aa-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="578aa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="578aa-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="578aa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="578aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="578aa-109">*пеарлиест*</span><span class="sxs-lookup"><span data-stu-id="578aa-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="578aa-110">Указатель на переменную, которая получает самое раннее время для эффективного поиска.</span><span class="sxs-lookup"><span data-stu-id="578aa-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="578aa-111">Переменная имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="578aa-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="578aa-112">*Пластина*</span><span class="sxs-lookup"><span data-stu-id="578aa-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="578aa-113">Указатель на переменную, которая получает Последнее время для эффективного поиска.</span><span class="sxs-lookup"><span data-stu-id="578aa-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="578aa-114">Переменной присваивается значение переменной-члена [**ксаурцесикинг:: m \_ ртдуратион**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="578aa-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="578aa-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="578aa-115">Return value</span></span>

<span data-ttu-id="578aa-116">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="578aa-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="578aa-117">Требования</span><span class="sxs-lookup"><span data-stu-id="578aa-117">Requirements</span></span>



| <span data-ttu-id="578aa-118">Требование</span><span class="sxs-lookup"><span data-stu-id="578aa-118">Requirement</span></span> | <span data-ttu-id="578aa-119">Значение</span><span class="sxs-lookup"><span data-stu-id="578aa-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="578aa-120">Header</span><span class="sxs-lookup"><span data-stu-id="578aa-120">Header</span></span><br/>  | <dl> <span data-ttu-id="578aa-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="578aa-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="578aa-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="578aa-122">Library</span></span><br/> | <dl> <span data-ttu-id="578aa-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="578aa-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="578aa-124">См. также</span><span class="sxs-lookup"><span data-stu-id="578aa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578aa-125">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="578aa-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




