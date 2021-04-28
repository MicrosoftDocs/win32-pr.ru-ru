---
description: 'Ксаурцесикинг. Исформатсуппортед, метод Исформатсуппортед определяет, поддерживается ли указанный формат времени. Этот метод реализует метод Имедиасикинг:: Исформатсуппортед.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Ксаурцесикинг. Исформатсуппортед, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c58e8edd908c101c3045e221cc86420cbb5cb94
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098752"
---
# <a name="csourceseekingisformatsupported-method"></a><span data-ttu-id="7d130-104">Ксаурцесикинг. Исформатсуппортед, метод</span><span class="sxs-lookup"><span data-stu-id="7d130-104">CSourceSeeking.IsFormatSupported method</span></span>

<span data-ttu-id="7d130-105">`IsFormatSupported`Метод определяет, поддерживается ли указанный формат времени.</span><span class="sxs-lookup"><span data-stu-id="7d130-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="7d130-106">Этот метод реализует метод [**имедиасикинг:: исформатсуппортед**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="7d130-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d130-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d130-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="7d130-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d130-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d130-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="7d130-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="7d130-110">Указатель на GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="7d130-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="7d130-111">См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7d130-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d130-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d130-112">Return value</span></span>

<span data-ttu-id="7d130-113">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7d130-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="7d130-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7d130-114">Return code</span></span>                                                                               | <span data-ttu-id="7d130-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7d130-115">Description</span></span>                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="7d130-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7d130-116"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="7d130-117">Формат не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d130-117">The format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="7d130-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7d130-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7d130-119">Формат поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d130-119">The format is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="7d130-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7d130-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7d130-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="7d130-121">**NULL** pointer argument.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="7d130-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="7d130-122">Remarks</span></span>

<span data-ttu-id="7d130-123">Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="7d130-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d130-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7d130-124">Requirements</span></span>



| <span data-ttu-id="7d130-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7d130-125">Requirement</span></span> | <span data-ttu-id="7d130-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7d130-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d130-127">Header</span><span class="sxs-lookup"><span data-stu-id="7d130-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7d130-128"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d130-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7d130-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7d130-129">Library</span></span><br/> | <dl> <span data-ttu-id="7d130-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7d130-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d130-131">См. также</span><span class="sxs-lookup"><span data-stu-id="7d130-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d130-132">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="7d130-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




