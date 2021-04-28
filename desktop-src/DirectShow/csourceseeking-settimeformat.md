---
description: 'Ксаурцесикинг. Сеттимеформат, метод Сеттимеформат задает формат времени. Этот метод реализует метод Имедиасикинг:: Сеттимеформат.'
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Ксаурцесикинг. Сеттимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdb3889ecfa5bdcd49b4054822a2b2d09df58fa6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085202"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="82d69-104">Ксаурцесикинг. Сеттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="82d69-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="82d69-105">`SetTimeFormat`Метод задает формат времени.</span><span class="sxs-lookup"><span data-stu-id="82d69-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="82d69-106">Этот метод реализует метод [**имедиасикинг:: сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="82d69-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d69-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82d69-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="82d69-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="82d69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d69-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="82d69-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="82d69-110">Указатель на GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="82d69-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="82d69-111">См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="82d69-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d69-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82d69-112">Return value</span></span>

<span data-ttu-id="82d69-113">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="82d69-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="82d69-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="82d69-114">Return code</span></span>                                                                                  | <span data-ttu-id="82d69-115">Описание</span><span class="sxs-lookup"><span data-stu-id="82d69-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="82d69-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="82d69-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="82d69-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="82d69-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="82d69-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="82d69-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="82d69-119">Указанный формат не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="82d69-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="82d69-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="82d69-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="82d69-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="82d69-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="82d69-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="82d69-122">Remarks</span></span>

<span data-ttu-id="82d69-123">Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="82d69-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="82d69-124">Требования</span><span class="sxs-lookup"><span data-stu-id="82d69-124">Requirements</span></span>



| <span data-ttu-id="82d69-125">Требование</span><span class="sxs-lookup"><span data-stu-id="82d69-125">Requirement</span></span> | <span data-ttu-id="82d69-126">Значение</span><span class="sxs-lookup"><span data-stu-id="82d69-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d69-127">Header</span><span class="sxs-lookup"><span data-stu-id="82d69-127">Header</span></span><br/>  | <dl> <span data-ttu-id="82d69-128"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82d69-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82d69-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82d69-129">Library</span></span><br/> | <dl> <span data-ttu-id="82d69-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="82d69-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82d69-131">См. также</span><span class="sxs-lookup"><span data-stu-id="82d69-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d69-132">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="82d69-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




