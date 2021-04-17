---
description: Задает атрибуты Иинканалисисрекогнизер.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Перечисление Рекогнизеркапабилитиес (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702410"
---
# <a name="recognizercapabilities-enumeration"></a><span data-ttu-id="25ae4-103">Перечисление Рекогнизеркапабилитиес</span><span class="sxs-lookup"><span data-stu-id="25ae4-103">RecognizerCapabilities enumeration</span></span>

<span data-ttu-id="25ae4-104">Задает атрибуты [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="25ae4-104">Specifies the attributes of an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="25ae4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25ae4-105">Syntax</span></span>


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a><span data-ttu-id="25ae4-106">Константы</span><span class="sxs-lookup"><span data-stu-id="25ae4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="25ae4-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**Версия-кандидат \_ None**</span><span class="sxs-lookup"><span data-stu-id="25ae4-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC\_None**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-108">Возможности не указаны.</span><span class="sxs-lookup"><span data-stu-id="25ae4-108">No capabilities specified.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**Версия-кандидат \_ доноткаре**</span><span class="sxs-lookup"><span data-stu-id="25ae4-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC\_DoNotCare**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-110">Игнорирует все установленные флаги.</span><span class="sxs-lookup"><span data-stu-id="25ae4-110">Ignores all other flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC, \_ объект**</span><span class="sxs-lookup"><span data-stu-id="25ae4-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC\_Object**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-112">Поддерживает распознавание объектов; в противном случае распознает только текст.</span><span class="sxs-lookup"><span data-stu-id="25ae4-112">Supports object recognition; otherwise, recognizes only text.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**Версия-кандидат \_ фриинпут**</span><span class="sxs-lookup"><span data-stu-id="25ae4-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC\_FreeInput**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-114">Поддерживает свободные входные данные, в которых рукописные данные записываются без использования руководств по распознаванию, например линии или поля.</span><span class="sxs-lookup"><span data-stu-id="25ae4-114">Supports free input, where ink is entered without the use of a recognition guide, such as a line or a box.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**Версия-кандидат \_ линединпут**</span><span class="sxs-lookup"><span data-stu-id="25ae4-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC\_LinedInput**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-116">Поддерживает линейный ввод, аналогичный написанию на бумаге.</span><span class="sxs-lookup"><span data-stu-id="25ae4-116">Supports lined input, which is similar to writing on lined paper.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**Версия-кандидат \_ боксединпут**</span><span class="sxs-lookup"><span data-stu-id="25ae4-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC\_BoxedInput**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-118">Поддерживает Упакованные входные данные, где каждый символ или слово введены в поле.</span><span class="sxs-lookup"><span data-stu-id="25ae4-118">Supports boxed input, where each character or word is entered in a box.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**Версия-кандидат \_ чарактераутокомплетионинпут**</span><span class="sxs-lookup"><span data-stu-id="25ae4-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC\_CharacterAutoCompletionInput**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-120">Поддерживает автозаполнение символов.</span><span class="sxs-lookup"><span data-stu-id="25ae4-120">Supports character Autocomplete.</span></span> <span data-ttu-id="25ae4-121">Распознаватели, поддерживающие Автозаполнение символов, нуждаются в упакованных входных данных.</span><span class="sxs-lookup"><span data-stu-id="25ae4-121">Recognizers that support character Autocomplete require boxed input.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**Версия-кандидат \_ ригхтанддовн**</span><span class="sxs-lookup"><span data-stu-id="25ae4-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC\_RightAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-123">Поддерживает ввод рукописного ввода в правильном и меньшом порядке, например в западных языках и на некоторых восточно-азиатских языках.</span><span class="sxs-lookup"><span data-stu-id="25ae4-123">Supports handwriting input in right and down order, such as in western languages and some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**Версия-кандидат \_ лефтанддовн**</span><span class="sxs-lookup"><span data-stu-id="25ae4-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC\_LeftAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-125">Поддерживает рукописный ввод в левом и меньшом порядке, например на иврите и арабском языке.</span><span class="sxs-lookup"><span data-stu-id="25ae4-125">Supports handwriting input in left and down order, such as in Hebrew and Arabic languages.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**Версия-кандидат \_ довнандлефт**</span><span class="sxs-lookup"><span data-stu-id="25ae4-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC\_DownAndLeft**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-127">Поддерживает рукописный ввод в порядке вниз и слева, например на некоторых восточно-азиатских языках.</span><span class="sxs-lookup"><span data-stu-id="25ae4-127">Supports handwriting input in down and left order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**Версия-кандидат \_ довнандригхт**</span><span class="sxs-lookup"><span data-stu-id="25ae4-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC\_DownAndRight**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-129">Поддерживает ввод рукописного ввода в неправильном порядке, например на некоторых восточно-азиатских языках.</span><span class="sxs-lookup"><span data-stu-id="25ae4-129">Supports handwriting input in down and right order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**Версия-кандидат \_ арбитрарянгле**</span><span class="sxs-lookup"><span data-stu-id="25ae4-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC\_ArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-131">Поддерживает текст, написанный в произвольных угловах.</span><span class="sxs-lookup"><span data-stu-id="25ae4-131">Supports text written at arbitrary angles.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**Версия-кандидат \_ Lattice**</span><span class="sxs-lookup"><span data-stu-id="25ae4-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC\_Lattice**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-133">Поддерживает возврат Lattice в качестве альтернативы строки для результатов распознавания рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="25ae4-133">Supports returning a lattice as an alternative a string for handwriting recognition results.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**Версия-кандидат \_ адвисеинкчанже**</span><span class="sxs-lookup"><span data-stu-id="25ae4-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC\_AdviseInkChange**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-135">Поддерживает прерывание распознавания фона, например изменение рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="25ae4-135">Supports interrupting background recognition, such as when the ink has changed.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**Версия-кандидат \_ строкереордер**</span><span class="sxs-lookup"><span data-stu-id="25ae4-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC\_StrokeReorder**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-137">Поддерживает этот порядок штрихов, пространственный и временный, который обрабатывается как часть операции распознавания.</span><span class="sxs-lookup"><span data-stu-id="25ae4-137">Supports that stroke order, spatial and temporal, is handled as part of the recognition operation.</span></span> <span data-ttu-id="25ae4-138">[**Иинканализер**](iinkanalyzer.md) не переупорядочивает штрихи перед отправкой рукописного ввода в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="25ae4-138">The [**IInkAnalyzer**](iinkanalyzer.md) does not reorder strokes before sending ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**\_Настраиваемый RC**</span><span class="sxs-lookup"><span data-stu-id="25ae4-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC\_Personalizable**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-140">Поддерживает персонализированный рукописный ввод, при котором распознаватель улучшает распознавание при использовании рукописного ввода с течением времени.</span><span class="sxs-lookup"><span data-stu-id="25ae4-140">Supports personalized handwriting, where the recognizer improves recognition when exposed to the same handwriting over time.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**Версия-кандидат \_ преферсарбитрарянгле**</span><span class="sxs-lookup"><span data-stu-id="25ae4-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC\_PrefersArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-142">[**Иинканализер**](iinkanalyzer.md) не нужно поворачивать рукописный текст на горизонтальную ориентацию перед отправкой рукописного ввода в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="25ae4-142">The [**IInkAnalyzer**](iinkanalyzer.md) need not rotate the handwriting to a horizontal orientation before sending the ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**Версия-кандидат \_ преферспараграфбреакинг**</span><span class="sxs-lookup"><span data-stu-id="25ae4-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC\_PrefersParagraphBreaking**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-144">[**Иинканализер**](iinkanalyzer.md) должен отправить в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)целые абзацы рукописного ввода, позволяя **иинканалисисрекогнизер** выполнить разрыв строки и слово (или знак).</span><span class="sxs-lookup"><span data-stu-id="25ae4-144">The [**IInkAnalyzer**](iinkanalyzer.md) should send entire paragraphs of ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), allowing the **IInkAnalysisRecognizer** to do the line breaking and word (or character) breaking.</span></span>

