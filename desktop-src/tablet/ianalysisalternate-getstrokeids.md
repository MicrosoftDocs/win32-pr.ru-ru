---
description: Возвращает идентификаторы Stroke, связанные с этим Ианалисисалтернате.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'Метод Ианалисисалтернате:: Жетстрокеидс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897498"
---
# <a name="ianalysisalternategetstrokeids-method"></a><span data-ttu-id="9db42-103">Метод Ианалисисалтернате:: Жетстрокеидс</span><span class="sxs-lookup"><span data-stu-id="9db42-103">IAnalysisAlternate::GetStrokeIds method</span></span>

<span data-ttu-id="9db42-104">Возвращает идентификаторы Stroke, связанные с этим [**ианалисисалтернате**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="9db42-104">Returns the stroke identifiers that are associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9db42-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9db42-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="9db42-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9db42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db42-107">*пулстрокеидскаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9db42-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9db42-108">Указатель на **ulong** , для которой задано число идентификаторов Stroke, связанных с этим [**ианалисисалтернате**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="9db42-108">A pointer to a **ULONG** that is set to the number of stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> <dt>

<span data-ttu-id="9db42-109">*пплстрокеидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9db42-109">*pplStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9db42-110">\[out, размер \_ ( \* *ПУЛСТРОКЕИДСКАУНТ* \* sizeof (Long))\]</span><span class="sxs-lookup"><span data-stu-id="9db42-110">\[out, size\_is(\**pulStrokeIdsCount* \* sizeof(LONG))\]</span></span>

<span data-ttu-id="9db42-111">Массив **длинной** длины *пулстрокеидскаунт* , для которой заданы идентификаторы штриха, связанные с этим [**ианалисисалтернате**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="9db42-111">An array of **LONG** of length *pulStrokeIdsCount* that is set to the stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db42-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9db42-112">Return value</span></span>

<span data-ttu-id="9db42-113">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9db42-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9db42-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9db42-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9db42-115">Чтобы избежать утечки памяти, используйте [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *пплстрокеидс* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="9db42-115">To avoid a memory leak, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokeIds* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9db42-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9db42-116">Requirements</span></span>



| <span data-ttu-id="9db42-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9db42-117">Requirement</span></span> | <span data-ttu-id="9db42-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9db42-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db42-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9db42-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9db42-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9db42-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9db42-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9db42-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9db42-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9db42-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9db42-123">Header</span><span class="sxs-lookup"><span data-stu-id="9db42-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db42-124"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9db42-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9db42-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9db42-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db42-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db42-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9db42-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9db42-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db42-128">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="9db42-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="9db42-129">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9db42-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

