---
title: Варфилеинфо BLOCK, инструкция
description: Описывает форму информационного блока переменной.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Меню инструкций блока Варфилеинфо и другие ресурсы
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645801618de130439bdf1998b92183e4791783
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069148"
---
# <a name="varfileinfo-block-statement"></a><span data-ttu-id="3ab9b-104">Варфилеинфо BLOCK, инструкция</span><span class="sxs-lookup"><span data-stu-id="3ab9b-104">VarFileInfo BLOCK statement</span></span>

<span data-ttu-id="3ab9b-105">Определяет блок сведений о переменной.</span><span class="sxs-lookup"><span data-stu-id="3ab9b-105">Defines a variable information block.</span></span>

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a><span data-ttu-id="3ab9b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ab9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ab9b-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Надежно*</span><span class="sxs-lookup"><span data-stu-id="3ab9b-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="3ab9b-108">Один из идентификаторов языка, указанных в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="3ab9b-108">One of the language identifiers specified in the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="3ab9b-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*чарсетид*</span><span class="sxs-lookup"><span data-stu-id="3ab9b-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="3ab9b-110">Один из идентификаторов наборов символов, указанных в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="3ab9b-110">One of the character-set identifiers specified in the Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ab9b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ab9b-111">Remarks</span></span>

<span data-ttu-id="3ab9b-112">Можно указать более одной пары идентификаторов, но каждую пару следует отделять от предшествующей пары запятыми.</span><span class="sxs-lookup"><span data-stu-id="3ab9b-112">More than one identifier pair can be given, but each pair must be separated from the preceding pair with a comma.</span></span>

<span data-ttu-id="3ab9b-113">Параметр *langID* указывает один из следующих кодов языка.</span><span class="sxs-lookup"><span data-stu-id="3ab9b-113">The *langID* parameter specifies one of the following language codes.</span></span>



