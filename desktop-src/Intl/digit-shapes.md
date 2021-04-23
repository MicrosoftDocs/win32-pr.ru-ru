---
description: Арабский и многие другие языки имеют классические фигуры для чисел, которые отличаются от стандартных западных цифр, наиболее часто используемых на компьютерах.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Цифры фигур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664323"
---
# <a name="digit-shapes"></a><span data-ttu-id="24ec3-103">Цифры фигур</span><span class="sxs-lookup"><span data-stu-id="24ec3-103">Digit Shapes</span></span>

<span data-ttu-id="24ec3-104">Арабский и многие другие языки имеют классические фигуры для чисел, которые отличаются от стандартных западных цифр, наиболее часто используемых на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="24ec3-104">Arabic and many other languages have classical shapes for numbers that are different from the conventional western digits most often used on computers.</span></span> <span data-ttu-id="24ec3-105">Чтобы избежать неоднозначности при именовании этих фигур, в этом документе используются следующие имена из стандарта Unicode.</span><span class="sxs-lookup"><span data-stu-id="24ec3-105">To avoid ambiguity in naming these shapes, this document uses the following names from the Unicode standard.</span></span>



| <span data-ttu-id="24ec3-106">Имена символов в Юникоде</span><span class="sxs-lookup"><span data-stu-id="24ec3-106">Unicode name of the digits</span></span>                                     | <span data-ttu-id="24ec3-107">Страна или регион, где используется</span><span class="sxs-lookup"><span data-stu-id="24ec3-107">Country/region where used</span></span>                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="24ec3-108">Европейские цифры</span><span class="sxs-lookup"><span data-stu-id="24ec3-108">European digits</span></span>                                                | <span data-ttu-id="24ec3-109">Европа, Americas и многие другие страны и регионы</span><span class="sxs-lookup"><span data-stu-id="24ec3-109">Europe, the Americas, and many other countries/regions</span></span>       |
| <span data-ttu-id="24ec3-110">Arabic-Indic цифры</span><span class="sxs-lookup"><span data-stu-id="24ec3-110">Arabic-Indic digits</span></span>                                            | <span data-ttu-id="24ec3-111">Арабские страны и регионы (хотя многие из них используют европейские цифры)</span><span class="sxs-lookup"><span data-stu-id="24ec3-111">Arabic countries/regions (although many use European digits)</span></span> |
| <span data-ttu-id="24ec3-112">Другие национальные цифры: индийские цифры, тайские цифры и т. д.</span><span class="sxs-lookup"><span data-stu-id="24ec3-112">Other national digits: Indic digits, Thai digits, and the like</span></span> | <span data-ttu-id="24ec3-113">Различные страны и регионы</span><span class="sxs-lookup"><span data-stu-id="24ec3-113">Various countries/regions</span></span>                                    |



 

<span data-ttu-id="24ec3-114">Юникод предоставляет отдельные кодовые точки для каждой фигуры цифр.</span><span class="sxs-lookup"><span data-stu-id="24ec3-114">Unicode provides separate code points for each digit shape.</span></span> <span data-ttu-id="24ec3-115">Таким же, чтобы получить доступ к специальным формам цифр языка, приложение может использовать соответствующие коды символов Юникода для указанных выше цифр, U + 0030 до U + 0039.</span><span class="sxs-lookup"><span data-stu-id="24ec3-115">Thus, to access special language digit shapes, your application can use the relevant Unicode character codes for the digits above, U+0030 through U+0039.</span></span> <span data-ttu-id="24ec3-116">Эти коды всегда отображаются с соответствующей формой, в зависимости от доступности шрифта.</span><span class="sxs-lookup"><span data-stu-id="24ec3-116">These codes are always displayed with the appropriate shape, subject to font availability.</span></span>

