---
description: Метод Исусингтимеформат определяет, является ли указанный формат времени используемым в данный момент форматом.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Ксаурцесикинг. Исусингтимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657498"
---
# <a name="csourceseekingisusingtimeformat-method"></a><span data-ttu-id="f401d-103">Ксаурцесикинг. Исусингтимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="f401d-103">CSourceSeeking.IsUsingTimeFormat method</span></span>

<span data-ttu-id="f401d-104">`IsUsingTimeFormat`Метод определяет, является ли указанный формат времени используемым в данный момент форматом.</span><span class="sxs-lookup"><span data-stu-id="f401d-104">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="f401d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f401d-105">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="f401d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f401d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f401d-107">*пформат*</span><span class="sxs-lookup"><span data-stu-id="f401d-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="f401d-108">Указатель на GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="f401d-108">Pointer to a time format GUID.</span></span> <span data-ttu-id="f401d-109">См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f401d-109">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f401d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f401d-110">Return value</span></span>

<span data-ttu-id="f401d-111">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f401d-111">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="f401d-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f401d-112">Return code</span></span>                                                                               | <span data-ttu-id="f401d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f401d-113">Description</span></span>                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="f401d-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f401d-114"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="f401d-115">Указанный формат не является текущим форматом.</span><span class="sxs-lookup"><span data-stu-id="f401d-115">The specified format is not the current format.</span></span><br/> |
| <dl> <span data-ttu-id="f401d-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f401d-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f401d-117">Указанный формат является текущим форматом.</span><span class="sxs-lookup"><span data-stu-id="f401d-117">The specified format is the current format.</span></span><br/>     |
| <dl> <span data-ttu-id="f401d-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f401d-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="f401d-119">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="f401d-119">**NULL** pointer argument.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="f401d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f401d-120">Remarks</span></span>

<span data-ttu-id="f401d-121">Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="f401d-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="f401d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f401d-122">Requirements</span></span>



| <span data-ttu-id="f401d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f401d-123">Requirement</span></span> | <span data-ttu-id="f401d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f401d-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f401d-125">Header</span><span class="sxs-lookup"><span data-stu-id="f401d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f401d-126"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f401d-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f401d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f401d-127">Library</span></span><br/> | <dl> <span data-ttu-id="f401d-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f401d-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f401d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f401d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f401d-130">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="f401d-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




