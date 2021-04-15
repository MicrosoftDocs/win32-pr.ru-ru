---
description: 'Метод Жетпреролл извлекает время предвыполнения. Этот метод реализует метод Имедиасикинг:: Жетпреролл.'
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Ксаурцесикинг. Жетпреролл, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097af089a7221f005cf7f3aac74953166af3cb2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688978"
---
# <a name="csourceseekinggetpreroll-method"></a><span data-ttu-id="a5c5f-104">Ксаурцесикинг. Жетпреролл, метод</span><span class="sxs-lookup"><span data-stu-id="a5c5f-104">CSourceSeeking.GetPreroll method</span></span>

<span data-ttu-id="a5c5f-105">`GetPreroll`Метод получает время предизвлечения.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-105">The `GetPreroll` method retrieves the preroll time.</span></span> <span data-ttu-id="a5c5f-106">Этот метод реализует метод [**имедиасикинг:: жетпреролл**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="a5c5f-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c5f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5c5f-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="a5c5f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5c5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c5f-109">*ппреролл*</span><span class="sxs-lookup"><span data-stu-id="a5c5f-109">*pPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c5f-110">Указатель на переменную, которая получает время предвыполнения.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-110">Pointer to a variable that receives the preroll time.</span></span> <span data-ttu-id="a5c5f-111">Значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-111">The value is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c5f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5c5f-112">Return value</span></span>

<span data-ttu-id="a5c5f-113">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a5c5f-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="a5c5f-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a5c5f-114">Return code</span></span>                                                                               | <span data-ttu-id="a5c5f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a5c5f-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="a5c5f-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a5c5f-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="a5c5f-117">Успешно</span><span class="sxs-lookup"><span data-stu-id="a5c5f-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="a5c5f-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a5c5f-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="a5c5f-119">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="a5c5f-119">**NULL** pointer value</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a5c5f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a5c5f-120">Requirements</span></span>



| <span data-ttu-id="a5c5f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a5c5f-121">Requirement</span></span> | <span data-ttu-id="a5c5f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a5c5f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c5f-123">Header</span><span class="sxs-lookup"><span data-stu-id="a5c5f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a5c5f-124"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5c5f-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5c5f-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a5c5f-125">Library</span></span><br/> | <dl> <span data-ttu-id="a5c5f-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a5c5f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5c5f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5c5f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c5f-128">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="a5c5f-128">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




