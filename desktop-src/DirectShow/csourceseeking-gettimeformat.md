---
description: 'Метод Жеттимеформат извлекает текущий формат времени. Этот метод реализует метод Имедиасикинг:: Жеттимеформат.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Ксаурцесикинг. Жеттимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce53f4a6cabcc5face6c332666701dc208c3f8bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657500"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="fc8ee-104">Ксаурцесикинг. Жеттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="fc8ee-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="fc8ee-105">`GetTimeFormat`Метод получает текущий формат времени.</span><span class="sxs-lookup"><span data-stu-id="fc8ee-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="fc8ee-106">Этот метод реализует метод [**имедиасикинг:: жеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="fc8ee-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8ee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc8ee-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="fc8ee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc8ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc8ee-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="fc8ee-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="fc8ee-110">Указатель на переменную, которая получает GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="fc8ee-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="fc8ee-111">См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="fc8ee-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc8ee-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc8ee-112">Return value</span></span>

<span data-ttu-id="fc8ee-113">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fc8ee-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="fc8ee-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fc8ee-114">Return code</span></span>                                                                               | <span data-ttu-id="fc8ee-115">Описание</span><span class="sxs-lookup"><span data-stu-id="fc8ee-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="fc8ee-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fc8ee-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="fc8ee-117">Успешно</span><span class="sxs-lookup"><span data-stu-id="fc8ee-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="fc8ee-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc8ee-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="fc8ee-119">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="fc8ee-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fc8ee-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc8ee-120">Remarks</span></span>

<span data-ttu-id="fc8ee-121">Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="fc8ee-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8ee-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fc8ee-122">Requirements</span></span>



| <span data-ttu-id="fc8ee-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fc8ee-123">Requirement</span></span> | <span data-ttu-id="fc8ee-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fc8ee-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8ee-125">Header</span><span class="sxs-lookup"><span data-stu-id="fc8ee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fc8ee-126"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc8ee-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc8ee-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc8ee-127">Library</span></span><br/> | <dl> <span data-ttu-id="fc8ee-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fc8ee-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc8ee-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc8ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc8ee-130">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="fc8ee-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




