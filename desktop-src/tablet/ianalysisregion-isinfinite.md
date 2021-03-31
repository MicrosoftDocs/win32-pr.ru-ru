---
description: Извлекает значение, указывающее, представляет ли Ианалисисрегион неограниченную область.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'Метод Ианалисисрегион:: Infinite (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263160"
---
# <a name="ianalysisregionisinfinite-method"></a><span data-ttu-id="6ba87-103">Метод Ианалисисрегион:: Infinite</span><span class="sxs-lookup"><span data-stu-id="6ba87-103">IAnalysisRegion::IsInfinite method</span></span>

<span data-ttu-id="6ba87-104">Извлекает значение, указывающее, представляет ли [**ианалисисрегион**](ianalysisregion.md) неограниченную область.</span><span class="sxs-lookup"><span data-stu-id="6ba87-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite region.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba87-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ba87-105">Syntax</span></span>


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a><span data-ttu-id="6ba87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ba87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba87-107">*пфисинфините* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6ba87-107">*pfIsInfinite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba87-108">**Вариант \_ Значение TRUE** , если представленный регион является бесконечным; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="6ba87-108">**VARIANT\_TRUE** if the represented region is infinite; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba87-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ba87-109">Return value</span></span>

<span data-ttu-id="6ba87-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6ba87-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba87-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6ba87-111">Requirements</span></span>



| <span data-ttu-id="6ba87-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6ba87-112">Requirement</span></span> | <span data-ttu-id="6ba87-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6ba87-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba87-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ba87-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba87-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6ba87-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6ba87-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ba87-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba87-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6ba87-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6ba87-118">Header</span><span class="sxs-lookup"><span data-stu-id="6ba87-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ba87-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6ba87-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6ba87-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6ba87-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ba87-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ba87-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6ba87-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ba87-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba87-123">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="6ba87-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="6ba87-124">**Метод Ианалисисрегион:: IsEmpty**</span><span class="sxs-lookup"><span data-stu-id="6ba87-124">**IAnalysisRegion::IsEmpty Method**</span></span>](ianalysisregion-isempty.md)
</dt> <dt>

[<span data-ttu-id="6ba87-125">**Метод Ианалисисрегион:: Макимпти**</span><span class="sxs-lookup"><span data-stu-id="6ba87-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="6ba87-126">**Метод Ианалисисрегион:: Макеинфините**</span><span class="sxs-lookup"><span data-stu-id="6ba87-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="6ba87-127">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="6ba87-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




