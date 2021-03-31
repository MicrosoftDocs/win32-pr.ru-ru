---
description: 'Определяет глобальные уникальные идентификаторы (GUID) для свойств узла указания по анализу (см. Иконтекстноде:: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Свойства указания по анализу (Иагуид. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990825"
---
# <a name="analysis-hint-properties"></a><span data-ttu-id="9ce65-103">Свойства указания по анализу</span><span class="sxs-lookup"><span data-stu-id="9ce65-103">Analysis Hint Properties</span></span>

<span data-ttu-id="9ce65-104">Определяет глобальные уникальные идентификаторы (GUID) для свойств узла указания по анализу (см. [**иконтекстноде:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="9ce65-104">Defines globally unique identifiers (GUIDs) for properties of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="9ce65-105">В следующей таблице описаны сведения, на которые ссылается Каждая константа.</span><span class="sxs-lookup"><span data-stu-id="9ce65-105">The following table describes information referenced by each constant.</span></span>



| <span data-ttu-id="9ce65-106">Константа</span><span class="sxs-lookup"><span data-stu-id="9ce65-106">Constant</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="9ce65-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9ce65-107">Description</span></span>                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <span data-ttu-id="9ce65-108"><dt>**GUID \_ ахп \_ алловпартиалдиктионаритермс**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-108"><dt>**GUID\_AHP\_ALLOWPARTIALDICTIONARYTERMS**</dt></span></span> </dl>       | <span data-ttu-id="9ce65-109">Разрешены ли в подсказке анализа частичные словарные термины.</span><span class="sxs-lookup"><span data-stu-id="9ce65-109">Whether partial dictionary terms are allowed on an analysis hint.</span></span><br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <span data-ttu-id="9ce65-110"><dt>**GUID \_ ахп \_ аналисишинтнаме**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-110"><dt>**GUID\_AHP\_ANALYSISHINTNAME**</dt></span></span> </dl>                                        | <span data-ttu-id="9ce65-111">Имя подсказки анализа.</span><span class="sxs-lookup"><span data-stu-id="9ce65-111">The name of an analysis hint.</span></span><br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <span data-ttu-id="9ce65-112"><dt>**GUID \_ ахп \_ коерцетофактоид**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-112"><dt>**GUID\_AHP\_COERCETOFACTOID**</dt></span></span> </dl>                                           | <span data-ttu-id="9ce65-113">Ограничивается ли анализатором рукописного ввода анализ рукописных данных в области подсказки для соответствия фактоид.</span><span class="sxs-lookup"><span data-stu-id="9ce65-113">Whether the ink analyzer limits its analysis of ink within the hint's area to conform to the factoid.</span></span><br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <span data-ttu-id="9ce65-114"><dt>**GUID \_ ахп \_ енабледуникодечарактерранжес**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-114"><dt>**GUID\_AHP\_ENABLEDUNICODECHARACTERRANGES**</dt></span></span> </dl> | <span data-ttu-id="9ce65-115">Указание содержит массив символов, который представляет ограниченный набор поддерживаемых символов Юникода, поддерживаемый данным Инкрекогнизер.</span><span class="sxs-lookup"><span data-stu-id="9ce65-115">The hint contains an array of characters that represent the restricted set of supported unicode character set supported by this InkRecognizer.</span></span><br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <span data-ttu-id="9ce65-116"><dt>**GUID \_ ахп \_ фактоид**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-116"><dt>**GUID\_AHP\_FACTOID**</dt></span></span> </dl>                                                                   | <span data-ttu-id="9ce65-117">Фактоид в подсказке анализа.</span><span class="sxs-lookup"><span data-stu-id="9ce65-117">The factoid on an analysis hint.</span></span><br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <span data-ttu-id="9ce65-118"><dt>**\_ \_ руководство по ахп GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-118"><dt>**GUID\_AHP\_GUIDE**</dt></span></span> </dl>                                                                         | <span data-ttu-id="9ce65-119">Структура [**инканалисисрекогнизергуиде**](inkanalysisrecognizerguide.md) , представляющая собой руководством для указания по анализу.</span><span class="sxs-lookup"><span data-stu-id="9ce65-119">The [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) structure that represents the guide for an analysis hint.</span></span><br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <span data-ttu-id="9ce65-120"><dt>**GUID \_ ахп \_ префикстекст**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-120"><dt>**GUID\_AHP\_PREFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="9ce65-121">Текст префикса для указания анализа.</span><span class="sxs-lookup"><span data-stu-id="9ce65-121">The prefix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <span data-ttu-id="9ce65-122"><dt>**GUID \_ ахп \_ суффикстекст**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-122"><dt>**GUID\_AHP\_SUFFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="9ce65-123">Текст суффикса в подсказке анализа.</span><span class="sxs-lookup"><span data-stu-id="9ce65-123">The suffix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <span data-ttu-id="9ce65-124"><dt>**GUID \_ ахп \_ топинкбреаксонли**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-124"><dt>**GUID\_AHP\_TOPINKBREAKSONLY**</dt></span></span> </dl>                                        | <span data-ttu-id="9ce65-125">Отключаются ли множественные сегменты в результатах распознавания рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="9ce65-125">Whether the multiple segmentations in the ink recognition results are disabled.</span></span><br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <span data-ttu-id="9ce65-126"><dt>**GUID \_ ахп \_ список слов**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-126"><dt>**GUID\_AHP\_WORDLIST**</dt></span></span> </dl>                                                                | <span data-ttu-id="9ce65-127">Массив строк, представляющий список слов для указания анализа.</span><span class="sxs-lookup"><span data-stu-id="9ce65-127">The array of strings that represents the word list for an analysis hint.</span></span><br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <span data-ttu-id="9ce65-128"><dt>**GUID \_ ахп \_ вордмоде**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-128"><dt>**GUID\_AHP\_WORDMODE**</dt></span></span> </dl>                                                                | <span data-ttu-id="9ce65-129">Определяет, следует ли анализатору рукописного ввода определять приоритеты отдельных слов по нескольким словам для указания анализа.</span><span class="sxs-lookup"><span data-stu-id="9ce65-129">Whether the ink analyzer prioritizes single-word results over multiple-word results for an analysis hint.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="9ce65-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ce65-130">Remarks</span></span>

<span data-ttu-id="9ce65-131">Эти идентификаторы GUID используются для указания свойств, которые [**иинканализер**](iinkanalyzer.md) может установить для узла контекста указания анализа (см. раздел [**Иконтекстноде:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="9ce65-131">These GUIDs are used to identify properties that the [**IInkAnalyzer**](iinkanalyzer.md) can set on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="9ce65-132">Сведения о получении или задании свойств [**иконтекстноде**](icontextnode.md) в целом см. в разделе [Свойства узла контекста](context-node-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9ce65-132">To get or set properties of an [**IContextNode**](icontextnode.md) in general, see [Context Node Properties](context-node-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce65-133">Требования</span><span class="sxs-lookup"><span data-stu-id="9ce65-133">Requirements</span></span>



| <span data-ttu-id="9ce65-134">Требование</span><span class="sxs-lookup"><span data-stu-id="9ce65-134">Requirement</span></span> | <span data-ttu-id="9ce65-135">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce65-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce65-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ce65-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce65-137">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9ce65-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9ce65-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ce65-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce65-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9ce65-139">None supported</span></span><br/>                                                           |
| <span data-ttu-id="9ce65-140">Header</span><span class="sxs-lookup"><span data-stu-id="9ce65-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ce65-141"><dt>Иагуид. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce65-141"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce65-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ce65-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce65-143">Свойства узла контекста</span><span class="sxs-lookup"><span data-stu-id="9ce65-143">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="9ce65-144">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="9ce65-144">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="9ce65-145">**Метод Иинканализер:: Креатеаналисишинт**</span><span class="sxs-lookup"><span data-stu-id="9ce65-145">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="9ce65-146">**Метод Иинканализер:: Жетаналисишинтсбинаме**</span><span class="sxs-lookup"><span data-stu-id="9ce65-146">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="9ce65-147">**Иконтекстноде:: Контаинспропертидата**</span><span class="sxs-lookup"><span data-stu-id="9ce65-147">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="9ce65-148">**Иконтекстноде:: Жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="9ce65-148">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="9ce65-149">**Иконтекстноде:: Жетпропертидатаидс**</span><span class="sxs-lookup"><span data-stu-id="9ce65-149">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="9ce65-150">**Иконтекстноде:: Лоадпропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="9ce65-150">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="9ce65-151">**Иконтекстноде:: Ремовепропертидата**</span><span class="sxs-lookup"><span data-stu-id="9ce65-151">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="9ce65-152">**Иконтекстноде:: Савепропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="9ce65-152">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="9ce65-153">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9ce65-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




