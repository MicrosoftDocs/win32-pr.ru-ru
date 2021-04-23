---
description: Задает набор доступных предупреждений, которые могут возникнуть во время анализа рукописного ввода.
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: Перечисление Аналисисварнингкоде (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisWarningCode
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 651408678daa64788952b2706980968ca315abf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663555"
---
# <a name="analysiswarningcode-enumeration"></a><span data-ttu-id="97483-103">Перечисление Аналисисварнингкоде</span><span class="sxs-lookup"><span data-stu-id="97483-103">AnalysisWarningCode enumeration</span></span>

<span data-ttu-id="97483-104">Задает набор доступных предупреждений, которые могут возникнуть во время анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="97483-104">Specifies the set of available warnings that can occur during ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="97483-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97483-105">Syntax</span></span>


```C++
typedef enum AnalysisWarningCode { 
  AnalysisWarningCode_Aborted                                    = 0,
  AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound       = 1,
  AnalysisWarningCode_FactoidNotSupported                        = 2,
  AnalysisWarningCode_FactoidCoercionNotSupported                = 3,
  AnalysisWarningCode_GuideNotSupported                          = 4,
  AnalysisWarningCode_WordlistNotSupported                       = 5,
  AnalysisWarningCode_WordModeNotSupported                       = 6,
  AnalysisWarningCode_PartialDictionaryTermsNotSupported         = 7,
  AnalysisWarningCode_TextRecognitionProcessFailed               = 8,
  AnalysisWarningCode_AddInkToRecognizerFailed                   = 9,
  AnalysisWarningCode_SetPrefixSuffixFailed                      = 10,
  AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed  = 11,
  AnalysisWarningCode_ConfirmedWithoutInkRecognition             = 12,
  AnalysisWarningCode_BackgroundException                        = 13,
  AnalysisWarningCode_ContextNodeLocationNotSet                  = 14,
  AnalysisWarningCode_LanguageIdNotRespected                     = 15,
  AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported   = 16,
  AnalysisWarningCode_TopInkBreaksOnlyNotSupported               = 17,
  AnalysisWarningCode_AnalysisAlreadyRunning                     = 18
} AnalysisWarningCode;
```



## <a name="constants"></a><span data-ttu-id="97483-106">Константы</span><span class="sxs-lookup"><span data-stu-id="97483-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="97483-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**Аналисисварнингкоде \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="97483-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode\_Aborted**</span></span>
</dt> <dd>

<span data-ttu-id="97483-108">Операция анализа прервана.</span><span class="sxs-lookup"><span data-stu-id="97483-108">The analysis operation was aborted.</span></span>

<span data-ttu-id="97483-109">Возвращается только при вызове операции синхронного анализа.</span><span class="sxs-lookup"><span data-stu-id="97483-109">Returned only when the synchronous analysis operation is called.</span></span> <span data-ttu-id="97483-110">Прерывание асинхронной операции не вызовет событие [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="97483-110">Aborting an asynchronous operation will not raise an [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="97483-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**Аналисисварнингкоде \_ номатчингинканалисисрекогнизерфаунд**</span><span class="sxs-lookup"><span data-stu-id="97483-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**</span></span>
</dt> <dd>

<span data-ttu-id="97483-112">[**Иинканализер**](iinkanalyzer.md) не удается найти распознаватель рукописного ввода, который соответствует требованиям к языку или возможности, необходимым для выполнения операции анализа.</span><span class="sxs-lookup"><span data-stu-id="97483-112">The [**IInkAnalyzer**](iinkanalyzer.md) cannot find an ink recognizer that meets language or capability requirements needed to perform the analysis operation.</span></span>

</dd> <dt>

<span data-ttu-id="97483-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**Аналисисварнингкоде \_ фактоиднотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="97483-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="97483-114">Распознаватель рукописного ввода не смог соблюдать указанный набор фактоид на узле указания по анализу (см. раздел свойства указания [**иконтекстноде:: GetType**](icontextnode-gettype.md) и указания по [анализу](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="97483-114">The ink recognizer was unable to respect the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="97483-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**Аналисисварнингкоде \_ фактоидкоерЦионнотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="97483-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidCoercionNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="97483-116">Распознаватель рукописного ввода не смог привести свои результаты к указанному фактоид в узле указания по анализу (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md) и свойства указания по [анализу](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="97483-116">The ink recognizer was unable to coerce its results to the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="97483-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**Аналисисварнингкоде \_ гуиденотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="97483-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode\_GuideNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="97483-118">Распознаватель рукописного ввода не смог соблюдать указанный набор руководств на узле указания по анализу (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md) и свойства указания по [анализу](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="97483-118">The ink recognizer was unable to respect the specified guide set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="97483-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**Аналисисварнингкоде \_ вордлистнотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="97483-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode\_WordlistNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="97483-120">Распознаватель рукописного ввода не смог соблюдать указанный набор списков слов на узле указания по анализу (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md) и свойства указания по [анализу](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="97483-120">The ink recognizer was unable to respect the specified word list set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="97483-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**Аналисисварнингкоде \_ вордмоденотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="97483-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode\_WordModeNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="97483-122">Распознаватель рукописного ввода не смог проанализировать указанный режим Word на узле указания по анализу (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md) и свойства указания по [анализу](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="97483-122">The ink recognizer was unable to respect the specified word mode set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="97483-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**Аналисисварнингкоде \_ партиалдиктионаритермснотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="97483-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode\_PartialDictionaryTermsNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="97483-124">Указывает, что часть словарных терминов не может быть возвращена из [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="97483-124">Indicates that partial dictionary terms could not be returned from the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="97483-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**Аналисисварнингкоде \_ текстрекогнитионпроцессфаилед**</span><span class="sxs-lookup"><span data-stu-id="97483-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode\_TextRecognitionProcessFailed**</span></span>
</dt> <dd>

<span data-ttu-id="97483-126">Указывает, что процесс распознавания текста завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="97483-126">Indicates the text recognition process failed.</span></span>

</dd> <dt>

<span data-ttu-id="97483-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**Аналисисварнингкоде \_ аддинкторекогнизерфаилед**</span><span class="sxs-lookup"><span data-stu-id="97483-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode\_AddInkToRecognizerFailed**</span></span>
</dt> <dd>

<span data-ttu-id="97483-128">Не удалось добавить рукописный ввод в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="97483-128">The ink could not be added to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="97483-129">Например, добавление штрихов, собираемых с помощью мыши в распознавателе жестов, завершится ошибкой, так как для распознавателя жестов требуются штрихи, полученные от дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="97483-129">For example, adding strokes collected from a mouse on a gesture recognizer will fail, as the gesture recognizer requires strokes collected from a digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="97483-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**Аналисисварнингкоде \_ сетпрефикссуффиксфаилед**</span><span class="sxs-lookup"><span data-stu-id="97483-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode\_SetPrefixSuffixFailed**</span></span>
</dt> <dd>

<span data-ttu-id="97483-131">[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) не удалось сособлюдать указанный префикс или текст суффикса узла указания анализа (см. раздел [Свойства подсказки](analysis-hint-properties.md) [**Иконтекстноде:: GetType**](icontextnode-gettype.md) и Analysis).</span><span class="sxs-lookup"><span data-stu-id="97483-131">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) was unable to respect the specified prefix or suffix text of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="97483-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**Аналисисварнингкоде \_ инканалисисрекогнизеринитиализатионфаилед**</span><span class="sxs-lookup"><span data-stu-id="97483-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed**</span></span>
</dt> <dd>

<span data-ttu-id="97483-133">[**Иинканализер**](iinkanalyzer.md) не удалось создать, клонировать или задать штрихи в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="97483-133">The [**IInkAnalyzer**](iinkanalyzer.md) was not able to instantiate, clone, or set strokes on the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="97483-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**Аналисисварнингкоде \_ конфирмедвисаутинкрекогнитион**</span><span class="sxs-lookup"><span data-stu-id="97483-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode\_ConfirmedWithoutInkRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="97483-135">Указывает, что объект [**иконтекстноде**](icontextnode.md) подтвержден пользователем, но не имеет значений распознавания, вычисленных для узла.</span><span class="sxs-lookup"><span data-stu-id="97483-135">Indicates that an [**IContextNode**](icontextnode.md) object has been confirmed by the user without having any recognition values computed for the node.</span></span>

</dd> <dt>

<span data-ttu-id="97483-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**Аналисисварнингкоде \_ баккграундексцептион**</span><span class="sxs-lookup"><span data-stu-id="97483-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode\_BackgroundException**</span></span>
</dt> <dd>

<span data-ttu-id="97483-137">Фоновая операция не была завершена из-за исключения.</span><span class="sxs-lookup"><span data-stu-id="97483-137">The background operation did not complete due to an exception.</span></span> <span data-ttu-id="97483-138">Это неустранимая ошибка, которая требует повторного создания экземпляра [**иинканализер**](iinkanalyzer.md) перед дальнейшим использованием.</span><span class="sxs-lookup"><span data-stu-id="97483-138">This is a fatal error and requires that the [**IInkAnalyzer**](iinkanalyzer.md) is re-instantiated before further use.</span></span>

</dd> <dt>

<span data-ttu-id="97483-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**Аналисисварнингкоде \_ контекстноделокатионнотсет**</span><span class="sxs-lookup"><span data-stu-id="97483-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode\_ContextNodeLocationNotSet**</span></span>
</dt> <dd>

<span data-ttu-id="97483-140">Указывает, что объект [**иконтекстноде**](icontextnode.md) не имеет правильного набора местоположений (см. [**Иконтекстноде:: SetLocation**](icontextnode-setlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="97483-140">Indicates that an [**IContextNode**](icontextnode.md) object does not have a proper location set (see [**IContextNode::SetLocation**](icontextnode-setlocation.md)).</span></span> <span data-ttu-id="97483-141">Метод [**иконтекстноде::**](icontextnode-getlocation.md) GetObject должен возвращать непустое значение, если объект **иконтекстноде** не помечен как частично заполненный.</span><span class="sxs-lookup"><span data-stu-id="97483-141">The [**IContextNode::GetLocation**](icontextnode-getlocation.md) method must return a non-empty value unless the **IContextNode** object is marked as partially populated.</span></span>

</dd> <dt>

<span data-ttu-id="97483-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**Аналисисварнингкоде \_ лангуажеиднотреспектед**</span><span class="sxs-lookup"><span data-stu-id="97483-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode\_LanguageIdNotRespected**</span></span>
</dt> <dd>

<span data-ttu-id="97483-143">Идентификатор языка, заданный для штриха, связанного с узлом пользовательского распознавателя (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md)), не соответствует идентификатору языка используемого [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="97483-143">The language identifier set on a stroke associated with a custom recognizer node (see [**IContextNode::GetType**](icontextnode-gettype.md)) did not match the language identifier of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) used.</span></span> <span data-ttu-id="97483-144">Рукописный ввод по-прежнему распознан указанным **иинканалисисрекогнизер**.</span><span class="sxs-lookup"><span data-stu-id="97483-144">The ink was still recognized with the specified **IInkAnalysisRecognizer**.</span></span>

</dd> <dt>

<span data-ttu-id="97483-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**Аналисисварнингкоде \_ енаблеуникодечарактерранжеснотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="97483-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode\_EnableUnicodeCharacterRangesNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="97483-146">[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) не поддерживает включение диапазонов символов Юникода, как указано.</span><span class="sxs-lookup"><span data-stu-id="97483-146">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support enabling Unicode character ranges as specified.</span></span>

</dd> <dt>

<span data-ttu-id="97483-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**Аналисисварнингкоде \_ топинкбреаксонлинотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="97483-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode\_TopInkBreaksOnlyNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="97483-148">[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) не поддерживает топинкбреакс только в том случае, если указания содержали запрос только для топинкбреакс.</span><span class="sxs-lookup"><span data-stu-id="97483-148">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support TopInkBreaks only even though the hints contained the request for TopInkBreaks only.</span></span>

</dd> <dt>

<span data-ttu-id="97483-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**Аналисисварнингкоде \_ аналисисалреадируннинг**</span><span class="sxs-lookup"><span data-stu-id="97483-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode\_AnalysisAlreadyRunning**</span></span>
</dt> <dd>

<span data-ttu-id="97483-150">[**Иинканализер**](iinkanalyzer.md) уже выполняет фоновый анализ.</span><span class="sxs-lookup"><span data-stu-id="97483-150">The [**IInkAnalyzer**](iinkanalyzer.md) is already performing background analysis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97483-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97483-151">Remarks</span></span>

<span data-ttu-id="97483-152">**Аналисисварнингкоде \_ Баккграундексцептион** — это единственное значение кода предупреждения, которое требует повторного создания экземпляра объекта [**иинканализер**](iinkanalyzer.md) перед дальнейшим использованием.</span><span class="sxs-lookup"><span data-stu-id="97483-152">**AnalysisWarningCode\_BackgroundException** is the only warning code value that requires that the [**IInkAnalyzer**](iinkanalyzer.md) object is re-instantiated before further use.</span></span>

<span data-ttu-id="97483-153">Другие предупреждения, например **аналисисварнингкоде \_ Инканалисисрекогнизеринитиализатионфаилед** и **аналисисварнингкоде \_ NoMatchingInkAnalysisRecognizerFound**, могут потребовать, чтобы объект [**IInkAnalyzer**](iinkanalyzer.md) использовал другой распознаватель.</span><span class="sxs-lookup"><span data-stu-id="97483-153">Other warnings code values, such as **AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed** and **AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**, might require that the [**IInkAnalyzer**](iinkanalyzer.md) object use a different recognizer.</span></span>

## <a name="requirements"></a><span data-ttu-id="97483-154">Требования</span><span class="sxs-lookup"><span data-stu-id="97483-154">Requirements</span></span>



| <span data-ttu-id="97483-155">Требование</span><span class="sxs-lookup"><span data-stu-id="97483-155">Requirement</span></span> | <span data-ttu-id="97483-156">Значение</span><span class="sxs-lookup"><span data-stu-id="97483-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97483-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97483-157">Minimum supported client</span></span><br/> | <span data-ttu-id="97483-158">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="97483-158">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="97483-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97483-159">Minimum supported server</span></span><br/> | <span data-ttu-id="97483-160">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="97483-160">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="97483-161">Header</span><span class="sxs-lookup"><span data-stu-id="97483-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="97483-162"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="97483-162"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97483-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97483-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97483-164">**Ианалисисварнинг:: Жетварнингкоде**</span><span class="sxs-lookup"><span data-stu-id="97483-164">**IAnalysisWarning::GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[<span data-ttu-id="97483-165">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="97483-165">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




