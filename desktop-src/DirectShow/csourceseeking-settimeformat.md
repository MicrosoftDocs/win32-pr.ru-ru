---
description: 'Метод Сеттимеформат задает формат времени. Этот метод реализует метод Имедиасикинг:: Сеттимеформат.'
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
ms.openlocfilehash: 61ab0cdf7c954e0fa5f370127f00529bb9ef7b16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658115"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="3fa88-104">Ксаурцесикинг. Сеттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="3fa88-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="3fa88-105">`SetTimeFormat`Метод задает формат времени.</span><span class="sxs-lookup"><span data-stu-id="3fa88-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="3fa88-106">Этот метод реализует метод [**имедиасикинг:: сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="3fa88-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa88-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fa88-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="3fa88-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fa88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fa88-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="3fa88-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3fa88-110">Указатель на GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="3fa88-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="3fa88-111">См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3fa88-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fa88-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3fa88-112">Return value</span></span>

<span data-ttu-id="3fa88-113">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3fa88-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="3fa88-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3fa88-114">Return code</span></span>                                                                                  | <span data-ttu-id="3fa88-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3fa88-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="3fa88-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3fa88-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3fa88-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3fa88-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="3fa88-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3fa88-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3fa88-119">Указанный формат не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3fa88-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="3fa88-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="3fa88-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3fa88-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="3fa88-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="3fa88-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fa88-122">Remarks</span></span>

<span data-ttu-id="3fa88-123">Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="3fa88-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa88-124">Требования</span><span class="sxs-lookup"><span data-stu-id="3fa88-124">Requirements</span></span>



| <span data-ttu-id="3fa88-125">Требование</span><span class="sxs-lookup"><span data-stu-id="3fa88-125">Requirement</span></span> | <span data-ttu-id="3fa88-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3fa88-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa88-127">Header</span><span class="sxs-lookup"><span data-stu-id="3fa88-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3fa88-128"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fa88-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3fa88-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3fa88-129">Library</span></span><br/> | <dl> <span data-ttu-id="3fa88-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3fa88-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fa88-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fa88-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa88-132">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="3fa88-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




