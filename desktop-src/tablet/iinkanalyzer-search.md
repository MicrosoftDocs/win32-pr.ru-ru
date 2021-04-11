---
description: Предоставляет поиск с учетом регистра нечетких символов, не учитывающих регистр, для проанализированных рукописных штрихов и проанализированных графических штрихов, имеющих распознаваемые типы.
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'Метод Иинканализер:: Search (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ea9755c0f2836b363b967a3d6bfdc5d64a1305b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145439"
---
# <a name="iinkanalyzersearch-method"></a><span data-ttu-id="75493-103">Метод Иинканализер:: Search</span><span class="sxs-lookup"><span data-stu-id="75493-103">IInkAnalyzer::Search method</span></span>

<span data-ttu-id="75493-104">Предоставляет поиск с учетом регистра нечетких символов, не учитывающих регистр, для проанализированных рукописных штрихов и проанализированных графических штрихов, имеющих распознаваемые типы.</span><span class="sxs-lookup"><span data-stu-id="75493-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="75493-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75493-105">Syntax</span></span>


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="75493-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75493-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75493-107">*бстрфрасетоматч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75493-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75493-108">Фраза, которая будет найдена в альтернативах для анализируемых в настоящее время штрихов.</span><span class="sxs-lookup"><span data-stu-id="75493-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="75493-109">*пулсеарчресулткаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="75493-109">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75493-110">Максимальное число результатов, возвращаемых при поиске.</span><span class="sxs-lookup"><span data-stu-id="75493-110">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="75493-111">*ппулстрокекаунтперресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75493-111">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75493-112">Указатель на массив числа штрихов в каждом результате поиска.</span><span class="sxs-lookup"><span data-stu-id="75493-112">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="75493-113">*пулстрокеидскаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="75493-113">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75493-114">Число идентификаторов Stroke в *ппулстрокеидс*.</span><span class="sxs-lookup"><span data-stu-id="75493-114">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="75493-115">*ппулстрокеидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75493-115">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75493-116">Указатель на массив идентификаторов Stroke, представляющих набор наборов штрихов.</span><span class="sxs-lookup"><span data-stu-id="75493-116">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75493-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75493-117">Return value</span></span>

<span data-ttu-id="75493-118">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="75493-118">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75493-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75493-119">Remarks</span></span>

<span data-ttu-id="75493-120">В результате поиска будут найдены подстроки из нескольких слов и отдельных слов.</span><span class="sxs-lookup"><span data-stu-id="75493-120">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="75493-121">Поиск выполняется в альтернативных результатах распознавания и в альтернативных сегментах.</span><span class="sxs-lookup"><span data-stu-id="75493-121">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="75493-122">Все входящие строки будут преобразованы в единый регистр для сравнения с использованием LCID текущего потока для выполнения этого преобразования в соответствии с региональными соглашениями о регистрах.</span><span class="sxs-lookup"><span data-stu-id="75493-122">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="75493-123">Переданная строка обрабатывается как фраза.</span><span class="sxs-lookup"><span data-stu-id="75493-123">The string passed is treated as a phrase.</span></span> <span data-ttu-id="75493-124">Слова и символы должны присутствовать в алтерантес для штрихов в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="75493-124">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="75493-125">Первое и Последнее слова фразы могут сопоставляться как подстроки (первое слово, отображаемое в конце альтернативного, и Последнее слово, отображаемое в беггингинге), но все остальные слова (внутри фразы) должны быть целыми словами.</span><span class="sxs-lookup"><span data-stu-id="75493-125">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="75493-126">Если переданная строка не содержит пробелов между символами, то подстрока может находиться в любом месте внутри одного слова в альтернативном.</span><span class="sxs-lookup"><span data-stu-id="75493-126">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="75493-127">Результаты поиска изменяются только присутствием или отсутствием пробелов между символами.</span><span class="sxs-lookup"><span data-stu-id="75493-127">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="75493-128">Пробелы, не заключенные в символы, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="75493-128">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="75493-129">Тип пробела игнорируется (знак табуляции или пробел между символами дает одинаковый результат).</span><span class="sxs-lookup"><span data-stu-id="75493-129">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="75493-130">Количество пробелов не имеет значения — один или два пробела между символами дают одинаковый результат.</span><span class="sxs-lookup"><span data-stu-id="75493-130">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="75493-131">Поиск не создает событий Популатеконтекстноде.</span><span class="sxs-lookup"><span data-stu-id="75493-131">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="75493-132">Будет выполнен поиск только уже заполненных штрихов.</span><span class="sxs-lookup"><span data-stu-id="75493-132">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="75493-133">Требования</span><span class="sxs-lookup"><span data-stu-id="75493-133">Requirements</span></span>



| <span data-ttu-id="75493-134">Требование</span><span class="sxs-lookup"><span data-stu-id="75493-134">Requirement</span></span> | <span data-ttu-id="75493-135">Значение</span><span class="sxs-lookup"><span data-stu-id="75493-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75493-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75493-136">Minimum supported client</span></span><br/> | <span data-ttu-id="75493-137">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="75493-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75493-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75493-138">Minimum supported server</span></span><br/> | <span data-ttu-id="75493-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="75493-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="75493-140">Header</span><span class="sxs-lookup"><span data-stu-id="75493-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="75493-141"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="75493-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75493-142">DLL</span><span class="sxs-lookup"><span data-stu-id="75493-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75493-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75493-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="75493-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75493-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75493-145">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="75493-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




