---
description: Определяет, пересекаются ли области Ианалисисрегион с указанным прямоугольником.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'Метод Ианалисисрегион:: Интерсектсвис (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542095"
---
# <a name="ianalysisregionintersectswith-method"></a><span data-ttu-id="11bed-103">Метод Ианалисисрегион:: Интерсектсвис</span><span class="sxs-lookup"><span data-stu-id="11bed-103">IAnalysisRegion::IntersectsWith method</span></span>

<span data-ttu-id="11bed-104">Определяет, пересекаются ли области [**ианалисисрегион**](ianalysisregion.md) с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="11bed-104">Determines whether the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="11bed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11bed-105">Syntax</span></span>


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a><span data-ttu-id="11bed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11bed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11bed-107">*пректангле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11bed-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11bed-108">Указатель на прямоугольник, с которым выполняется сравнение, в координатах рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="11bed-108">A pointer to the rectangle with which to compare, in ink-space coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="11bed-109">*пфисинтерсектинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="11bed-109">*pfIsIntersecting* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11bed-110">**Вариант \_ Значение TRUE** , если область [**ианалисисрегион**](ianalysisregion.md) пересекается с указанным прямоугольником; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="11bed-110">**VARIANT\_TRUE** if the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11bed-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11bed-111">Return value</span></span>

<span data-ttu-id="11bed-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="11bed-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="11bed-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11bed-113">Remarks</span></span>

<span data-ttu-id="11bed-114">Сравнение осуществляется по координатам рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="11bed-114">The comparison is in ink-space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="11bed-115">Требования</span><span class="sxs-lookup"><span data-stu-id="11bed-115">Requirements</span></span>



| <span data-ttu-id="11bed-116">Требование</span><span class="sxs-lookup"><span data-stu-id="11bed-116">Requirement</span></span> | <span data-ttu-id="11bed-117">Значение</span><span class="sxs-lookup"><span data-stu-id="11bed-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11bed-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11bed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="11bed-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="11bed-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11bed-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11bed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="11bed-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="11bed-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="11bed-122">Header</span><span class="sxs-lookup"><span data-stu-id="11bed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="11bed-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="11bed-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="11bed-124">DLL</span><span class="sxs-lookup"><span data-stu-id="11bed-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11bed-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11bed-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="11bed-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11bed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11bed-127">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="11bed-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="11bed-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="11bed-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




