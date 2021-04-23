---
description: Получает значение, указывающее, представляет ли Ианалисисрегион пустой регион.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'Метод Ианалисисрегион:: IsEmpty (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719348"
---
# <a name="ianalysisregionisempty-method"></a><span data-ttu-id="1e630-103">Метод Ианалисисрегион:: IsEmpty</span><span class="sxs-lookup"><span data-stu-id="1e630-103">IAnalysisRegion::IsEmpty method</span></span>

<span data-ttu-id="1e630-104">Получает значение, указывающее, представляет ли [**ианалисисрегион**](ianalysisregion.md) пустой регион.</span><span class="sxs-lookup"><span data-stu-id="1e630-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an empty region.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e630-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e630-105">Syntax</span></span>


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a><span data-ttu-id="1e630-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e630-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e630-107">*пфисемпти* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e630-107">*pfIsEmpty* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e630-108">**Вариант \_ Значение TRUE** , если представленный регион пуст; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="1e630-108">**VARIANT\_TRUE** if the represented region is empty; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e630-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e630-109">Return value</span></span>

<span data-ttu-id="1e630-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1e630-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e630-111">Требования</span><span class="sxs-lookup"><span data-stu-id="1e630-111">Requirements</span></span>



| <span data-ttu-id="1e630-112">Требование</span><span class="sxs-lookup"><span data-stu-id="1e630-112">Requirement</span></span> | <span data-ttu-id="1e630-113">Значение</span><span class="sxs-lookup"><span data-stu-id="1e630-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e630-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e630-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1e630-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1e630-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1e630-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e630-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1e630-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1e630-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1e630-118">Header</span><span class="sxs-lookup"><span data-stu-id="1e630-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e630-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1e630-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1e630-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1e630-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e630-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e630-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1e630-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e630-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e630-123">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="1e630-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="1e630-124">**Метод Ианалисисрегион:: Infinite**</span><span class="sxs-lookup"><span data-stu-id="1e630-124">**IAnalysisRegion::IsInfinite Method**</span></span>](ianalysisregion-isinfinite.md)
</dt> <dt>

[<span data-ttu-id="1e630-125">**Метод Ианалисисрегион:: Макимпти**</span><span class="sxs-lookup"><span data-stu-id="1e630-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="1e630-126">**Метод Ианалисисрегион:: Макеинфините**</span><span class="sxs-lookup"><span data-stu-id="1e630-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="1e630-127">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="1e630-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




