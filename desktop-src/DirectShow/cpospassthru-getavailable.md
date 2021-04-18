---
description: 'Метод доступа к доступу извлекает диапазон времени, в течение которого поиск является эффективным. Этот метод реализует метод Имедиасикинг:: onavailable.'
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
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675409"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="68eff-104">Кпоспасссру. доступный метод</span><span class="sxs-lookup"><span data-stu-id="68eff-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="68eff-105">`GetAvailable`Метод извлекает диапазон времени, в котором поиск является эффективным.</span><span class="sxs-lookup"><span data-stu-id="68eff-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="68eff-106">Этот метод реализует метод [**имедиасикинг:: onavailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="68eff-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="68eff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68eff-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="68eff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68eff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68eff-109">*пеарлиест*</span><span class="sxs-lookup"><span data-stu-id="68eff-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="68eff-110">Указатель на переменную, которая получает самое раннее время для эффективного поиска.</span><span class="sxs-lookup"><span data-stu-id="68eff-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="68eff-111">*Пластина*</span><span class="sxs-lookup"><span data-stu-id="68eff-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="68eff-112">Указатель на переменную, которая получает Последнее время для эффективного поиска.</span><span class="sxs-lookup"><span data-stu-id="68eff-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68eff-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68eff-113">Return value</span></span>

<span data-ttu-id="68eff-114">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="68eff-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="68eff-115">Требования</span><span class="sxs-lookup"><span data-stu-id="68eff-115">Requirements</span></span>



| <span data-ttu-id="68eff-116">Требование</span><span class="sxs-lookup"><span data-stu-id="68eff-116">Requirement</span></span> | <span data-ttu-id="68eff-117">Значение</span><span class="sxs-lookup"><span data-stu-id="68eff-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68eff-118">Header</span><span class="sxs-lookup"><span data-stu-id="68eff-118">Header</span></span><br/>  | <dl> <span data-ttu-id="68eff-119"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68eff-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="68eff-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68eff-120">Library</span></span><br/> | <dl> <span data-ttu-id="68eff-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="68eff-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68eff-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68eff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68eff-123">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="68eff-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




