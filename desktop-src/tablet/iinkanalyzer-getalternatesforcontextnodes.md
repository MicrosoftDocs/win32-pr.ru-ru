---
description: Извлекает варианты анализа для узлов в указанной коллекции Иконтекстнодес.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'Метод Иинканализер:: Жеталтернатесфорконтекстнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145466"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a><span data-ttu-id="d0c1a-103">Метод Иинканализер:: Жеталтернатесфорконтекстнодес</span><span class="sxs-lookup"><span data-stu-id="d0c1a-103">IInkAnalyzer::GetAlternatesForContextNodes method</span></span>

<span data-ttu-id="d0c1a-104">Извлекает варианты анализа для узлов в указанной коллекции [**иконтекстнодес**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="d0c1a-104">Retrieves analysis alternates for the nodes in a specified [**IContextNodes**](icontextnodes.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0c1a-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="d0c1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0c1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c1a-107">*пконтекстнодес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0c1a-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c1a-108">Коллекция [**иконтекстнодес**](icontextnodes.md) , для которой возвращаются альтернативные варианты анализа.</span><span class="sxs-lookup"><span data-stu-id="d0c1a-108">The [**IContextNodes**](icontextnodes.md) collection for which the analysis alternatives are returned.</span></span>

</dd> <dt>

<span data-ttu-id="d0c1a-109">*улмаксимумалтернатес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0c1a-109">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c1a-110">Максимальное число возвращаемых вариантов.</span><span class="sxs-lookup"><span data-stu-id="d0c1a-110">The maximum number of alternatives to return.</span></span>

</dd> <dt>

<span data-ttu-id="d0c1a-111">*ппалтернатес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d0c1a-111">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c1a-112">Объект [**ианалисисалтернатес**](ianalysisalternates.md) , содержащий альтернативные варианты анализа.</span><span class="sxs-lookup"><span data-stu-id="d0c1a-112">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c1a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0c1a-113">Return value</span></span>

<span data-ttu-id="d0c1a-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d0c1a-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0c1a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0c1a-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d0c1a-116">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппалтернатес* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="d0c1a-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="d0c1a-117">Top [**ианалисисалтернате**](ianalysisalternate.md) возвращается в качестве первой альтернативы коллекции.</span><span class="sxs-lookup"><span data-stu-id="d0c1a-117">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="d0c1a-118">Объекты [**иконтекстноде**](icontextnode.md) в *пконтекстнодес* не должны представлять смежные области документа.</span><span class="sxs-lookup"><span data-stu-id="d0c1a-118">The [**IContextNode**](icontextnode.md) objects in *pContextNodes* do not have to represent adjacent areas of the document.</span></span>

<span data-ttu-id="d0c1a-119">Для каждой подсказки по анализу в узлах [**иинканализер**](iinkanalyzer.md) возвращает только верхний альтернативный вариант.</span><span class="sxs-lookup"><span data-stu-id="d0c1a-119">For each analysis hint in nodes, the [**IInkAnalyzer**](iinkanalyzer.md) returns only the top alternate.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c1a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d0c1a-120">Requirements</span></span>



| <span data-ttu-id="d0c1a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d0c1a-121">Requirement</span></span> | <span data-ttu-id="d0c1a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d0c1a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c1a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0c1a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c1a-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d0c1a-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d0c1a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0c1a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c1a-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d0c1a-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d0c1a-127">Header</span><span class="sxs-lookup"><span data-stu-id="d0c1a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0c1a-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d0c1a-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d0c1a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d0c1a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0c1a-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0c1a-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d0c1a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0c1a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c1a-132">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="d0c1a-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d0c1a-133">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="d0c1a-133">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="d0c1a-134">**ианалисисалтернатес**</span><span class="sxs-lookup"><span data-stu-id="d0c1a-134">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="d0c1a-135">**Метод Иинканализер:: Alternate**</span><span class="sxs-lookup"><span data-stu-id="d0c1a-135">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="d0c1a-136">**Метод Иинканализер:: Жеталтернатесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="d0c1a-136">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="d0c1a-137">**Метод Иинканализер:: Модифитопалтернате**</span><span class="sxs-lookup"><span data-stu-id="d0c1a-137">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="d0c1a-138">**Метод Иинканализер:: Модифитопалтернатевисконфирматион**</span><span class="sxs-lookup"><span data-stu-id="d0c1a-138">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="d0c1a-139">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="d0c1a-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

