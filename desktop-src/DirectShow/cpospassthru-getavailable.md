---
description: 'Метод Кпоспасссру. дальнего действия. метод доступа к доступности извлекает диапазон времени, в течение которого поиск является эффективным. Этот метод реализует метод Имедиасикинг:: onavailable.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Метод Кпоспасссру. Available (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d56827a68f4c287e5808f0d8f64b8142c31b1f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095292"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="2ff04-104">Кпоспасссру. доступный метод</span><span class="sxs-lookup"><span data-stu-id="2ff04-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="2ff04-105">`GetAvailable`Метод извлекает диапазон времени, в котором поиск является эффективным.</span><span class="sxs-lookup"><span data-stu-id="2ff04-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="2ff04-106">Этот метод реализует метод [**имедиасикинг:: onavailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="2ff04-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff04-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ff04-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="2ff04-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ff04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff04-109">*пеарлиест*</span><span class="sxs-lookup"><span data-stu-id="2ff04-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="2ff04-110">Указатель на переменную, которая получает самое раннее время для эффективного поиска.</span><span class="sxs-lookup"><span data-stu-id="2ff04-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="2ff04-111">*Пластина*</span><span class="sxs-lookup"><span data-stu-id="2ff04-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="2ff04-112">Указатель на переменную, которая получает Последнее время для эффективного поиска.</span><span class="sxs-lookup"><span data-stu-id="2ff04-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff04-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ff04-113">Return value</span></span>

<span data-ttu-id="2ff04-114">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="2ff04-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff04-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2ff04-115">Requirements</span></span>



| <span data-ttu-id="2ff04-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2ff04-116">Requirement</span></span> | <span data-ttu-id="2ff04-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2ff04-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff04-118">Header</span><span class="sxs-lookup"><span data-stu-id="2ff04-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2ff04-119"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ff04-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2ff04-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ff04-120">Library</span></span><br/> | <dl> <span data-ttu-id="2ff04-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2ff04-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ff04-122">См. также</span><span class="sxs-lookup"><span data-stu-id="2ff04-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff04-123">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="2ff04-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




