---
description: 'Метод unadvise Удаляет ожидающий запрос Advise. Этот метод реализует метод Иреференцеклокк:: unadvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Метод Кбасереференцеклокк. unadvise (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657907"
---
# <a name="cbasereferenceclockunadvise-method"></a><span data-ttu-id="09e26-104">Кбасереференцеклокк. unadvise, метод</span><span class="sxs-lookup"><span data-stu-id="09e26-104">CBaseReferenceClock.Unadvise method</span></span>

<span data-ttu-id="09e26-105">`Unadvise`Метод удаляет ожидающий запрос рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="09e26-105">The `Unadvise` method removes a pending advise request.</span></span> <span data-ttu-id="09e26-106">Этот метод реализует метод [**иреференцеклокк:: unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .</span><span class="sxs-lookup"><span data-stu-id="09e26-106">This method implements the [**IReferenceClock::Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e26-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09e26-107">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="09e26-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="09e26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e26-109">*двадвисетокен*</span><span class="sxs-lookup"><span data-stu-id="09e26-109">*dwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="09e26-110">Идентификатор удаляемого запроса.</span><span class="sxs-lookup"><span data-stu-id="09e26-110">Identifier of the request to remove.</span></span> <span data-ttu-id="09e26-111">Используйте значение, возвращаемое методами [**кбасереференцеклокк:: адвисетиме**](cbasereferenceclock-advisetime.md) или [**Кбасереференцеклокк:: адвисепериодик**](cbasereferenceclock-adviseperiodic.md) в параметре *пдвадвисетокен* .</span><span class="sxs-lookup"><span data-stu-id="09e26-111">Use the value returned by the [**CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) or [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) methods in the *pdwAdviseToken* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e26-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09e26-112">Return value</span></span>

<span data-ttu-id="09e26-113">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="09e26-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="09e26-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="09e26-114">Return code</span></span>                                                                             | <span data-ttu-id="09e26-115">Описание</span><span class="sxs-lookup"><span data-stu-id="09e26-115">Description</span></span>           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="09e26-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="09e26-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="09e26-117">Не найдено.</span><span class="sxs-lookup"><span data-stu-id="09e26-117">Not found.</span></span><br/> |
| <dl> <span data-ttu-id="09e26-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="09e26-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="09e26-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="09e26-119">Success.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="09e26-120">Требования</span><span class="sxs-lookup"><span data-stu-id="09e26-120">Requirements</span></span>



| <span data-ttu-id="09e26-121">Требование</span><span class="sxs-lookup"><span data-stu-id="09e26-121">Requirement</span></span> | <span data-ttu-id="09e26-122">Значение</span><span class="sxs-lookup"><span data-stu-id="09e26-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09e26-123">Header</span><span class="sxs-lookup"><span data-stu-id="09e26-123">Header</span></span><br/>  | <dl> <span data-ttu-id="09e26-124"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09e26-124"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="09e26-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09e26-125">Library</span></span><br/> | <dl> <span data-ttu-id="09e26-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="09e26-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09e26-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09e26-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e26-128">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="09e26-128">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




