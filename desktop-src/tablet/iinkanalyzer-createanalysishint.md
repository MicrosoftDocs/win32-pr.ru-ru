---
description: Добавляет новый узел указания анализа с бесконечной областью в Иинканализер.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'Метод Иинканализер:: Креатеаналисишинт (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343705"
---
# <a name="iinkanalyzercreateanalysishint-method"></a><span data-ttu-id="408c7-103">Метод Иинканализер:: Креатеаналисишинт</span><span class="sxs-lookup"><span data-stu-id="408c7-103">IInkAnalyzer::CreateAnalysisHint method</span></span>

<span data-ttu-id="408c7-104">Добавляет новый узел указания анализа с бесконечной областью в [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="408c7-104">Adds a new analysis hint node with an infinite area to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="408c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="408c7-105">Syntax</span></span>


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="408c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="408c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="408c7-107">*ппаналисишинт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="408c7-107">*ppAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="408c7-108">Новый узел указания по анализу.</span><span class="sxs-lookup"><span data-stu-id="408c7-108">The new analysis hint node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="408c7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="408c7-109">Return value</span></span>

<span data-ttu-id="408c7-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md) .</span><span class="sxs-lookup"><span data-stu-id="408c7-110">See [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) for a description of the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="408c7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="408c7-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="408c7-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппаналисишинт* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="408c7-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHint* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="408c7-113">Чтобы предоставить дополнительные сведения о контексте для [**иинканализер**](iinkanalyzer.md), можно добавить в анализатор рукописного ввода указания по анализу.</span><span class="sxs-lookup"><span data-stu-id="408c7-113">To provide extra context information for the [**IInkAnalyzer**](iinkanalyzer.md), you can add analysis hints to the ink analyzer.</span></span> <span data-ttu-id="408c7-114">Указания по анализу могут улучшить точность распознавания.</span><span class="sxs-lookup"><span data-stu-id="408c7-114">Analysis hints can improve recognition accuracy.</span></span> <span data-ttu-id="408c7-115">Например, можно добавить фактоид и справочные сведения для полей в приложении-форме.</span><span class="sxs-lookup"><span data-stu-id="408c7-115">For example, you can add factoid and guide information for fields in a form application.</span></span>

<span data-ttu-id="408c7-116">Этот метод создает новый [**иконтекстноде**](icontextnode.md) с типом узла контекста аналисишинт (см [**. Иконтекстноде:: GetType**](icontextnode-gettype.md)) и добавляет новое указание в качестве подузла корневого узла объекта [**Иинканализер**](iinkanalyzer.md) (см. раздел [**иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) и [**иинканализер:: GetRootNode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="408c7-116">This method creates a new [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)) and adds the new hint as a subnode of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="408c7-117">Чтобы добавить сведения о контексте в указание, используйте [**иконтекстноде:: аддпропертидата**](icontextnode-addpropertydata.md) с параметром *ппропертидатаид* , равным одной из констант [свойств указания анализа](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="408c7-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="408c7-118">Если подсказке присвоена неограниченная область, которая называется глобальным указанием, [**иинканализер**](iinkanalyzer.md) применяет контекст подсказки ко всем рукописным данным, не находящихся в области другого подсказки.</span><span class="sxs-lookup"><span data-stu-id="408c7-118">If a hint is assigned an infinite area, termed a global hint, the [**IInkAnalyzer**](iinkanalyzer.md) applies the hint's context to all ink that is not within another hint's area.</span></span> <span data-ttu-id="408c7-119">Несколько подсказок могут быть присоединены к одному **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="408c7-119">Multiple hints may be attached to a single **IInkAnalyzer**.</span></span> <span data-ttu-id="408c7-120">Однако только одно глобальное указание может быть присоединено к одному анализатору рукописного ввода, а неглобальные подсказки могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="408c7-120">However, only one global hint can be attached to a single ink analyzer, and no non-global hints can overlap.</span></span> <span data-ttu-id="408c7-121">Дополнительные сведения о типах контекстных данных, которые может предоставить подсказка, см. в разделе [Свойства указания анализа](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="408c7-121">For more information about the types of context information that a hint can provide, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="408c7-122">Добавление подсказки анализа не помечает область подсказки для переанализа.</span><span class="sxs-lookup"><span data-stu-id="408c7-122">Adding an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="408c7-123">Чтобы пометить область в подсказке для переанализа, используйте [**метод иинканализер:: сетдиртирегион**](iinkanalyzer-setdirtyregion.md) , чтобы задать для "грязной" области объединение текущей "грязной" области и области указания по анализу.</span><span class="sxs-lookup"><span data-stu-id="408c7-123">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="408c7-124">При использовании подсказок для приложения формы приложение должно избегать смешивания текстового контекста с рукописными данными в формах.</span><span class="sxs-lookup"><span data-stu-id="408c7-124">When using hints for a form application, the application should avoid mixing text context with ink in the forms.</span></span> <span data-ttu-id="408c7-125">Это означает, например, что имена текстовых полей не должны создаваться в дереве анализа.</span><span class="sxs-lookup"><span data-stu-id="408c7-125">This means for example that text field names should not be created in the analysis tree.</span></span> <span data-ttu-id="408c7-126">Указания предназначены для связывания рукописного ввода с областями на страницах. любой контекст текста мешает сопоставлению с рукописным указанием.</span><span class="sxs-lookup"><span data-stu-id="408c7-126">Hints are meant to associate the ink to areas on pages; any text context interferes with this ink-to-hint association.</span></span> <span data-ttu-id="408c7-127">Операция анализа может объединить рукописный ввод и текстовый контекст в одном регионе для записи, что не позволит связать рукописный ввод с областью подсказки.</span><span class="sxs-lookup"><span data-stu-id="408c7-127">The analysis operation may merge the ink and the text context in the same writing region which would prevent the ink from being associated with the hint area.</span></span>

<span data-ttu-id="408c7-128">Дополнительные сведения о анализе рукописного ввода см. в разделе [Общие сведения об анализе рукописного текста](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="408c7-128">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="408c7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="408c7-129">Requirements</span></span>



| <span data-ttu-id="408c7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="408c7-130">Requirement</span></span> | <span data-ttu-id="408c7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="408c7-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="408c7-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="408c7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="408c7-133">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="408c7-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="408c7-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="408c7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="408c7-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="408c7-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="408c7-136">Header</span><span class="sxs-lookup"><span data-stu-id="408c7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="408c7-137"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="408c7-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="408c7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="408c7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="408c7-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="408c7-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="408c7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="408c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="408c7-141">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="408c7-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="408c7-142">**Иконтекстноде:: Аддпропертидата**</span><span class="sxs-lookup"><span data-stu-id="408c7-142">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="408c7-143">**Иинканализер: метод:D Елетеаналисишинт**</span><span class="sxs-lookup"><span data-stu-id="408c7-143">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="408c7-144">**Метод Иинканализер:: Жетаналисишинтс**</span><span class="sxs-lookup"><span data-stu-id="408c7-144">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="408c7-145">**Метод Иинканализер:: Жетаналисишинтсбинаме**</span><span class="sxs-lookup"><span data-stu-id="408c7-145">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="408c7-146">Свойства указания по анализу</span><span class="sxs-lookup"><span data-stu-id="408c7-146">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="408c7-147">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="408c7-147">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