| <span data-ttu-id="3ab9b-114">Код</span><span class="sxs-lookup"><span data-stu-id="3ab9b-114">Code</span></span>   | <span data-ttu-id="3ab9b-115">Язык</span><span class="sxs-lookup"><span data-stu-id="3ab9b-115">Language</span></span>            | <span data-ttu-id="3ab9b-116">Код</span><span class="sxs-lookup"><span data-stu-id="3ab9b-116">Code</span></span>   | <span data-ttu-id="3ab9b-117">Язык</span><span class="sxs-lookup"><span data-stu-id="3ab9b-117">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="3ab9b-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="3ab9b-118">0x0401</span></span> | <span data-ttu-id="3ab9b-119">Арабский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-119">Arabic</span></span>              | <span data-ttu-id="3ab9b-120">0x0415</span><span class="sxs-lookup"><span data-stu-id="3ab9b-120">0x0415</span></span> | <span data-ttu-id="3ab9b-121">Польский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-121">Polish</span></span>                    |
| <span data-ttu-id="3ab9b-122">0x0402</span><span class="sxs-lookup"><span data-stu-id="3ab9b-122">0x0402</span></span> | <span data-ttu-id="3ab9b-123">Болгарский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-123">Bulgarian</span></span>           | <span data-ttu-id="3ab9b-124">0x0416</span><span class="sxs-lookup"><span data-stu-id="3ab9b-124">0x0416</span></span> | <span data-ttu-id="3ab9b-125">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-125">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="3ab9b-126">0x0403</span><span class="sxs-lookup"><span data-stu-id="3ab9b-126">0x0403</span></span> | <span data-ttu-id="3ab9b-127">Каталонский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-127">Catalan</span></span>             | <span data-ttu-id="3ab9b-128">0x0417</span><span class="sxs-lookup"><span data-stu-id="3ab9b-128">0x0417</span></span> | <span data-ttu-id="3ab9b-129">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="3ab9b-129">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="3ab9b-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="3ab9b-130">0x0404</span></span> | <span data-ttu-id="3ab9b-131">Китайский (традиционный)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-131">Traditional Chinese</span></span> | <span data-ttu-id="3ab9b-132">0x0418</span><span class="sxs-lookup"><span data-stu-id="3ab9b-132">0x0418</span></span> | <span data-ttu-id="3ab9b-133">Румынский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-133">Romanian</span></span>                  |
| <span data-ttu-id="3ab9b-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="3ab9b-134">0x0405</span></span> | <span data-ttu-id="3ab9b-135">Чешский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-135">Czech</span></span>               | <span data-ttu-id="3ab9b-136">0x0419</span><span class="sxs-lookup"><span data-stu-id="3ab9b-136">0x0419</span></span> | <span data-ttu-id="3ab9b-137">русском языке</span><span class="sxs-lookup"><span data-stu-id="3ab9b-137">Russian</span></span>                   |
| <span data-ttu-id="3ab9b-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="3ab9b-138">0x0406</span></span> | <span data-ttu-id="3ab9b-139">Датский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-139">Danish</span></span>              | <span data-ttu-id="3ab9b-140">0x041A</span><span class="sxs-lookup"><span data-stu-id="3ab9b-140">0x041A</span></span> | <span data-ttu-id="3ab9b-141">Croato-Serbian (латиница)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-141">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="3ab9b-142">0x0407</span><span class="sxs-lookup"><span data-stu-id="3ab9b-142">0x0407</span></span> | <span data-ttu-id="3ab9b-143">Немецкий</span><span class="sxs-lookup"><span data-stu-id="3ab9b-143">German</span></span>              | <span data-ttu-id="3ab9b-144">0x041B</span><span class="sxs-lookup"><span data-stu-id="3ab9b-144">0x041B</span></span> | <span data-ttu-id="3ab9b-145">Словацкий</span><span class="sxs-lookup"><span data-stu-id="3ab9b-145">Slovak</span></span>                    |
| <span data-ttu-id="3ab9b-146">0x0408</span><span class="sxs-lookup"><span data-stu-id="3ab9b-146">0x0408</span></span> | <span data-ttu-id="3ab9b-147">Греческий</span><span class="sxs-lookup"><span data-stu-id="3ab9b-147">Greek</span></span>               | <span data-ttu-id="3ab9b-148">0x041C</span><span class="sxs-lookup"><span data-stu-id="3ab9b-148">0x041C</span></span> | <span data-ttu-id="3ab9b-149">Албанский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-149">Albanian</span></span>                  |
| <span data-ttu-id="3ab9b-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="3ab9b-150">0x0409</span></span> | <span data-ttu-id="3ab9b-151">Английский (США)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-151">U.S. English</span></span>        | <span data-ttu-id="3ab9b-152">0x041D</span><span class="sxs-lookup"><span data-stu-id="3ab9b-152">0x041D</span></span> | <span data-ttu-id="3ab9b-153">Шведский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-153">Swedish</span></span>                   |
| <span data-ttu-id="3ab9b-154">0x040A</span><span class="sxs-lookup"><span data-stu-id="3ab9b-154">0x040A</span></span> | <span data-ttu-id="3ab9b-155">Кастильский испанский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-155">Castilian Spanish</span></span>   | <span data-ttu-id="3ab9b-156">0x041E</span><span class="sxs-lookup"><span data-stu-id="3ab9b-156">0x041E</span></span> | <span data-ttu-id="3ab9b-157">Тайский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-157">Thai</span></span>                      |
| <span data-ttu-id="3ab9b-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="3ab9b-158">0x040B</span></span> | <span data-ttu-id="3ab9b-159">Финский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-159">Finnish</span></span>             | <span data-ttu-id="3ab9b-160">0x041F</span><span class="sxs-lookup"><span data-stu-id="3ab9b-160">0x041F</span></span> | <span data-ttu-id="3ab9b-161">Турецкий</span><span class="sxs-lookup"><span data-stu-id="3ab9b-161">Turkish</span></span>                   |
| <span data-ttu-id="3ab9b-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="3ab9b-162">0x040C</span></span> | <span data-ttu-id="3ab9b-163">Французский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-163">French</span></span>              | <span data-ttu-id="3ab9b-164">0x0420</span><span class="sxs-lookup"><span data-stu-id="3ab9b-164">0x0420</span></span> | <span data-ttu-id="3ab9b-165">Урду</span><span class="sxs-lookup"><span data-stu-id="3ab9b-165">Urdu</span></span>                      |
| <span data-ttu-id="3ab9b-166">0x040D</span><span class="sxs-lookup"><span data-stu-id="3ab9b-166">0x040D</span></span> | <span data-ttu-id="3ab9b-167">Иврит</span><span class="sxs-lookup"><span data-stu-id="3ab9b-167">Hebrew</span></span>              | <span data-ttu-id="3ab9b-168">0x0421</span><span class="sxs-lookup"><span data-stu-id="3ab9b-168">0x0421</span></span> | <span data-ttu-id="3ab9b-169">Бахаса</span><span class="sxs-lookup"><span data-stu-id="3ab9b-169">Bahasa</span></span>                    |
| <span data-ttu-id="3ab9b-170">0x040E</span><span class="sxs-lookup"><span data-stu-id="3ab9b-170">0x040E</span></span> | <span data-ttu-id="3ab9b-171">Венгерский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-171">Hungarian</span></span>           | <span data-ttu-id="3ab9b-172">0x0804</span><span class="sxs-lookup"><span data-stu-id="3ab9b-172">0x0804</span></span> | <span data-ttu-id="3ab9b-173">Китайский (упрощенный)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-173">Simplified Chinese</span></span>        |
| <span data-ttu-id="3ab9b-174">0x040F</span><span class="sxs-lookup"><span data-stu-id="3ab9b-174">0x040F</span></span> | <span data-ttu-id="3ab9b-175">Исландский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-175">Icelandic</span></span>           | <span data-ttu-id="3ab9b-176">0x0807</span><span class="sxs-lookup"><span data-stu-id="3ab9b-176">0x0807</span></span> | <span data-ttu-id="3ab9b-177">Швейцарская немецкая</span><span class="sxs-lookup"><span data-stu-id="3ab9b-177">Swiss German</span></span>              |
| <span data-ttu-id="3ab9b-178">0x0410</span><span class="sxs-lookup"><span data-stu-id="3ab9b-178">0x0410</span></span> | <span data-ttu-id="3ab9b-179">Итальянский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-179">Italian</span></span>             | <span data-ttu-id="3ab9b-180">0x0809</span><span class="sxs-lookup"><span data-stu-id="3ab9b-180">0x0809</span></span> | <span data-ttu-id="3ab9b-181">Великобритании</span><span class="sxs-lookup"><span data-stu-id="3ab9b-181">U.K.</span></span> <span data-ttu-id="3ab9b-182">Английский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-182">English</span></span>              |
| <span data-ttu-id="3ab9b-183">0x0411</span><span class="sxs-lookup"><span data-stu-id="3ab9b-183">0x0411</span></span> | <span data-ttu-id="3ab9b-184">Японский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-184">Japanese</span></span>            | <span data-ttu-id="3ab9b-185">0x080A</span><span class="sxs-lookup"><span data-stu-id="3ab9b-185">0x080A</span></span> | <span data-ttu-id="3ab9b-186">Испанский (Мексика)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-186">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="3ab9b-187">0x0412</span><span class="sxs-lookup"><span data-stu-id="3ab9b-187">0x0412</span></span> | <span data-ttu-id="3ab9b-188">Корейский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-188">Korean</span></span>              | <span data-ttu-id="3ab9b-189">0x080C</span><span class="sxs-lookup"><span data-stu-id="3ab9b-189">0x080C</span></span> | <span data-ttu-id="3ab9b-190">Бельгия (французский)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-190">Belgian French</span></span>            |
| <span data-ttu-id="3ab9b-191">0x0413</span><span class="sxs-lookup"><span data-stu-id="3ab9b-191">0x0413</span></span> | <span data-ttu-id="3ab9b-192">Нидерландский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-192">Dutch</span></span>               | <span data-ttu-id="3ab9b-193">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="3ab9b-193">0x0C0C</span></span> | <span data-ttu-id="3ab9b-194">Французский (Канада)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-194">Canadian French</span></span>           |
| <span data-ttu-id="3ab9b-195">0x0414</span><span class="sxs-lookup"><span data-stu-id="3ab9b-195">0x0414</span></span> | <span data-ttu-id="3ab9b-196">Норвежский — букмол</span><span class="sxs-lookup"><span data-stu-id="3ab9b-196">Norwegian – Bokmal</span></span>  | <span data-ttu-id="3ab9b-197">0x100C</span><span class="sxs-lookup"><span data-stu-id="3ab9b-197">0x100C</span></span> | <span data-ttu-id="3ab9b-198">Швейцарский французский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-198">Swiss French</span></span>              |
| <span data-ttu-id="3ab9b-199">0x0810</span><span class="sxs-lookup"><span data-stu-id="3ab9b-199">0x0810</span></span> | <span data-ttu-id="3ab9b-200">Швейцарский итальянский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-200">Swiss Italian</span></span>       | <span data-ttu-id="3ab9b-201">0x0816</span><span class="sxs-lookup"><span data-stu-id="3ab9b-201">0x0816</span></span> | <span data-ttu-id="3ab9b-202">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-202">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="3ab9b-203">0x0813</span><span class="sxs-lookup"><span data-stu-id="3ab9b-203">0x0813</span></span> | <span data-ttu-id="3ab9b-204">Голландский (Бельгия)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-204">Belgian Dutch</span></span>       | <span data-ttu-id="3ab9b-205">0x081A</span><span class="sxs-lookup"><span data-stu-id="3ab9b-205">0x081A</span></span> | <span data-ttu-id="3ab9b-206">Serbo-Croatian (кириллица)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-206">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="3ab9b-207">0x0814</span><span class="sxs-lookup"><span data-stu-id="3ab9b-207">0x0814</span></span> | <span data-ttu-id="3ab9b-208">Норвежский — нюнорск</span><span class="sxs-lookup"><span data-stu-id="3ab9b-208">Norwegian – Nynorsk</span></span> | <span data-ttu-id="3ab9b-209">?</span><span class="sxs-lookup"><span data-stu-id="3ab9b-209">?</span></span>      | <span data-ttu-id="3ab9b-210">?</span><span class="sxs-lookup"><span data-stu-id="3ab9b-210">?</span></span>                         |



 

