---
description: 'Метод Куерипреферредформат извлекает предпочтительный формат времени объекта. Этот метод реализует метод Имедиасикинг:: Куерипреферредформат.'
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Ксаурцесикинг. Куерипреферредформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688889"
---
# <a name="csourceseekingquerypreferredformat-method"></a><span data-ttu-id="bf550-104">Ксаурцесикинг. Куерипреферредформат, метод</span><span class="sxs-lookup"><span data-stu-id="bf550-104">CSourceSeeking.QueryPreferredFormat method</span></span>

<span data-ttu-id="bf550-105">`QueryPreferredFormat`Метод получает предпочтительный формат времени объекта.</span><span class="sxs-lookup"><span data-stu-id="bf550-105">The `QueryPreferredFormat` method retrieves the object's preferred time format.</span></span> <span data-ttu-id="bf550-106">Этот метод реализует метод [**имедиасикинг:: куерипреферредформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="bf550-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf550-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf550-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="bf550-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf550-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf550-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="bf550-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="bf550-110">Указатель на переменную, которая получает GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="bf550-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="bf550-111">См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="bf550-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf550-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf550-112">Return value</span></span>

<span data-ttu-id="bf550-113">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bf550-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="bf550-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bf550-114">Return code</span></span>                                                                               | <span data-ttu-id="bf550-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bf550-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="bf550-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bf550-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="bf550-117">Успешно</span><span class="sxs-lookup"><span data-stu-id="bf550-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="bf550-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="bf550-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="bf550-119">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="bf550-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf550-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf550-120">Remarks</span></span>

<span data-ttu-id="bf550-121">Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="bf550-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf550-122">Требования</span><span class="sxs-lookup"><span data-stu-id="bf550-122">Requirements</span></span>



| <span data-ttu-id="bf550-123">Требование</span><span class="sxs-lookup"><span data-stu-id="bf550-123">Requirement</span></span> | <span data-ttu-id="bf550-124">Значение</span><span class="sxs-lookup"><span data-stu-id="bf550-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf550-125">Header</span><span class="sxs-lookup"><span data-stu-id="bf550-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bf550-126"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf550-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf550-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf550-127">Library</span></span><br/> | <dl> <span data-ttu-id="bf550-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bf550-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf550-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf550-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf550-130">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="bf550-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




