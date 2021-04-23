---
description: В этом разделе содержатся сведения об интерфейсах и классах, используемых при анализе рукописного ввода. Классы и интерфейсы анализа рукописного ввода не совместимы с автоматизацией.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Классы и интерфейсы анализа рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539938"
---
# <a name="ink-analysis-classes-and-interfaces"></a><span data-ttu-id="6e55c-104">Классы и интерфейсы анализа рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="6e55c-104">Ink Analysis Classes and Interfaces</span></span>

<span data-ttu-id="6e55c-105">В этом разделе содержатся сведения об интерфейсах и классах, используемых при анализе рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="6e55c-105">This section contains information about the interfaces and classes used in ink analysis.</span></span> <span data-ttu-id="6e55c-106">Классы и интерфейсы анализа рукописного ввода не совместимы с автоматизацией.</span><span class="sxs-lookup"><span data-stu-id="6e55c-106">The ink analysis classes and interfaces are not Automation-compliant.</span></span>

## <a name="classes"></a><span data-ttu-id="6e55c-107">Классы</span><span class="sxs-lookup"><span data-stu-id="6e55c-107">Classes</span></span>



| <span data-ttu-id="6e55c-108">Класс</span><span class="sxs-lookup"><span data-stu-id="6e55c-108">Class</span></span>                                    | <span data-ttu-id="6e55c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6e55c-109">Description</span></span>                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="6e55c-110">**аналисисрегион**</span><span class="sxs-lookup"><span data-stu-id="6e55c-110">**AnalysisRegion**</span></span>](analysisregion.md) | <span data-ttu-id="6e55c-111">Реализует интерфейс [**ианалисисрегион**](ianalysisregion.md) .</span><span class="sxs-lookup"><span data-stu-id="6e55c-111">Implements the [**IAnalysisRegion**](ianalysisregion.md) interface.</span></span><br/> |
| [<span data-ttu-id="6e55c-112">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6e55c-112">**InkAnalyzer**</span></span>](inkanalyzer.md)       | <span data-ttu-id="6e55c-113">Реализует интерфейс [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="6e55c-113">Implements the [**IInkAnalyzer**](iinkanalyzer.md) interface.</span></span><br/>       |



 

## <a name="interfaces"></a><span data-ttu-id="6e55c-114">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="6e55c-114">Interfaces</span></span>



| <span data-ttu-id="6e55c-115">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="6e55c-115">Interface</span></span>                                                    | <span data-ttu-id="6e55c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6e55c-116">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e55c-117">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="6e55c-117">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)             | <span data-ttu-id="6e55c-118">Представляет возможные совпадения слов распознавания рукописного текста для объектов [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="6e55c-118">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span><br/>                                                                                        |
| [<span data-ttu-id="6e55c-119">**ианалисисалтернатес**</span><span class="sxs-lookup"><span data-stu-id="6e55c-119">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)           | <span data-ttu-id="6e55c-120">Содержит коллекцию объектов, реализующих интерфейс [**ианалисисалтернате**](ianalysisalternate.md) и являющихся результатом анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="6e55c-120">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span><br/>                                               |
| [<span data-ttu-id="6e55c-121">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="6e55c-121">**IAnalysisRegion**</span></span>](ianalysisregion.md)                   | <span data-ttu-id="6e55c-122">Предоставляет методы и свойства для региона, представляющего область документа.</span><span class="sxs-lookup"><span data-stu-id="6e55c-122">Exposes methods and properties for a region that represents an area of a document.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="6e55c-123">**ианалисисстатус**</span><span class="sxs-lookup"><span data-stu-id="6e55c-123">**IAnalysisStatus**</span></span>](ianalysisstatus.md)                   | <span data-ttu-id="6e55c-124">Представляет состояние операции анализа рукописного ввода, описывая, успешно ли был выполнен анализ и возникли ли какие либо предупреждения.</span><span class="sxs-lookup"><span data-stu-id="6e55c-124">Represents the status of the ink analysis operation by describing whether the analysis was completed successfully and whether any warnings occurred.</span></span><br/>                                                  |
| [<span data-ttu-id="6e55c-125">**ианалисисварнинг**</span><span class="sxs-lookup"><span data-stu-id="6e55c-125">**IAnalysisWarning**</span></span>](ianalysiswarning.md)                 | <span data-ttu-id="6e55c-126">Представляет предупреждение или ошибку, возникающую во время операции анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="6e55c-126">Represents a warning or error that occurs during an ink analysis operation.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="6e55c-127">**ианалисисварнингс**</span><span class="sxs-lookup"><span data-stu-id="6e55c-127">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)               | <span data-ttu-id="6e55c-128">Содержит коллекцию объектов, реализующих интерфейс [**ианалисисварнинг**](ianalysiswarning.md) и являющихся результатом операции анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="6e55c-128">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span><br/>                                      |
| [<span data-ttu-id="6e55c-129">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="6e55c-129">**IContextLink**</span></span>](icontextlink.md)                         | <span data-ttu-id="6e55c-130">Представляет связь между двумя объектами [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="6e55c-130">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="6e55c-131">**иконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="6e55c-131">**IContextLinks**</span></span>](icontextlinks.md)                       | <span data-ttu-id="6e55c-132">Содержит коллекцию объектов, реализующих интерфейс [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="6e55c-132">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="6e55c-133">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="6e55c-133">**IContextNode**</span></span>](icontextnode.md)                         | <span data-ttu-id="6e55c-134">Представляет узел в дереве объектов, созданных в ходе анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="6e55c-134">Represents a node in a tree of objects that are created as part of ink analysis.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="6e55c-135">**иконтекстнодес**</span><span class="sxs-lookup"><span data-stu-id="6e55c-135">**IContextNodes**</span></span>](icontextnodes.md)                       | <span data-ttu-id="6e55c-136">Содержит коллекцию объектов, реализующих интерфейс [**иконтекстноде**](icontextnode.md) и являющихся результатом операции анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="6e55c-136">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span><br/>                                              |
| [<span data-ttu-id="6e55c-137">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="6e55c-137">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)     | <span data-ttu-id="6e55c-138">Предоставляет доступ к распознавателям рукописного ввода для использования с анализом рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="6e55c-138">Provides access to handwriting recognizers for use with ink analysis.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="6e55c-139">**иинканалисисрекогнизерс**</span><span class="sxs-lookup"><span data-stu-id="6e55c-139">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)   | <span data-ttu-id="6e55c-140">Содержит коллекцию объектов, реализующих интерфейс [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) и представляющих возможность распознавания рукописного текста, объектов или жестов.</span><span class="sxs-lookup"><span data-stu-id="6e55c-140">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span><br/> |
| [<span data-ttu-id="6e55c-141">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="6e55c-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)                         | <span data-ttu-id="6e55c-142">Предоставляет доступ к анализу макета, разметке, классификации и распознаванию рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="6e55c-142">Provides access to layout analysis, writing and drawing classification, and handwriting recognition.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="6e55c-143">**иматческритериакаллбакк**</span><span class="sxs-lookup"><span data-stu-id="6e55c-143">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md) | <span data-ttu-id="6e55c-144">Предоставляет метод для определения того, соответствует ли объект [**иконтекстноде**](icontextnode.md) или завершается с указанными критериями.</span><span class="sxs-lookup"><span data-stu-id="6e55c-144">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span><br/>                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="6e55c-145">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6e55c-145">Return Values</span></span>

<span data-ttu-id="6e55c-146">Методы в библиотеке COM на платформе Tablet PC возвращают значения **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6e55c-146">Methods in the Tablet PC COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="6e55c-147">Если не указано иное, в этой таблице описаны значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e55c-147">Unless otherwise noted, the meanings of the **HRESULT** values are described in this table.</span></span>



| <span data-ttu-id="6e55c-148">Значение HRESULT</span><span class="sxs-lookup"><span data-stu-id="6e55c-148">HRESULT value</span></span>                                   | <span data-ttu-id="6e55c-149">Описание</span><span class="sxs-lookup"><span data-stu-id="6e55c-149">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e55c-150">\_ОК</span><span class="sxs-lookup"><span data-stu-id="6e55c-150">S\_OK</span></span><br/>                                | <span data-ttu-id="6e55c-151">Успешно.</span><span class="sxs-lookup"><span data-stu-id="6e55c-151">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="6e55c-152">\_указатель E</span><span class="sxs-lookup"><span data-stu-id="6e55c-152">E\_POINTER</span></span><br/>                           | <span data-ttu-id="6e55c-153">По крайней мере один указатель (для входного или выходного параметра) является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="6e55c-153">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="6e55c-154">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="6e55c-154">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="6e55c-155">Член попытался передать недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="6e55c-155">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="6e55c-156">\_исключение рукописного ввода \_</span><span class="sxs-lookup"><span data-stu-id="6e55c-156">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="6e55c-157">Возникло исключение.</span><span class="sxs-lookup"><span data-stu-id="6e55c-157">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="6e55c-158">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="6e55c-158">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="6e55c-159">Системе не удается выделить память для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="6e55c-159">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="6e55c-160">\_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="6e55c-160">E\_FAIL</span></span><br/>                              | <span data-ttu-id="6e55c-161">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6e55c-161">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="6e55c-162">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="6e55c-162">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="6e55c-163">Член попытался использовать недопустимую операцию.</span><span class="sxs-lookup"><span data-stu-id="6e55c-163">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="6e55c-164">\_ \_ Недопустимый \_ режим TPC E</span><span class="sxs-lookup"><span data-stu-id="6e55c-164">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="6e55c-165">Член попытался использовать недопустимый режим.</span><span class="sxs-lookup"><span data-stu-id="6e55c-165">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="6e55c-166">TPC \_ E \_ Недопустимая \_ Конфигурация</span><span class="sxs-lookup"><span data-stu-id="6e55c-166">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="6e55c-167">Член попытался использовать недопустимую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="6e55c-167">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="6e55c-168">\_ \_ Описание недействительного пакета TPC E \_ \_</span><span class="sxs-lookup"><span data-stu-id="6e55c-168">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="6e55c-169">Член попытался использовать недопустимое описание пакета.</span><span class="sxs-lookup"><span data-stu-id="6e55c-169">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="6e55c-170">См. также</span><span class="sxs-lookup"><span data-stu-id="6e55c-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e55c-171">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="6e55c-171">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