<span data-ttu-id="3ab9b-211">Параметр *чарсетид* задает один из следующих идентификаторов наборов символов:</span><span class="sxs-lookup"><span data-stu-id="3ab9b-211">The *charsetID* parameter specifies one of the following character-set identifiers:</span></span>



| <span data-ttu-id="3ab9b-212">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="3ab9b-212">Identifier</span></span> | <span data-ttu-id="3ab9b-213">Кодировка</span><span class="sxs-lookup"><span data-stu-id="3ab9b-213">Character Set</span></span>              |
|------------|----------------------------|
| <span data-ttu-id="3ab9b-214">0</span><span class="sxs-lookup"><span data-stu-id="3ab9b-214">0</span></span>          | <span data-ttu-id="3ab9b-215">7-разрядный код ASCII</span><span class="sxs-lookup"><span data-stu-id="3ab9b-215">7-bit ASCII</span></span>                |
| <span data-ttu-id="3ab9b-216">932</span><span class="sxs-lookup"><span data-stu-id="3ab9b-216">932</span></span>        | <span data-ttu-id="3ab9b-217">Япония (Shift – JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-217">Japan (Shift – JIS X-0208)</span></span> |
| <span data-ttu-id="3ab9b-218">949</span><span class="sxs-lookup"><span data-stu-id="3ab9b-218">949</span></span>        | <span data-ttu-id="3ab9b-219">Корея (Shift — КСК 5601)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-219">Korea (Shift – KSC 5601)</span></span>   |
| <span data-ttu-id="3ab9b-220">950</span><span class="sxs-lookup"><span data-stu-id="3ab9b-220">950</span></span>        | <span data-ttu-id="3ab9b-221">Тайвань (Big5)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-221">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="3ab9b-222">1200</span><span class="sxs-lookup"><span data-stu-id="3ab9b-222">1200</span></span>       | <span data-ttu-id="3ab9b-223">Юникод</span><span class="sxs-lookup"><span data-stu-id="3ab9b-223">Unicode</span></span>                    |
| <span data-ttu-id="3ab9b-224">1250</span><span class="sxs-lookup"><span data-stu-id="3ab9b-224">1250</span></span>       | <span data-ttu-id="3ab9b-225">Латиница 2 (Восточная Европа)</span><span class="sxs-lookup"><span data-stu-id="3ab9b-225">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="3ab9b-226">1251</span><span class="sxs-lookup"><span data-stu-id="3ab9b-226">1251</span></span>       | <span data-ttu-id="3ab9b-227">Кириллица</span><span class="sxs-lookup"><span data-stu-id="3ab9b-227">Cyrillic</span></span>                   |
| <span data-ttu-id="3ab9b-228">1252</span><span class="sxs-lookup"><span data-stu-id="3ab9b-228">1252</span></span>       | <span data-ttu-id="3ab9b-229">Многоязычных</span><span class="sxs-lookup"><span data-stu-id="3ab9b-229">Multilingual</span></span>               |
| <span data-ttu-id="3ab9b-230">1253</span><span class="sxs-lookup"><span data-stu-id="3ab9b-230">1253</span></span>       | <span data-ttu-id="3ab9b-231">Греческий</span><span class="sxs-lookup"><span data-stu-id="3ab9b-231">Greek</span></span>                      |
| <span data-ttu-id="3ab9b-232">1254</span><span class="sxs-lookup"><span data-stu-id="3ab9b-232">1254</span></span>       | <span data-ttu-id="3ab9b-233">Турецкий</span><span class="sxs-lookup"><span data-stu-id="3ab9b-233">Turkish</span></span>                    |
| <span data-ttu-id="3ab9b-234">1255</span><span class="sxs-lookup"><span data-stu-id="3ab9b-234">1255</span></span>       | <span data-ttu-id="3ab9b-235">Иврит</span><span class="sxs-lookup"><span data-stu-id="3ab9b-235">Hebrew</span></span>                     |
| <span data-ttu-id="3ab9b-236">1256</span><span class="sxs-lookup"><span data-stu-id="3ab9b-236">1256</span></span>       | <span data-ttu-id="3ab9b-237">Арабский</span><span class="sxs-lookup"><span data-stu-id="3ab9b-237">Arabic</span></span>                     |



 

 

 




