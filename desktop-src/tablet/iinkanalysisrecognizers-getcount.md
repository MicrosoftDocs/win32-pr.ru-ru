---
description: Возвращает число объектов Иинканалисисрекогнизер в данной коллекции.
ms.assetid: dfb5c530-b481-4c60-b7fe-87fe162de270
title: 'Метод Иинканалисисрекогнизерс:: NOCOUNT (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e65f8399c661d551e805abe5f1c5db33eb0b154a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542039"
---
# <a name="iinkanalysisrecognizersgetcount-method"></a><span data-ttu-id="a0bf3-103">Метод Иинканалисисрекогнизерс:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="a0bf3-103">IInkAnalysisRecognizers::GetCount method</span></span>

<span data-ttu-id="a0bf3-104">Возвращает число объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) в данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="a0bf3-104">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bf3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0bf3-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="a0bf3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0bf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0bf3-107">*пулкаунт* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a0bf3-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a0bf3-108">Число объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="a0bf3-108">The number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0bf3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0bf3-109">Return value</span></span>

<span data-ttu-id="a0bf3-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a0bf3-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0bf3-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a0bf3-111">Requirements</span></span>



| <span data-ttu-id="a0bf3-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a0bf3-112">Requirement</span></span> | <span data-ttu-id="a0bf3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a0bf3-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bf3-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0bf3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a0bf3-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a0bf3-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a0bf3-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0bf3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a0bf3-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a0bf3-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a0bf3-118">Header</span><span class="sxs-lookup"><span data-stu-id="a0bf3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0bf3-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a0bf3-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a0bf3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a0bf3-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0bf3-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0bf3-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a0bf3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0bf3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bf3-123">**инканалисисрекогнизерс**</span><span class="sxs-lookup"><span data-stu-id="a0bf3-123">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="a0bf3-124">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="a0bf3-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