</dd> <dt>

<span data-ttu-id="25ae4-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**Версия-кандидат \_ преферссегментатионрекогнитион**</span><span class="sxs-lookup"><span data-stu-id="25ae4-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC\_PrefersSegmentationRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="25ae4-146">Распознает только одно слово или символ для каждой операции распознавания.</span><span class="sxs-lookup"><span data-stu-id="25ae4-146">Recognizes only one word or character per recognition operation.</span></span> <span data-ttu-id="25ae4-147">[**Иинканализер**](iinkanalyzer.md) выполняет сегментацию на рукописном тексте и отправляет в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)только один сегмент.</span><span class="sxs-lookup"><span data-stu-id="25ae4-147">The [**IInkAnalyzer**](iinkanalyzer.md) performs segmentation on the handwriting and sends only one segment at a time to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25ae4-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25ae4-148">Remarks</span></span>

<span data-ttu-id="25ae4-149">Это перечисление позволяет побитовое сочетание значений его членов.</span><span class="sxs-lookup"><span data-stu-id="25ae4-149">This enumeration allows a bitwise combination of its member values.</span></span> <span data-ttu-id="25ae4-150">Используйте это перечисление, чтобы найти установленный распознаватель рукописного ввода, который поддерживает необходимые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="25ae4-150">Use this enumeration to find an installed ink recognizer that supports the attributes you need.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ae4-151">Требования</span><span class="sxs-lookup"><span data-stu-id="25ae4-151">Requirements</span></span>



| <span data-ttu-id="25ae4-152">Требование</span><span class="sxs-lookup"><span data-stu-id="25ae4-152">Requirement</span></span> | <span data-ttu-id="25ae4-153">Значение</span><span class="sxs-lookup"><span data-stu-id="25ae4-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25ae4-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25ae4-154">Minimum supported client</span></span><br/> | <span data-ttu-id="25ae4-155">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="25ae4-155">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="25ae4-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25ae4-156">Minimum supported server</span></span><br/> | <span data-ttu-id="25ae4-157">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25ae4-157">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="25ae4-158">Header</span><span class="sxs-lookup"><span data-stu-id="25ae4-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="25ae4-159"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="25ae4-159"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25ae4-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25ae4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ae4-161">**Возможности Иинканалисисрекогнизер:: Capabilities**</span><span class="sxs-lookup"><span data-stu-id="25ae4-161">**IInkAnalysisRecognizer::GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[<span data-ttu-id="25ae4-162">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="25ae4-162">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




