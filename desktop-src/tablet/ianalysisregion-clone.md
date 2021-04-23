---
description: Создает копию Ианалисисрегион.
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: 'Метод Ианалисисрегион:: Clone (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fb069ddb461ab4422f8cbbc8990fb6d735808e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692455"
---
# <a name="ianalysisregionclone-method"></a><span data-ttu-id="efe8b-103">Метод Ианалисисрегион:: Clone</span><span class="sxs-lookup"><span data-stu-id="efe8b-103">IAnalysisRegion::Clone method</span></span>

<span data-ttu-id="efe8b-104">Создает копию [**ианалисисрегион**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="efe8b-104">Creates a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="efe8b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efe8b-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="efe8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efe8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe8b-107">*пклонедрегион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="efe8b-107">*pClonedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efe8b-108">Указатель на копию [**ианалисисрегион**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="efe8b-108">A pointer to a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe8b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efe8b-109">Return value</span></span>

<span data-ttu-id="efe8b-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="efe8b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="efe8b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efe8b-111">Remarks</span></span>

<span data-ttu-id="efe8b-112">Этот метод екивалент в метод Сесистем. Windows. Ink. Аналисискоре. Аналисисрегионбасе. Clone в платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="efe8b-112">This method is eqivalent to theSystem.Windows.Ink.AnalysisCore.AnalysisRegionBase.Clone Method in the .NET Framework.</span></span>

> [!Caution]  
> <span data-ttu-id="efe8b-113">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *пклонедрегион* , когда больше не нужно использовать клонированный регион анализа.</span><span class="sxs-lookup"><span data-stu-id="efe8b-113">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pClonedRegion* when you no longer need to use the cloned analysis region.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="efe8b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="efe8b-114">Requirements</span></span>



| <span data-ttu-id="efe8b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="efe8b-115">Requirement</span></span> | <span data-ttu-id="efe8b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="efe8b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efe8b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efe8b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="efe8b-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="efe8b-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="efe8b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efe8b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="efe8b-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="efe8b-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="efe8b-121">Header</span><span class="sxs-lookup"><span data-stu-id="efe8b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="efe8b-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="efe8b-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="efe8b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="efe8b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efe8b-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efe8b-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="efe8b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efe8b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe8b-126">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="efe8b-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="efe8b-127">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="efe8b-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

