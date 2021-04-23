---
description: Предоставляет поиск с учетом регистра нечетких символов, не учитывающих регистр, для проанализированных рукописных штрихов и проанализированных графических штрихов, имеющих распознаваемые типы.
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: 'Метод Иинканализер:: Сеарчвислангуажеид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 829878a6fd326abb8a685b644cfc222ba6921385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809995"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a><span data-ttu-id="63184-103">Метод Иинканализер:: Сеарчвислангуажеид</span><span class="sxs-lookup"><span data-stu-id="63184-103">IInkAnalyzer::SearchWithLanguageId method</span></span>

<span data-ttu-id="63184-104">Предоставляет поиск с учетом регистра нечетких символов, не учитывающих регистр, для проанализированных рукописных штрихов и проанализированных графических штрихов, имеющих распознаваемые типы.</span><span class="sxs-lookup"><span data-stu-id="63184-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="63184-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63184-105">Syntax</span></span>


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="63184-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63184-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63184-107">*бстрфрасетоматч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63184-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63184-108">Фраза, которая будет найдена в альтернативах для анализируемых в настоящее время штрихов.</span><span class="sxs-lookup"><span data-stu-id="63184-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="63184-109">*лсеарчстринглангуажеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63184-109">*lSearchStringLanguageId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63184-110">Идентификатор LCID, связанный со строкой, которая передается.</span><span class="sxs-lookup"><span data-stu-id="63184-110">The LCID associated with the string that is passed.</span></span> <span data-ttu-id="63184-111">Используется для внутреннего преобразования регистра для поддержки сравнений без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="63184-111">Used to convert the case internally to support case insensitive comparisons.</span></span>

</dd> <dt>

<span data-ttu-id="63184-112">*пулсеарчресулткаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="63184-112">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63184-113">Максимальное число результатов, возвращаемых при поиске.</span><span class="sxs-lookup"><span data-stu-id="63184-113">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="63184-114">*ппулстрокекаунтперресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63184-114">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63184-115">Указатель на массив числа штрихов в каждом результате поиска.</span><span class="sxs-lookup"><span data-stu-id="63184-115">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="63184-116">*пулстрокеидскаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="63184-116">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63184-117">Число идентификаторов Stroke в *ппулстрокеидс*.</span><span class="sxs-lookup"><span data-stu-id="63184-117">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="63184-118">*ппулстрокеидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63184-118">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63184-119">Указатель на массив идентификаторов Stroke, представляющих набор наборов штрихов.</span><span class="sxs-lookup"><span data-stu-id="63184-119">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63184-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63184-120">Return value</span></span>

<span data-ttu-id="63184-121">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="63184-121">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="63184-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63184-122">Remarks</span></span>

<span data-ttu-id="63184-123">В результате поиска будут найдены подстроки из нескольких слов и отдельных слов.</span><span class="sxs-lookup"><span data-stu-id="63184-123">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="63184-124">Поиск выполняется в альтернативных результатах распознавания и в альтернативных сегментах.</span><span class="sxs-lookup"><span data-stu-id="63184-124">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="63184-125">Все входящие строки будут преобразованы в единый регистр для сравнения с использованием LCID текущего потока для выполнения этого преобразования в соответствии с региональными соглашениями о регистрах.</span><span class="sxs-lookup"><span data-stu-id="63184-125">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="63184-126">Переданная строка обрабатывается как фраза.</span><span class="sxs-lookup"><span data-stu-id="63184-126">The string passed is treated as a phrase.</span></span> <span data-ttu-id="63184-127">Слова и символы должны присутствовать в алтерантес для штрихов в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="63184-127">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="63184-128">Первое и Последнее слова фразы могут сопоставляться как подстроки (первое слово, отображаемое в конце альтернативного, и Последнее слово, отображаемое в беггингинге), но все остальные слова (внутри фразы) должны быть целыми словами.</span><span class="sxs-lookup"><span data-stu-id="63184-128">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="63184-129">Если переданная строка не содержит пробелов между символами, то подстрока может находиться в любом месте внутри одного слова в альтернативном.</span><span class="sxs-lookup"><span data-stu-id="63184-129">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="63184-130">Результаты поиска изменяются только присутствием или отсутствием пробелов между символами.</span><span class="sxs-lookup"><span data-stu-id="63184-130">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="63184-131">Пробелы, не заключенные в символы, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="63184-131">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="63184-132">Тип пробела игнорируется (знак табуляции или пробел между символами дает одинаковый результат).</span><span class="sxs-lookup"><span data-stu-id="63184-132">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="63184-133">Количество пробелов не имеет значения — один или два пробела между символами дают одинаковый результат.</span><span class="sxs-lookup"><span data-stu-id="63184-133">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="63184-134">Поиск не создает событий Популатеконтекстноде.</span><span class="sxs-lookup"><span data-stu-id="63184-134">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="63184-135">Будет выполнен поиск только уже заполненных штрихов.</span><span class="sxs-lookup"><span data-stu-id="63184-135">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="63184-136">Требования</span><span class="sxs-lookup"><span data-stu-id="63184-136">Requirements</span></span>



| <span data-ttu-id="63184-137">Требование</span><span class="sxs-lookup"><span data-stu-id="63184-137">Requirement</span></span> | <span data-ttu-id="63184-138">Значение</span><span class="sxs-lookup"><span data-stu-id="63184-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63184-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63184-139">Minimum supported client</span></span><br/> | <span data-ttu-id="63184-140">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="63184-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="63184-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63184-141">Minimum supported server</span></span><br/> | <span data-ttu-id="63184-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="63184-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="63184-143">Header</span><span class="sxs-lookup"><span data-stu-id="63184-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="63184-144"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="63184-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="63184-145">DLL</span><span class="sxs-lookup"><span data-stu-id="63184-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63184-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63184-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="63184-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63184-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63184-148">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="63184-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