<span data-ttu-id="24ec3-117">Коды символов Юникода U + 0030 в U + 0039 номинально представляют европейские цифры от 0 до 9, но их цифровую форму можно изменить.</span><span class="sxs-lookup"><span data-stu-id="24ec3-117">The Unicode character codes U+0030 through U+0039 nominally represent the European digits 0 through 9, but their digit shape can be altered.</span></span> <span data-ttu-id="24ec3-118">Интерфейсы API текстовых интерфейсов GDI и DirectWrite предоставляют механизмы для управления этим поведением.</span><span class="sxs-lookup"><span data-stu-id="24ec3-118">GDI and DirectWrite text APIs provide mechanisms for applications to control this behavior.</span></span> <span data-ttu-id="24ec3-119">(См., например, [**скриптапплидигитсубститутион**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) или [**Идвритетекстаналисиссинк:: сетнумберсубститутион**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) Поведение в некоторых элементах управления оболочки и платформах пользовательского интерфейса может реагировать на параметры национальной настройки пользователя для замены цифр. [языковой стандарт \_ идигитсубститутион](locale-idigitsubstitution.md) LCTYPE можно использовать для получения параметров подстановки цифр по умолчанию для разных языков или параметров рабочего стола текущего пользователя для замены цифр.</span><span class="sxs-lookup"><span data-stu-id="24ec3-119">(See, for instance, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) or [**IDWriteTextAnalysisSink::SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) The behavior in some shell controls and user interface frameworks may respond to user locale settings for digit substitution; the [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE can be used to obtain default digit substitution settings for different locales or the current user's desktop settings for digit substitution.</span></span>

## <a name="native-digits"></a><span data-ttu-id="24ec3-120">Собственные цифры</span><span class="sxs-lookup"><span data-stu-id="24ec3-120">Native Digits</span></span>

<span data-ttu-id="24ec3-121">Цифры в машинном кодах — это цифры, выбранные пользователем на странице свойств **число** в разделе региональные и языковые параметры панели управления.</span><span class="sxs-lookup"><span data-stu-id="24ec3-121">Native digits are the digit shapes chosen by the user in the **Number** property sheet in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="24ec3-122">Чтобы найти предпочитаемую пользователем цифровую презентацию, приложение использует функцию [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) или [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) с константой [locale \_ снативедигитс](locale-snative-constants.md) , представляющей сведения о языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="24ec3-122">To find the digit presentation preferred by the user, your application uses the [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) function with the [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) constant representing the locale information.</span></span>

> [!Note]  
> <span data-ttu-id="24ec3-123">Обычно коды цифр Юникода создаются в средах выполнения операционной системы.</span><span class="sxs-lookup"><span data-stu-id="24ec3-123">Typically, Unicode digit codes are generated in runtime operating system routines.</span></span> <span data-ttu-id="24ec3-124">Поэтому необходимо обновить общие операционные системы среды выполнения, чтобы приложение [ \_ снативедигитс языковой стандарт](locale-snative-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="24ec3-124">Therefore, common runtime operating systems must be upgraded for the application to inspect [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) appropriately.</span></span>

 

## <a name="digit-substitution"></a><span data-ttu-id="24ec3-125">Подстановка цифр</span><span class="sxs-lookup"><span data-stu-id="24ec3-125">Digit Substitution</span></span>

<span data-ttu-id="24ec3-126">Приложение может использовать подстановку цифр, чтобы сообщить операционной системе о способе печати цифр U + 0030 через U + 0039.</span><span class="sxs-lookup"><span data-stu-id="24ec3-126">The application can use digit substitution to tell the operating system how to print digits U+0030 through U+0039.</span></span> <span data-ttu-id="24ec3-127">Эта операция управляется константой [ \_ идигитсубститутион локали](locale-idigitsubstitution.md) .</span><span class="sxs-lookup"><span data-stu-id="24ec3-127">The [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) constant controls this operation.</span></span>

## <a name="digit-shaping-for-a-single-function"></a><span data-ttu-id="24ec3-128">Формирование цифр для одной функции</span><span class="sxs-lookup"><span data-stu-id="24ec3-128">Digit Shaping for a Single Function</span></span>

<span data-ttu-id="24ec3-129">Функции [результатов ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [жетчарактерплацемент](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)и [обеспечить \_ ](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) имеют флаги, управляющие заменой кодов Юникода u + 0030 до u + 0039 на время вызова функции.</span><span class="sxs-lookup"><span data-stu-id="24ec3-129">The [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa), and [GCP\_RESULTS](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) functions have flags that govern the substitution of Unicode codes U+0030 through U+0039 for the duration of the function call.</span></span> <span data-ttu-id="24ec3-130">Эти флаги переопределяют региональные параметры на панели управления, но не сбрасывают параметры.</span><span class="sxs-lookup"><span data-stu-id="24ec3-130">These flags override regional settings in the Control Panel, but do not reset the settings.</span></span> <span data-ttu-id="24ec3-131">Кроме того, они не переопределяют коды Юникода НАДС и узлы.</span><span class="sxs-lookup"><span data-stu-id="24ec3-131">Also, they do not override the Unicode codes NADS and NODS.</span></span> <span data-ttu-id="24ec3-132">Доступны следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="24ec3-132">The following flags are available.</span></span>



| <span data-ttu-id="24ec3-133">Флаги</span><span class="sxs-lookup"><span data-stu-id="24ec3-133">Flags</span></span>                 | <span data-ttu-id="24ec3-134">Используемые цифры</span><span class="sxs-lookup"><span data-stu-id="24ec3-134">Digits used</span></span>                      | <span data-ttu-id="24ec3-135">Используется в</span><span class="sxs-lookup"><span data-stu-id="24ec3-135">Used in</span></span>                   |
|-----------------------|----------------------------------|---------------------------|
| <span data-ttu-id="24ec3-136">ЕТО \_ нумерикслатин</span><span class="sxs-lookup"><span data-stu-id="24ec3-136">ETO\_NUMERICSLATIN</span></span>    | <span data-ttu-id="24ec3-137">Европейские цифры</span><span class="sxs-lookup"><span data-stu-id="24ec3-137">European digits</span></span>                  | <span data-ttu-id="24ec3-138">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="24ec3-138">**ExtTextOut**</span></span>            |
| <span data-ttu-id="24ec3-139">ЕТО \_ нумерикслокал</span><span class="sxs-lookup"><span data-stu-id="24ec3-139">ETO\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="24ec3-140">Цифры, соответствующие языковому стандарту</span><span class="sxs-lookup"><span data-stu-id="24ec3-140">Digits appropriate to the locale</span></span> | <span data-ttu-id="24ec3-141">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="24ec3-141">**ExtTextOut**</span></span>            |
| <span data-ttu-id="24ec3-142">ОБЕСПЕЧИТЬ \_ нумерикслатин</span><span class="sxs-lookup"><span data-stu-id="24ec3-142">GCP\_NUMERICSLATIN</span></span>    | <span data-ttu-id="24ec3-143">Европейские цифры</span><span class="sxs-lookup"><span data-stu-id="24ec3-143">European digits</span></span>                  | <span data-ttu-id="24ec3-144">**жетчарактерплацемент**</span><span class="sxs-lookup"><span data-stu-id="24ec3-144">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="24ec3-145">ОБЕСПЕЧИТЬ \_ нумерикслокал</span><span class="sxs-lookup"><span data-stu-id="24ec3-145">GCP\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="24ec3-146">Цифры, соответствующие языковому стандарту</span><span class="sxs-lookup"><span data-stu-id="24ec3-146">Digits appropriate to the locale</span></span> | <span data-ttu-id="24ec3-147">**жетчарактерплацемент**</span><span class="sxs-lookup"><span data-stu-id="24ec3-147">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="24ec3-148">ГКПКЛАСС \_ латиннумбер</span><span class="sxs-lookup"><span data-stu-id="24ec3-148">GCPCLASS\_LATINNUMBER</span></span> | <span data-ttu-id="24ec3-149">Европейские цифры</span><span class="sxs-lookup"><span data-stu-id="24ec3-149">European digits</span></span>                  | <span data-ttu-id="24ec3-150">**\_Результаты обеспечить**</span><span class="sxs-lookup"><span data-stu-id="24ec3-150">**GCP\_RESULTS**</span></span>          |
| <span data-ttu-id="24ec3-151">ГКПКЛАСС \_ локалнумбер</span><span class="sxs-lookup"><span data-stu-id="24ec3-151">GCPCLASS\_LOCALNUMBER</span></span> | <span data-ttu-id="24ec3-152">Цифры, соответствующие языковому стандарту</span><span class="sxs-lookup"><span data-stu-id="24ec3-152">Digits appropriate to the locale</span></span> | <span data-ttu-id="24ec3-153">**\_Результаты обеспечить**</span><span class="sxs-lookup"><span data-stu-id="24ec3-153">**GCP\_RESULTS**</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="24ec3-154">См. также</span><span class="sxs-lookup"><span data-stu-id="24ec3-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24ec3-155">Сведения о поддержке национальных языков</span><span class="sxs-lookup"><span data-stu-id="24ec3-155">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="24ec3-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="24ec3-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[<span data-ttu-id="24ec3-157">**GetLocaleInfoEx**</span><span class="sxs-lookup"><span data-stu-id="24ec3-157">**GetLocaleInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
