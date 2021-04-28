---
description: Крендерерпоспасссру. Жетмедиатиме, метод Жетмедиатиме извлекает метки времени для текущего образца.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Крендерерпоспасссру. Жетмедиатиме, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588c92faec6b68cfa51392d4df00567c4e881460
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085372"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="43f1c-103">Крендерерпоспасссру. Жетмедиатиме, метод</span><span class="sxs-lookup"><span data-stu-id="43f1c-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="43f1c-104">`GetMediaTime`Метод получает метки времени для текущего образца.</span><span class="sxs-lookup"><span data-stu-id="43f1c-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f1c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43f1c-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="43f1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43f1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f1c-107">*пстарттиме*</span><span class="sxs-lookup"><span data-stu-id="43f1c-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="43f1c-108">Указатель на переменную, которая получает время начала в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="43f1c-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="43f1c-109">*пендтиме*</span><span class="sxs-lookup"><span data-stu-id="43f1c-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="43f1c-110">Указатель на переменную, которая получает время окончания в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="43f1c-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="43f1c-111">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="43f1c-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f1c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43f1c-112">Return value</span></span>

<span data-ttu-id="43f1c-113">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43f1c-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="43f1c-114">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="43f1c-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="43f1c-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="43f1c-115">Return code</span></span>                                                                                  | <span data-ttu-id="43f1c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="43f1c-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="43f1c-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="43f1c-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="43f1c-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="43f1c-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="43f1c-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="43f1c-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="43f1c-120">Преобразование в этот формат не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="43f1c-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="43f1c-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="43f1c-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="43f1c-122">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="43f1c-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="43f1c-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="43f1c-123">Remarks</span></span>

<span data-ttu-id="43f1c-124">Этот метод переопределяет метод [**кпоспасссру:: жетмедиатиме**](cpospassthru-getmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="43f1c-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="43f1c-125">Значения временной метки преобразуются в текущий формат времени путем вызова метода [**кпоспасссру:: конверттимеформат**](cpospassthru-converttimeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="43f1c-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f1c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="43f1c-126">Requirements</span></span>



| <span data-ttu-id="43f1c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="43f1c-127">Requirement</span></span> | <span data-ttu-id="43f1c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="43f1c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43f1c-129">Header</span><span class="sxs-lookup"><span data-stu-id="43f1c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="43f1c-130"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43f1c-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43f1c-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43f1c-131">Library</span></span><br/> | <dl> <span data-ttu-id="43f1c-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="43f1c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




