---
description: Подмножество Юникода битовых полей (Усбс) используется в структурах ФОНТСИГНАТУРЕ и ЛОКАЛЕСИГНАТУРЕ.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Битовых полей подмножества Юникода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fced251b1bf8e04dd4c0d7d7cb0dca15c8bdfa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650978"
---
# <a name="unicode-subset-bitfields"></a><span data-ttu-id="7decc-103">Битовых полей подмножества Юникода</span><span class="sxs-lookup"><span data-stu-id="7decc-103">Unicode Subset Bitfields</span></span>

<span data-ttu-id="7decc-104">Подмножество Юникода битовых полей (Усбс) используется в структурах [**фонтсигнатуре**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) и [**локалесигнатуре**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .</span><span class="sxs-lookup"><span data-stu-id="7decc-104">The Unicode subset bitfields (USBs) are used in the [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) and [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) structures.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7decc-105">bit</span><span class="sxs-lookup"><span data-stu-id="7decc-105">Bit</span></span></th>
<th><span data-ttu-id="7decc-106">Поддиапазон Юникода</span><span class="sxs-lookup"><span data-stu-id="7decc-106">Unicode subrange</span></span></th>
<th><span data-ttu-id="7decc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7decc-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7decc-108">0</span><span class="sxs-lookup"><span data-stu-id="7decc-108">0</span></span></td>
<td><span data-ttu-id="7decc-109">0000 - 007F</span><span class="sxs-lookup"><span data-stu-id="7decc-109">0000 - 007F</span></span></td>
<td><span data-ttu-id="7decc-110">Базовая латиница</span><span class="sxs-lookup"><span data-stu-id="7decc-110">Basic Latin</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-111">1</span><span class="sxs-lookup"><span data-stu-id="7decc-111">1</span></span></td>
<td><span data-ttu-id="7decc-112">0080 - 00FF</span><span class="sxs-lookup"><span data-stu-id="7decc-112">0080 - 00FF</span></span></td>
<td><span data-ttu-id="7decc-113">Дополнительная латиница 1</span><span class="sxs-lookup"><span data-stu-id="7decc-113">Latin-1 Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-114">2</span><span class="sxs-lookup"><span data-stu-id="7decc-114">2</span></span></td>
<td><span data-ttu-id="7decc-115">0100 - 017F</span><span class="sxs-lookup"><span data-stu-id="7decc-115">0100 - 017F</span></span></td>
<td><span data-ttu-id="7decc-116">Расширенная латиница-A</span><span class="sxs-lookup"><span data-stu-id="7decc-116">Latin Extended-A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-117">3</span><span class="sxs-lookup"><span data-stu-id="7decc-117">3</span></span></td>
<td><span data-ttu-id="7decc-118">0180 - 024F</span><span class="sxs-lookup"><span data-stu-id="7decc-118">0180 - 024F</span></span></td>
<td><span data-ttu-id="7decc-119">Расширенная латиница-B</span><span class="sxs-lookup"><span data-stu-id="7decc-119">Latin Extended-B</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="7decc-120">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-120">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-121">0250 - 02AF</span><span class="sxs-lookup"><span data-stu-id="7decc-121">0250 - 02AF</span></span></td>
<td><span data-ttu-id="7decc-122">Расширения IPA</span><span class="sxs-lookup"><span data-stu-id="7decc-122">IPA Extensions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-123">1D00 - 1D7F</span><span class="sxs-lookup"><span data-stu-id="7decc-123">1D00 - 1D7F</span></span></td>
<td><span data-ttu-id="7decc-124">Фонетические расширения</span><span class="sxs-lookup"><span data-stu-id="7decc-124">Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-125">1D80 - 1DBF</span><span class="sxs-lookup"><span data-stu-id="7decc-125">1D80 - 1DBF</span></span></td>
<td><span data-ttu-id="7decc-126">Дополнение к фонетическим расширениям</span><span class="sxs-lookup"><span data-stu-id="7decc-126">Phonetic Extensions Supplement</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="7decc-127">5 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-127">5${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-128">02B0 - 02FF</span><span class="sxs-lookup"><span data-stu-id="7decc-128">02B0 - 02FF</span></span></td>
<td><span data-ttu-id="7decc-129">Буквы модификаторов расстояний</span><span class="sxs-lookup"><span data-stu-id="7decc-129">Spacing Modifier Letters</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-130">A700 - A71F</span><span class="sxs-lookup"><span data-stu-id="7decc-130">A700 - A71F</span></span></td>
<td><span data-ttu-id="7decc-131">Буквы тоновых модификаторов</span><span class="sxs-lookup"><span data-stu-id="7decc-131">Modifier Tone Letters</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="7decc-132">6 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-132">6${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-133">0300 - 036F</span><span class="sxs-lookup"><span data-stu-id="7decc-133">0300 - 036F</span></span></td>
<td><span data-ttu-id="7decc-134">Сочетание диакритических знаков</span><span class="sxs-lookup"><span data-stu-id="7decc-134">Combining Diacritical Marks</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-135">1DC0 - 1DFF</span><span class="sxs-lookup"><span data-stu-id="7decc-135">1DC0 - 1DFF</span></span></td>
<td><span data-ttu-id="7decc-136">Дополняющие диакритические знаки</span><span class="sxs-lookup"><span data-stu-id="7decc-136">Combining Diacritical Marks Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-137">7</span><span class="sxs-lookup"><span data-stu-id="7decc-137">7</span></span></td>
<td><span data-ttu-id="7decc-138">0370 - 03FF</span><span class="sxs-lookup"><span data-stu-id="7decc-138">0370 - 03FF</span></span></td>
<td><span data-ttu-id="7decc-139">Греческий и Коптский</span><span class="sxs-lookup"><span data-stu-id="7decc-139">Greek and Coptic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-140">8</span><span class="sxs-lookup"><span data-stu-id="7decc-140">8</span></span></td>
<td><span data-ttu-id="7decc-141">2C80 - 2CFF</span><span class="sxs-lookup"><span data-stu-id="7decc-141">2C80 - 2CFF</span></span></td>
<td><span data-ttu-id="7decc-142">Коптский</span><span class="sxs-lookup"><span data-stu-id="7decc-142">Coptic</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="7decc-143">9 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-143">9${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-144">0400 - 04FF</span><span class="sxs-lookup"><span data-stu-id="7decc-144">0400 - 04FF</span></span></td>
<td><span data-ttu-id="7decc-145">Кириллица</span><span class="sxs-lookup"><span data-stu-id="7decc-145">Cyrillic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-146">0500 - 052F</span><span class="sxs-lookup"><span data-stu-id="7decc-146">0500 - 052F</span></span></td>
<td><span data-ttu-id="7decc-147">Дополнение для кириллицы</span><span class="sxs-lookup"><span data-stu-id="7decc-147">Cyrillic Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-148">2DE0 - 2DFF</span><span class="sxs-lookup"><span data-stu-id="7decc-148">2DE0 - 2DFF</span></span></td>
<td><span data-ttu-id="7decc-149">Кириллица, расширенная — A</span><span class="sxs-lookup"><span data-stu-id="7decc-149">Cyrillic Extended-A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-150">A640 - A69F</span><span class="sxs-lookup"><span data-stu-id="7decc-150">A640 - A69F</span></span></td>
<td><span data-ttu-id="7decc-151">Кириллица, расширенная — B</span><span class="sxs-lookup"><span data-stu-id="7decc-151">Cyrillic Extended-B</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-152">10</span><span class="sxs-lookup"><span data-stu-id="7decc-152">10</span></span></td>
<td><span data-ttu-id="7decc-153">0530 - 058F</span><span class="sxs-lookup"><span data-stu-id="7decc-153">0530 - 058F</span></span></td>
<td><span data-ttu-id="7decc-154">Армянский</span><span class="sxs-lookup"><span data-stu-id="7decc-154">Armenian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-155">11</span><span class="sxs-lookup"><span data-stu-id="7decc-155">11</span></span></td>
<td><span data-ttu-id="7decc-156">0590 - 05FF</span><span class="sxs-lookup"><span data-stu-id="7decc-156">0590 - 05FF</span></span></td>
<td><span data-ttu-id="7decc-157">Иврит</span><span class="sxs-lookup"><span data-stu-id="7decc-157">Hebrew</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-158">12</span><span class="sxs-lookup"><span data-stu-id="7decc-158">12</span></span></td>
<td><span data-ttu-id="7decc-159">A500 - A63F</span><span class="sxs-lookup"><span data-stu-id="7decc-159">A500 - A63F</span></span></td>
<td><span data-ttu-id="7decc-160">Ваи</span><span class="sxs-lookup"><span data-stu-id="7decc-160">Vai</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7decc-161">13 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-161">13${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-162">0600 - 06FF</span><span class="sxs-lookup"><span data-stu-id="7decc-162">0600 - 06FF</span></span></td>
<td><span data-ttu-id="7decc-163">Арабский</span><span class="sxs-lookup"><span data-stu-id="7decc-163">Arabic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-164">0750-077F</span><span class="sxs-lookup"><span data-stu-id="7decc-164">0750 - 077F</span></span></td>
<td><span data-ttu-id="7decc-165">Дополнение для арабского языка</span><span class="sxs-lookup"><span data-stu-id="7decc-165">Arabic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-166">14</span><span class="sxs-lookup"><span data-stu-id="7decc-166">14</span></span></td>
<td><span data-ttu-id="7decc-167">07C0 - 07FF</span><span class="sxs-lookup"><span data-stu-id="7decc-167">07C0 - 07FF</span></span></td>
<td><span data-ttu-id="7decc-168">Блок</span><span class="sxs-lookup"><span data-stu-id="7decc-168">NKo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-169">15</span><span class="sxs-lookup"><span data-stu-id="7decc-169">15</span></span></td>
<td><span data-ttu-id="7decc-170">0900 - 097F</span><span class="sxs-lookup"><span data-stu-id="7decc-170">0900 - 097F</span></span></td>
<td><span data-ttu-id="7decc-171">Девангари</span><span class="sxs-lookup"><span data-stu-id="7decc-171">Devanagari</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-172">16</span><span class="sxs-lookup"><span data-stu-id="7decc-172">16</span></span></td>
<td><span data-ttu-id="7decc-173">0980 - 09FF</span><span class="sxs-lookup"><span data-stu-id="7decc-173">0980 - 09FF</span></span></td>
<td><span data-ttu-id="7decc-174">Бенгальский</span><span class="sxs-lookup"><span data-stu-id="7decc-174">Bangla</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-175">17</span><span class="sxs-lookup"><span data-stu-id="7decc-175">17</span></span></td>
<td><span data-ttu-id="7decc-176">0A00 - 0A7F</span><span class="sxs-lookup"><span data-stu-id="7decc-176">0A00 - 0A7F</span></span></td>
<td><span data-ttu-id="7decc-177">Гурмукхи</span><span class="sxs-lookup"><span data-stu-id="7decc-177">Gurmukhi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-178">18</span><span class="sxs-lookup"><span data-stu-id="7decc-178">18</span></span></td>
<td><span data-ttu-id="7decc-179">0A80 - 0AFF</span><span class="sxs-lookup"><span data-stu-id="7decc-179">0A80 - 0AFF</span></span></td>
<td><span data-ttu-id="7decc-180">Гуджарати</span><span class="sxs-lookup"><span data-stu-id="7decc-180">Gujarati</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-181">19</span><span class="sxs-lookup"><span data-stu-id="7decc-181">19</span></span></td>
<td><span data-ttu-id="7decc-182">0B00 - 0B7F</span><span class="sxs-lookup"><span data-stu-id="7decc-182">0B00 - 0B7F</span></span></td>
<td><span data-ttu-id="7decc-183">Ория</span><span class="sxs-lookup"><span data-stu-id="7decc-183">Odia</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-184">20</span><span class="sxs-lookup"><span data-stu-id="7decc-184">20</span></span></td>
<td><span data-ttu-id="7decc-185">0B80 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="7decc-185">0B80 - 0BFF</span></span></td>
<td><span data-ttu-id="7decc-186">Тамильский</span><span class="sxs-lookup"><span data-stu-id="7decc-186">Tamil</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-187">21</span><span class="sxs-lookup"><span data-stu-id="7decc-187">21</span></span></td>
<td><span data-ttu-id="7decc-188">0C00 - 0C7F</span><span class="sxs-lookup"><span data-stu-id="7decc-188">0C00 - 0C7F</span></span></td>
<td><span data-ttu-id="7decc-189">Телугу</span><span class="sxs-lookup"><span data-stu-id="7decc-189">Telugu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-190">22</span><span class="sxs-lookup"><span data-stu-id="7decc-190">22</span></span></td>
<td><span data-ttu-id="7decc-191">0C80 - 0CFF</span><span class="sxs-lookup"><span data-stu-id="7decc-191">0C80 - 0CFF</span></span></td>
<td><span data-ttu-id="7decc-192">Каннада</span><span class="sxs-lookup"><span data-stu-id="7decc-192">Kannada</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-193">23</span><span class="sxs-lookup"><span data-stu-id="7decc-193">23</span></span></td>
<td><span data-ttu-id="7decc-194">0D00 - 0D7F</span><span class="sxs-lookup"><span data-stu-id="7decc-194">0D00 - 0D7F</span></span></td>
<td><span data-ttu-id="7decc-195">Малаялам</span><span class="sxs-lookup"><span data-stu-id="7decc-195">Malayalam</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-196">24</span><span class="sxs-lookup"><span data-stu-id="7decc-196">24</span></span></td>
<td><span data-ttu-id="7decc-197">0E00 - 0E7F</span><span class="sxs-lookup"><span data-stu-id="7decc-197">0E00 - 0E7F</span></span></td>
<td><span data-ttu-id="7decc-198">Тайский</span><span class="sxs-lookup"><span data-stu-id="7decc-198">Thai</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-199">25</span><span class="sxs-lookup"><span data-stu-id="7decc-199">25</span></span></td>
<td><span data-ttu-id="7decc-200">0E80 - 0EFF</span><span class="sxs-lookup"><span data-stu-id="7decc-200">0E80 - 0EFF</span></span></td>
<td><span data-ttu-id="7decc-201">Лаосский</span><span class="sxs-lookup"><span data-stu-id="7decc-201">Lao</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7decc-202">26 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-202">26${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-203">10A0 - 10FF</span><span class="sxs-lookup"><span data-stu-id="7decc-203">10A0 - 10FF</span></span></td>
<td><span data-ttu-id="7decc-204">Грузинский</span><span class="sxs-lookup"><span data-stu-id="7decc-204">Georgian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-205">2D00 - 2D2F</span><span class="sxs-lookup"><span data-stu-id="7decc-205">2D00 - 2D2F</span></span></td>
<td><span data-ttu-id="7decc-206">Дополнительный грузинский</span><span class="sxs-lookup"><span data-stu-id="7decc-206">Georgian Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-207">27</span><span class="sxs-lookup"><span data-stu-id="7decc-207">27</span></span></td>
<td><span data-ttu-id="7decc-208">1B00 - 1B7F</span><span class="sxs-lookup"><span data-stu-id="7decc-208">1B00 - 1B7F</span></span></td>
<td><span data-ttu-id="7decc-209">Балийский</span><span class="sxs-lookup"><span data-stu-id="7decc-209">Balinese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-210">28</span><span class="sxs-lookup"><span data-stu-id="7decc-210">28</span></span></td>
<td><span data-ttu-id="7decc-211">1100 - 11FF</span><span class="sxs-lookup"><span data-stu-id="7decc-211">1100 - 11FF</span></span></td>
<td><span data-ttu-id="7decc-212">Знаки хангыль</span><span class="sxs-lookup"><span data-stu-id="7decc-212">Hangul Jamo</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="7decc-213">29 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-213">29${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-214">1E00 - 1EFF</span><span class="sxs-lookup"><span data-stu-id="7decc-214">1E00 - 1EFF</span></span></td>
<td><span data-ttu-id="7decc-215">Расширенная латиница дополнительно</span><span class="sxs-lookup"><span data-stu-id="7decc-215">Latin Extended Additional</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-216">2C60 - 2C7F</span><span class="sxs-lookup"><span data-stu-id="7decc-216">2C60 - 2C7F</span></span></td>
<td><span data-ttu-id="7decc-217">Латиница Extended-C</span><span class="sxs-lookup"><span data-stu-id="7decc-217">Latin Extended-C</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-218">A720 - A7FF</span><span class="sxs-lookup"><span data-stu-id="7decc-218">A720 - A7FF</span></span></td>
<td><span data-ttu-id="7decc-219">Расширенная латиница-D</span><span class="sxs-lookup"><span data-stu-id="7decc-219">Latin Extended-D</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-220">30</span><span class="sxs-lookup"><span data-stu-id="7decc-220">30</span></span></td>
<td><span data-ttu-id="7decc-221">1F00 - 1FFF</span><span class="sxs-lookup"><span data-stu-id="7decc-221">1F00 - 1FFF</span></span></td>
<td><span data-ttu-id="7decc-222">Греческий расширенный</span><span class="sxs-lookup"><span data-stu-id="7decc-222">Greek Extended</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7decc-223">31 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-223">31${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-224">2000 - 206F</span><span class="sxs-lookup"><span data-stu-id="7decc-224">2000 - 206F</span></span></td>
<td><span data-ttu-id="7decc-225">Общие знаки препинания</span><span class="sxs-lookup"><span data-stu-id="7decc-225">General Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-226">2E00 - 2E7F</span><span class="sxs-lookup"><span data-stu-id="7decc-226">2E00 - 2E7F</span></span></td>
<td><span data-ttu-id="7decc-227">Дополнительные знаки препинания</span><span class="sxs-lookup"><span data-stu-id="7decc-227">Supplemental Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-228">32</span><span class="sxs-lookup"><span data-stu-id="7decc-228">32</span></span></td>
<td><span data-ttu-id="7decc-229">2070 - 209F</span><span class="sxs-lookup"><span data-stu-id="7decc-229">2070 - 209F</span></span></td>
<td><span data-ttu-id="7decc-230">Надстрочные и подстрочные индексы</span><span class="sxs-lookup"><span data-stu-id="7decc-230">Superscripts And Subscripts</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-231">33</span><span class="sxs-lookup"><span data-stu-id="7decc-231">33</span></span></td>
<td><span data-ttu-id="7decc-232">20A0 - 20CF</span><span class="sxs-lookup"><span data-stu-id="7decc-232">20A0 - 20CF</span></span></td>
<td><span data-ttu-id="7decc-233">Символы валют</span><span class="sxs-lookup"><span data-stu-id="7decc-233">Currency Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-234">34</span><span class="sxs-lookup"><span data-stu-id="7decc-234">34</span></span></td>
<td><span data-ttu-id="7decc-235">20D0 - 20FF</span><span class="sxs-lookup"><span data-stu-id="7decc-235">20D0 - 20FF</span></span></td>
<td><span data-ttu-id="7decc-236">Сочетание диакритических знаков для символов</span><span class="sxs-lookup"><span data-stu-id="7decc-236">Combining Diacritical Marks For Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-237">35</span><span class="sxs-lookup"><span data-stu-id="7decc-237">35</span></span></td>
<td><span data-ttu-id="7decc-238">2100 - 214F</span><span class="sxs-lookup"><span data-stu-id="7decc-238">2100 - 214F</span></span></td>
<td><span data-ttu-id="7decc-239">Буквоподобных символы</span><span class="sxs-lookup"><span data-stu-id="7decc-239">Letterlike Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-240">36</span><span class="sxs-lookup"><span data-stu-id="7decc-240">36</span></span></td>
<td><span data-ttu-id="7decc-241">2150 - 218F</span><span class="sxs-lookup"><span data-stu-id="7decc-241">2150 - 218F</span></span></td>
<td><span data-ttu-id="7decc-242">Числовые формы</span><span class="sxs-lookup"><span data-stu-id="7decc-242">Number Forms</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="7decc-243">37 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-243">37${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-244">2190 - 21FF</span><span class="sxs-lookup"><span data-stu-id="7decc-244">2190 - 21FF</span></span></td>
<td><span data-ttu-id="7decc-245">Стрелки</span><span class="sxs-lookup"><span data-stu-id="7decc-245">Arrows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-246">27F0 - 27FF</span><span class="sxs-lookup"><span data-stu-id="7decc-246">27F0 - 27FF</span></span></td>
<td><span data-ttu-id="7decc-247">Дополнительные стрелки</span><span class="sxs-lookup"><span data-stu-id="7decc-247">Supplemental Arrows-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-248">2900 - 297F</span><span class="sxs-lookup"><span data-stu-id="7decc-248">2900 - 297F</span></span></td>
<td><span data-ttu-id="7decc-249">Дополнительные стрелки — B</span><span class="sxs-lookup"><span data-stu-id="7decc-249">Supplemental Arrows-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-250">2B00 - 2BFF</span><span class="sxs-lookup"><span data-stu-id="7decc-250">2B00 - 2BFF</span></span></td>
<td><span data-ttu-id="7decc-251">Различные символы и стрелки</span><span class="sxs-lookup"><span data-stu-id="7decc-251">Miscellaneous Symbols and Arrows</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="7decc-252">38 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-252">38${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-253">2200 - 22FF</span><span class="sxs-lookup"><span data-stu-id="7decc-253">2200 - 22FF</span></span></td>
<td><span data-ttu-id="7decc-254">Математические операторы</span><span class="sxs-lookup"><span data-stu-id="7decc-254">Mathematical Operators</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-255">27C0 - 27EF</span><span class="sxs-lookup"><span data-stu-id="7decc-255">27C0 - 27EF</span></span></td>
<td><span data-ttu-id="7decc-256">Различные математические символы — A</span><span class="sxs-lookup"><span data-stu-id="7decc-256">Miscellaneous Mathematical Symbols-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-257">2980 - 29FF</span><span class="sxs-lookup"><span data-stu-id="7decc-257">2980 - 29FF</span></span></td>
<td><span data-ttu-id="7decc-258">Различные математические символы — B</span><span class="sxs-lookup"><span data-stu-id="7decc-258">Miscellaneous Mathematical Symbols-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-259">2A00 - 2AFF</span><span class="sxs-lookup"><span data-stu-id="7decc-259">2A00 - 2AFF</span></span></td>
<td><span data-ttu-id="7decc-260">Дополнительные математические операторы</span><span class="sxs-lookup"><span data-stu-id="7decc-260">Supplemental Mathematical Operators</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-261">39</span><span class="sxs-lookup"><span data-stu-id="7decc-261">39</span></span></td>
<td><span data-ttu-id="7decc-262">2300 - 23FF</span><span class="sxs-lookup"><span data-stu-id="7decc-262">2300 - 23FF</span></span></td>
<td><span data-ttu-id="7decc-263">Прочие технические</span><span class="sxs-lookup"><span data-stu-id="7decc-263">Miscellaneous Technical</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-264">40</span><span class="sxs-lookup"><span data-stu-id="7decc-264">40</span></span></td>
<td><span data-ttu-id="7decc-265">2400 - 243F</span><span class="sxs-lookup"><span data-stu-id="7decc-265">2400 - 243F</span></span></td>
<td><span data-ttu-id="7decc-266">Управление рисунками</span><span class="sxs-lookup"><span data-stu-id="7decc-266">Control Pictures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-267">41</span><span class="sxs-lookup"><span data-stu-id="7decc-267">41</span></span></td>
<td><span data-ttu-id="7decc-268">2440 - 245F</span><span class="sxs-lookup"><span data-stu-id="7decc-268">2440 - 245F</span></span></td>
<td><span data-ttu-id="7decc-269">Оптическое распознавание символов</span><span class="sxs-lookup"><span data-stu-id="7decc-269">Optical Character Recognition</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-270">42</span><span class="sxs-lookup"><span data-stu-id="7decc-270">42</span></span></td>
<td><span data-ttu-id="7decc-271">2460 - 24FF</span><span class="sxs-lookup"><span data-stu-id="7decc-271">2460 - 24FF</span></span></td>
<td><span data-ttu-id="7decc-272">Вложенные буквенно-цифровые символы</span><span class="sxs-lookup"><span data-stu-id="7decc-272">Enclosed Alphanumerics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-273">43</span><span class="sxs-lookup"><span data-stu-id="7decc-273">43</span></span></td>
<td><span data-ttu-id="7decc-274">2500 - 257F</span><span class="sxs-lookup"><span data-stu-id="7decc-274">2500 - 257F</span></span></td>
<td><span data-ttu-id="7decc-275">Рисование Box</span><span class="sxs-lookup"><span data-stu-id="7decc-275">Box Drawing</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-276">44</span><span class="sxs-lookup"><span data-stu-id="7decc-276">44</span></span></td>
<td><span data-ttu-id="7decc-277">2580 - 259F</span><span class="sxs-lookup"><span data-stu-id="7decc-277">2580 - 259F</span></span></td>
<td><span data-ttu-id="7decc-278">Блочные элементы</span><span class="sxs-lookup"><span data-stu-id="7decc-278">Block Elements</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-279">45</span><span class="sxs-lookup"><span data-stu-id="7decc-279">45</span></span></td>
<td><span data-ttu-id="7decc-280">25A0 - 25FF</span><span class="sxs-lookup"><span data-stu-id="7decc-280">25A0 - 25FF</span></span></td>
<td><span data-ttu-id="7decc-281">Геометрические фигуры</span><span class="sxs-lookup"><span data-stu-id="7decc-281">Geometric Shapes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-282">46</span><span class="sxs-lookup"><span data-stu-id="7decc-282">46</span></span></td>
<td><span data-ttu-id="7decc-283">2600 - 26FF</span><span class="sxs-lookup"><span data-stu-id="7decc-283">2600 - 26FF</span></span></td>
<td><span data-ttu-id="7decc-284">Прочие символы</span><span class="sxs-lookup"><span data-stu-id="7decc-284">Miscellaneous Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-285">47</span><span class="sxs-lookup"><span data-stu-id="7decc-285">47</span></span></td>
<td><span data-ttu-id="7decc-286">2700 - 27BF</span><span class="sxs-lookup"><span data-stu-id="7decc-286">2700 - 27BF</span></span></td>
<td><span data-ttu-id="7decc-287">Dingbats</span><span class="sxs-lookup"><span data-stu-id="7decc-287">Dingbats</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-288">48</span><span class="sxs-lookup"><span data-stu-id="7decc-288">48</span></span></td>
<td><span data-ttu-id="7decc-289">3000 - 303F</span><span class="sxs-lookup"><span data-stu-id="7decc-289">3000 - 303F</span></span></td>
<td><span data-ttu-id="7decc-290">ККЯ — символы и пунктуация</span><span class="sxs-lookup"><span data-stu-id="7decc-290">CJK Symbols And Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-291">49</span><span class="sxs-lookup"><span data-stu-id="7decc-291">49</span></span></td>
<td><span data-ttu-id="7decc-292">3040 - 309F</span><span class="sxs-lookup"><span data-stu-id="7decc-292">3040 - 309F</span></span></td>
<td><span data-ttu-id="7decc-293">Хирагана</span><span class="sxs-lookup"><span data-stu-id="7decc-293">Hiragana</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7decc-294">50 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-294">50${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-295">30A0 - 30FF</span><span class="sxs-lookup"><span data-stu-id="7decc-295">30A0 - 30FF</span></span></td>
<td><span data-ttu-id="7decc-296">Катакана</span><span class="sxs-lookup"><span data-stu-id="7decc-296">Katakana</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-297">31F0 - 31FF</span><span class="sxs-lookup"><span data-stu-id="7decc-297">31F0 - 31FF</span></span></td>
<td><span data-ttu-id="7decc-298">Фонетические расширения катакана</span><span class="sxs-lookup"><span data-stu-id="7decc-298">Katakana Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7decc-299">51 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-299">51${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-300">3100 - 312F</span><span class="sxs-lookup"><span data-stu-id="7decc-300">3100 - 312F</span></span></td>
<td><span data-ttu-id="7decc-301">Бопомофо</span><span class="sxs-lookup"><span data-stu-id="7decc-301">Bopomofo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-302">31A0 - 31BF</span><span class="sxs-lookup"><span data-stu-id="7decc-302">31A0 - 31BF</span></span></td>
<td><span data-ttu-id="7decc-303">Расширенный бопомофо</span><span class="sxs-lookup"><span data-stu-id="7decc-303">Bopomofo Extended</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-304">52</span><span class="sxs-lookup"><span data-stu-id="7decc-304">52</span></span></td>
<td><span data-ttu-id="7decc-305">3130 - 318F</span><span class="sxs-lookup"><span data-stu-id="7decc-305">3130 - 318F</span></span></td>
<td><span data-ttu-id="7decc-306">Знаки совместимости хангыль</span><span class="sxs-lookup"><span data-stu-id="7decc-306">Hangul Compatibility Jamo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-307">53</span><span class="sxs-lookup"><span data-stu-id="7decc-307">53</span></span></td>
<td><span data-ttu-id="7decc-308">A840 - A87F</span><span class="sxs-lookup"><span data-stu-id="7decc-308">A840 - A87F</span></span></td>
<td><span data-ttu-id="7decc-309">Блок-PA</span><span class="sxs-lookup"><span data-stu-id="7decc-309">Phags-pa</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-310">54</span><span class="sxs-lookup"><span data-stu-id="7decc-310">54</span></span></td>
<td><span data-ttu-id="7decc-311">3200 - 32FF</span><span class="sxs-lookup"><span data-stu-id="7decc-311">3200 - 32FF</span></span></td>
<td><span data-ttu-id="7decc-312">Вложенные символы CJK и месяцы</span><span class="sxs-lookup"><span data-stu-id="7decc-312">Enclosed CJK Letters And Months</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-313">55</span><span class="sxs-lookup"><span data-stu-id="7decc-313">55</span></span></td>
<td><span data-ttu-id="7decc-314">3300 - 33FF</span><span class="sxs-lookup"><span data-stu-id="7decc-314">3300 - 33FF</span></span></td>
<td><span data-ttu-id="7decc-315">ККЯ — совместимость</span><span class="sxs-lookup"><span data-stu-id="7decc-315">CJK Compatibility</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-316">56</span><span class="sxs-lookup"><span data-stu-id="7decc-316">56</span></span></td>
<td><span data-ttu-id="7decc-317">AC00 - D7AF</span><span class="sxs-lookup"><span data-stu-id="7decc-317">AC00 - D7AF</span></span></td>
<td><span data-ttu-id="7decc-318">Слоги хангыль</span><span class="sxs-lookup"><span data-stu-id="7decc-318">Hangul Syllables</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-319">57</span><span class="sxs-lookup"><span data-stu-id="7decc-319">57</span></span></td>
<td><span data-ttu-id="7decc-320">D800-DFFF</span><span class="sxs-lookup"><span data-stu-id="7decc-320">D800 - DFFF</span></span></td>
<td><span data-ttu-id="7decc-321">Не плоскость 0.</span><span class="sxs-lookup"><span data-stu-id="7decc-321">Non-Plane 0.</span></span> <span data-ttu-id="7decc-322">Обратите внимание, что установка этого бита подразумевает наличие по крайней мере одной дополнительной кодовой точки за пределами основной многоязычной плоскости (BMP), поддерживаемой этим шрифтом.</span><span class="sxs-lookup"><span data-stu-id="7decc-322">Note that setting this bit implies that there is at least one supplementary code point beyond the Basic Multilingual Plane (BMP) that is supported by this font.</span></span> <span data-ttu-id="7decc-323">См. Дополнительные сведения о <a href="surrogates-and-supplementary-characters.md">суррогатах и добавочных символах</a>.</span><span class="sxs-lookup"><span data-stu-id="7decc-323">See <a href="surrogates-and-supplementary-characters.md">Surrogates and Supplementary Characters</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-324">58</span><span class="sxs-lookup"><span data-stu-id="7decc-324">58</span></span></td>
<td><span data-ttu-id="7decc-325">10900-1091F</span><span class="sxs-lookup"><span data-stu-id="7decc-325">10900 - 1091F</span></span></td>
<td><span data-ttu-id="7decc-326">Финикийский алфавит</span><span class="sxs-lookup"><span data-stu-id="7decc-326">Phoenician</span></span></td>
</tr>
<tr class="even">
<td rowspan="7"><span data-ttu-id="7decc-327">59 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-327">59${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-328">2E80 - 2EFF</span><span class="sxs-lookup"><span data-stu-id="7decc-328">2E80 - 2EFF</span></span></td>
<td><span data-ttu-id="7decc-329">Дополнительные радикалы CJK</span><span class="sxs-lookup"><span data-stu-id="7decc-329">CJK Radicals Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-330">2F00 - 2FDF</span><span class="sxs-lookup"><span data-stu-id="7decc-330">2F00 - 2FDF</span></span></td>
<td><span data-ttu-id="7decc-331">Радикалы кандзи</span><span class="sxs-lookup"><span data-stu-id="7decc-331">Kangxi Radicals</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-332">2FF0 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="7decc-332">2FF0 - 2FFF</span></span></td>
<td><span data-ttu-id="7decc-333">Идеографические символы описания</span><span class="sxs-lookup"><span data-stu-id="7decc-333">Ideographic Description Characters</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-334">3190 - 319F</span><span class="sxs-lookup"><span data-stu-id="7decc-334">3190 - 319F</span></span></td>
<td><span data-ttu-id="7decc-335">Канбуна</span><span class="sxs-lookup"><span data-stu-id="7decc-335">Kanbun</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-336">3400 - 4DBF</span><span class="sxs-lookup"><span data-stu-id="7decc-336">3400 - 4DBF</span></span></td>
<td><span data-ttu-id="7decc-337">ККЯ — унифицированные иероглифы, расширение A</span><span class="sxs-lookup"><span data-stu-id="7decc-337">CJK Unified Ideographs Extension A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-338">4E00 - 9FFF</span><span class="sxs-lookup"><span data-stu-id="7decc-338">4E00 - 9FFF</span></span></td>
<td><span data-ttu-id="7decc-339">ККЯ — унифицированные иероглифы</span><span class="sxs-lookup"><span data-stu-id="7decc-339">CJK Unified Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-340">20000-2A6DF</span><span class="sxs-lookup"><span data-stu-id="7decc-340">20000 - 2A6DF</span></span></td>
<td><span data-ttu-id="7decc-341">ККЯ — унифицированные иероглифы, расширение B</span><span class="sxs-lookup"><span data-stu-id="7decc-341">CJK Unified Ideographs Extension B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-342">60</span><span class="sxs-lookup"><span data-stu-id="7decc-342">60</span></span></td>
<td><span data-ttu-id="7decc-343">E000 - F8FF</span><span class="sxs-lookup"><span data-stu-id="7decc-343">E000 - F8FF</span></span></td>
<td><span data-ttu-id="7decc-344">Область закрытого использования</span><span class="sxs-lookup"><span data-stu-id="7decc-344">Private Use Area</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="7decc-345">61 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-345">61${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-346">31C0 - 31EF</span><span class="sxs-lookup"><span data-stu-id="7decc-346">31C0 - 31EF</span></span></td>
<td><span data-ttu-id="7decc-347">ККЯ — штрихи</span><span class="sxs-lookup"><span data-stu-id="7decc-347">CJK Strokes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-348">F900 - FAFF</span><span class="sxs-lookup"><span data-stu-id="7decc-348">F900 - FAFF</span></span></td>
<td><span data-ttu-id="7decc-349">ККЯ — иероглифы совместимости</span><span class="sxs-lookup"><span data-stu-id="7decc-349">CJK Compatibility Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-350">2F800 - 2FA1F</span><span class="sxs-lookup"><span data-stu-id="7decc-350">2F800 - 2FA1F</span></span></td>
<td><span data-ttu-id="7decc-351">ККЯ — дополнительные иероглифы совместимости</span><span class="sxs-lookup"><span data-stu-id="7decc-351">CJK Compatibility Ideographs Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-352">62</span><span class="sxs-lookup"><span data-stu-id="7decc-352">62</span></span></td>
<td><span data-ttu-id="7decc-353">FB00 - FB4F</span><span class="sxs-lookup"><span data-stu-id="7decc-353">FB00 - FB4F</span></span></td>
<td><span data-ttu-id="7decc-354">Формы представления по алфавиту</span><span class="sxs-lookup"><span data-stu-id="7decc-354">Alphabetic Presentation Forms</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-355">63</span><span class="sxs-lookup"><span data-stu-id="7decc-355">63</span></span></td>
<td><span data-ttu-id="7decc-356">FB50 - FDFF</span><span class="sxs-lookup"><span data-stu-id="7decc-356">FB50 - FDFF</span></span></td>
<td><span data-ttu-id="7decc-357">Формы для арабского представления — A</span><span class="sxs-lookup"><span data-stu-id="7decc-357">Arabic Presentation Forms-A</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-358">64</span><span class="sxs-lookup"><span data-stu-id="7decc-358">64</span></span></td>
<td><span data-ttu-id="7decc-359">FE20 - FE2F</span><span class="sxs-lookup"><span data-stu-id="7decc-359">FE20 - FE2F</span></span></td>
<td><span data-ttu-id="7decc-360">Объединение половинных делений</span><span class="sxs-lookup"><span data-stu-id="7decc-360">Combining Half Marks</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="7decc-361">65 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-361">65${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-362">FE10 - FE1F</span><span class="sxs-lookup"><span data-stu-id="7decc-362">FE10 - FE1F</span></span></td>
<td><span data-ttu-id="7decc-363">Вертикальные формы</span><span class="sxs-lookup"><span data-stu-id="7decc-363">Vertical Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-364">FE30 - FE4F</span><span class="sxs-lookup"><span data-stu-id="7decc-364">FE30 - FE4F</span></span></td>
<td><span data-ttu-id="7decc-365">ККЯ — формы совместимости</span><span class="sxs-lookup"><span data-stu-id="7decc-365">CJK Compatibility Forms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-366">66</span><span class="sxs-lookup"><span data-stu-id="7decc-366">66</span></span></td>
<td><span data-ttu-id="7decc-367">FE50 - FE6F</span><span class="sxs-lookup"><span data-stu-id="7decc-367">FE50 - FE6F</span></span></td>
<td><span data-ttu-id="7decc-368">Варианты малых форм</span><span class="sxs-lookup"><span data-stu-id="7decc-368">Small Form Variants</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-369">67</span><span class="sxs-lookup"><span data-stu-id="7decc-369">67</span></span></td>
<td><span data-ttu-id="7decc-370">FE70 - FEFF</span><span class="sxs-lookup"><span data-stu-id="7decc-370">FE70 - FEFF</span></span></td>
<td><span data-ttu-id="7decc-371">Формы для арабского представления — B</span><span class="sxs-lookup"><span data-stu-id="7decc-371">Arabic Presentation Forms-B</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-372">68</span><span class="sxs-lookup"><span data-stu-id="7decc-372">68</span></span></td>
<td><span data-ttu-id="7decc-373">FF00 - FFEF</span><span class="sxs-lookup"><span data-stu-id="7decc-373">FF00 - FFEF</span></span></td>
<td><span data-ttu-id="7decc-374">Формы с шириной в полуширинные и в виде ширины</span><span class="sxs-lookup"><span data-stu-id="7decc-374">Halfwidth And Fullwidth Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-375">69</span><span class="sxs-lookup"><span data-stu-id="7decc-375">69</span></span></td>
<td><span data-ttu-id="7decc-376">FFF0 - FFFF</span><span class="sxs-lookup"><span data-stu-id="7decc-376">FFF0 - FFFF</span></span></td>
<td><span data-ttu-id="7decc-377">Блок</span><span class="sxs-lookup"><span data-stu-id="7decc-377">Specials</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-378">70</span><span class="sxs-lookup"><span data-stu-id="7decc-378">70</span></span></td>
<td><span data-ttu-id="7decc-379">0F00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="7decc-379">0F00 - 0FFF</span></span></td>
<td><span data-ttu-id="7decc-380">Тибетский</span><span class="sxs-lookup"><span data-stu-id="7decc-380">Tibetan</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-381">71</span><span class="sxs-lookup"><span data-stu-id="7decc-381">71</span></span></td>
<td><span data-ttu-id="7decc-382">0700 - 074F</span><span class="sxs-lookup"><span data-stu-id="7decc-382">0700 - 074F</span></span></td>
<td><span data-ttu-id="7decc-383">Сирийский</span><span class="sxs-lookup"><span data-stu-id="7decc-383">Syriac</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-384">72</span><span class="sxs-lookup"><span data-stu-id="7decc-384">72</span></span></td>
<td><span data-ttu-id="7decc-385">0780 - 07BF</span><span class="sxs-lookup"><span data-stu-id="7decc-385">0780 - 07BF</span></span></td>
<td><span data-ttu-id="7decc-386">мальдивский</span><span class="sxs-lookup"><span data-stu-id="7decc-386">Thaana</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-387">73</span><span class="sxs-lookup"><span data-stu-id="7decc-387">73</span></span></td>
<td><span data-ttu-id="7decc-388">0D80 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="7decc-388">0D80 - 0DFF</span></span></td>
<td><span data-ttu-id="7decc-389">Сингальский</span><span class="sxs-lookup"><span data-stu-id="7decc-389">Sinhala</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-390">74</span><span class="sxs-lookup"><span data-stu-id="7decc-390">74</span></span></td>
<td><span data-ttu-id="7decc-391">1000 - 109F</span><span class="sxs-lookup"><span data-stu-id="7decc-391">1000 - 109F</span></span></td>
<td><span data-ttu-id="7decc-392">Мьянма</span><span class="sxs-lookup"><span data-stu-id="7decc-392">Myanmar</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="7decc-393">75 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-393">75${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-394">1200 - 137F</span><span class="sxs-lookup"><span data-stu-id="7decc-394">1200 - 137F</span></span></td>
<td><span data-ttu-id="7decc-395">Эфиопского</span><span class="sxs-lookup"><span data-stu-id="7decc-395">Ethiopic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-396">1380-139F</span><span class="sxs-lookup"><span data-stu-id="7decc-396">1380 - 139F</span></span></td>
<td><span data-ttu-id="7decc-397">Дополнение эфиопского</span><span class="sxs-lookup"><span data-stu-id="7decc-397">Ethiopic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-398">2D80 - 2DDF</span><span class="sxs-lookup"><span data-stu-id="7decc-398">2D80 - 2DDF</span></span></td>
<td><span data-ttu-id="7decc-399">Эфиопского Расширенная</span><span class="sxs-lookup"><span data-stu-id="7decc-399">Ethiopic Extended</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-400">76</span><span class="sxs-lookup"><span data-stu-id="7decc-400">76</span></span></td>
<td><span data-ttu-id="7decc-401">13A0 - 13FF</span><span class="sxs-lookup"><span data-stu-id="7decc-401">13A0 - 13FF</span></span></td>
<td><span data-ttu-id="7decc-402">Чероки</span><span class="sxs-lookup"><span data-stu-id="7decc-402">Cherokee</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-403">77</span><span class="sxs-lookup"><span data-stu-id="7decc-403">77</span></span></td>
<td><span data-ttu-id="7decc-404">1400 - 167F</span><span class="sxs-lookup"><span data-stu-id="7decc-404">1400 - 167F</span></span></td>
<td><span data-ttu-id="7decc-405">Унифицированное канадское письмо слогового письма</span><span class="sxs-lookup"><span data-stu-id="7decc-405">Unified Canadian Aboriginal Syllabics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-406">78</span><span class="sxs-lookup"><span data-stu-id="7decc-406">78</span></span></td>
<td><span data-ttu-id="7decc-407">1680 - 169F</span><span class="sxs-lookup"><span data-stu-id="7decc-407">1680 - 169F</span></span></td>
<td><span data-ttu-id="7decc-408">Блок</span><span class="sxs-lookup"><span data-stu-id="7decc-408">Ogham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-409">79</span><span class="sxs-lookup"><span data-stu-id="7decc-409">79</span></span></td>
<td><span data-ttu-id="7decc-410">16A0 - 16FF</span><span class="sxs-lookup"><span data-stu-id="7decc-410">16A0 - 16FF</span></span></td>
<td><span data-ttu-id="7decc-411">руник</span><span class="sxs-lookup"><span data-stu-id="7decc-411">Runic</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="7decc-412">80 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-412">80${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-413">1780 - 17FF</span><span class="sxs-lookup"><span data-stu-id="7decc-413">1780 - 17FF</span></span></td>
<td><span data-ttu-id="7decc-414">Кхмерский</span><span class="sxs-lookup"><span data-stu-id="7decc-414">Khmer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-415">19E0 - 19FF</span><span class="sxs-lookup"><span data-stu-id="7decc-415">19E0 - 19FF</span></span></td>
<td><span data-ttu-id="7decc-416">Кхмерский символ</span><span class="sxs-lookup"><span data-stu-id="7decc-416">Khmer Symbols</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-417">81</span><span class="sxs-lookup"><span data-stu-id="7decc-417">81</span></span></td>
<td><span data-ttu-id="7decc-418">1800 - 18AF</span><span class="sxs-lookup"><span data-stu-id="7decc-418">1800 - 18AF</span></span></td>
<td><span data-ttu-id="7decc-419">Монгольский</span><span class="sxs-lookup"><span data-stu-id="7decc-419">Mongolian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-420">82</span><span class="sxs-lookup"><span data-stu-id="7decc-420">82</span></span></td>
<td><span data-ttu-id="7decc-421">2800 - 28FF</span><span class="sxs-lookup"><span data-stu-id="7decc-421">2800 - 28FF</span></span></td>
<td><span data-ttu-id="7decc-422">Шаблоны Брайля</span><span class="sxs-lookup"><span data-stu-id="7decc-422">Braille Patterns</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="7decc-423">83 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-423">83${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-424">A000 - A48F</span><span class="sxs-lookup"><span data-stu-id="7decc-424">A000 - A48F</span></span></td>
<td><span data-ttu-id="7decc-425">Ий — слоги</span><span class="sxs-lookup"><span data-stu-id="7decc-425">Yi Syllables</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-426">A490 - A4CF</span><span class="sxs-lookup"><span data-stu-id="7decc-426">A490 - A4CF</span></span></td>
<td><span data-ttu-id="7decc-427">Радикалы в Yi</span><span class="sxs-lookup"><span data-stu-id="7decc-427">Yi Radicals</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="7decc-428">84 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-428">84${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-429">1700 - 171F</span><span class="sxs-lookup"><span data-stu-id="7decc-429">1700 - 171F</span></span></td>
<td><span data-ttu-id="7decc-430">Тагальский</span><span class="sxs-lookup"><span data-stu-id="7decc-430">Tagalog</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-431">1720 - 173F</span><span class="sxs-lookup"><span data-stu-id="7decc-431">1720 - 173F</span></span></td>
<td><span data-ttu-id="7decc-432">Блок</span><span class="sxs-lookup"><span data-stu-id="7decc-432">Hanunoo</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-433">1740 - 175F</span><span class="sxs-lookup"><span data-stu-id="7decc-433">1740 - 175F</span></span></td>
<td><span data-ttu-id="7decc-434">Бухид</span><span class="sxs-lookup"><span data-stu-id="7decc-434">Buhid</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-435">1760 - 177F</span><span class="sxs-lookup"><span data-stu-id="7decc-435">1760 - 177F</span></span></td>
<td><span data-ttu-id="7decc-436">Тагбануа</span><span class="sxs-lookup"><span data-stu-id="7decc-436">Tagbanwa</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-437">85</span><span class="sxs-lookup"><span data-stu-id="7decc-437">85</span></span></td>
<td><span data-ttu-id="7decc-438">10300-1032F</span><span class="sxs-lookup"><span data-stu-id="7decc-438">10300 - 1032F</span></span></td>
<td><span data-ttu-id="7decc-439">Старый курсив</span><span class="sxs-lookup"><span data-stu-id="7decc-439">Old Italic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-440">86</span><span class="sxs-lookup"><span data-stu-id="7decc-440">86</span></span></td>
<td><span data-ttu-id="7decc-441">10330-1034F</span><span class="sxs-lookup"><span data-stu-id="7decc-441">10330 - 1034F</span></span></td>
<td><span data-ttu-id="7decc-442">Arial</span><span class="sxs-lookup"><span data-stu-id="7decc-442">Gothic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-443">87</span><span class="sxs-lookup"><span data-stu-id="7decc-443">87</span></span></td>
<td><span data-ttu-id="7decc-444">10400-1044F</span><span class="sxs-lookup"><span data-stu-id="7decc-444">10400 - 1044F</span></span></td>
<td><span data-ttu-id="7decc-445">Дезерет</span><span class="sxs-lookup"><span data-stu-id="7decc-445">Deseret</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="7decc-446">88 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-446">88${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-447">1D000 - 1D0FF</span><span class="sxs-lookup"><span data-stu-id="7decc-447">1D000 - 1D0FF</span></span></td>
<td><span data-ttu-id="7decc-448">Бизантине Музыкальные символы</span><span class="sxs-lookup"><span data-stu-id="7decc-448">Byzantine Musical Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-449">1D100 - 1D1FF</span><span class="sxs-lookup"><span data-stu-id="7decc-449">1D100 - 1D1FF</span></span></td>
<td><span data-ttu-id="7decc-450">Музыкальные символы</span><span class="sxs-lookup"><span data-stu-id="7decc-450">Musical Symbols</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-451">1D200 - 1D24F</span><span class="sxs-lookup"><span data-stu-id="7decc-451">1D200 - 1D24F</span></span></td>
<td><span data-ttu-id="7decc-452">Античного греческая музыкальная нотация</span><span class="sxs-lookup"><span data-stu-id="7decc-452">Ancient Greek Musical Notation</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-453">89</span><span class="sxs-lookup"><span data-stu-id="7decc-453">89</span></span></td>
<td><span data-ttu-id="7decc-454">1D400 - 1D7FF</span><span class="sxs-lookup"><span data-stu-id="7decc-454">1D400 - 1D7FF</span></span></td>
<td><span data-ttu-id="7decc-455">Математические буквенно-цифровые символы</span><span class="sxs-lookup"><span data-stu-id="7decc-455">Mathematical Alphanumeric Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7decc-456">90 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-456">90${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-457">FF000-FFFF</span><span class="sxs-lookup"><span data-stu-id="7decc-457">FF000 - FFFFD</span></span></td>
<td><span data-ttu-id="7decc-458">Частное использование (плоскость 15)</span><span class="sxs-lookup"><span data-stu-id="7decc-458">Private Use (plane 15)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-459">100000-10FFFD</span><span class="sxs-lookup"><span data-stu-id="7decc-459">100000 - 10FFFD</span></span></td>
<td><span data-ttu-id="7decc-460">Частное использование (плоскость 16)</span><span class="sxs-lookup"><span data-stu-id="7decc-460">Private Use (plane 16)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7decc-461">91 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-461">91${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-462">FE00 - FE0F</span><span class="sxs-lookup"><span data-stu-id="7decc-462">FE00 - FE0F</span></span></td>
<td><span data-ttu-id="7decc-463">Селекторы вариантов</span><span class="sxs-lookup"><span data-stu-id="7decc-463">Variation Selectors</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-464">E0100 - E01EF</span><span class="sxs-lookup"><span data-stu-id="7decc-464">E0100 - E01EF</span></span></td>
<td><span data-ttu-id="7decc-465">Дополнение селекторов вариантов</span><span class="sxs-lookup"><span data-stu-id="7decc-465">Variation Selectors Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-466">92</span><span class="sxs-lookup"><span data-stu-id="7decc-466">92</span></span></td>
<td><span data-ttu-id="7decc-467">E0000 - E007F</span><span class="sxs-lookup"><span data-stu-id="7decc-467">E0000 - E007F</span></span></td>
<td><span data-ttu-id="7decc-468">Теги</span><span class="sxs-lookup"><span data-stu-id="7decc-468">Tags</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-469">93</span><span class="sxs-lookup"><span data-stu-id="7decc-469">93</span></span></td>
<td><span data-ttu-id="7decc-470">1900 - 194F</span><span class="sxs-lookup"><span data-stu-id="7decc-470">1900 - 194F</span></span></td>
<td><span data-ttu-id="7decc-471">Лимбу</span><span class="sxs-lookup"><span data-stu-id="7decc-471">Limbu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-472">94</span><span class="sxs-lookup"><span data-stu-id="7decc-472">94</span></span></td>
<td><span data-ttu-id="7decc-473">1950 - 197F</span><span class="sxs-lookup"><span data-stu-id="7decc-473">1950 - 197F</span></span></td>
<td><span data-ttu-id="7decc-474">Тай Le</span><span class="sxs-lookup"><span data-stu-id="7decc-474">Tai Le</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-475">95</span><span class="sxs-lookup"><span data-stu-id="7decc-475">95</span></span></td>
<td><span data-ttu-id="7decc-476">1980-19DF</span><span class="sxs-lookup"><span data-stu-id="7decc-476">1980 - 19DF</span></span></td>
<td><span data-ttu-id="7decc-477">Новая письменность тай-лю</span><span class="sxs-lookup"><span data-stu-id="7decc-477">New Tai Lue</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-478">96</span><span class="sxs-lookup"><span data-stu-id="7decc-478">96</span></span></td>
<td><span data-ttu-id="7decc-479">1A00 - 1A1F</span><span class="sxs-lookup"><span data-stu-id="7decc-479">1A00 - 1A1F</span></span></td>
<td><span data-ttu-id="7decc-480">Бугийский</span><span class="sxs-lookup"><span data-stu-id="7decc-480">Buginese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-481">97</span><span class="sxs-lookup"><span data-stu-id="7decc-481">97</span></span></td>
<td><span data-ttu-id="7decc-482">2C00 - 2C5F</span><span class="sxs-lookup"><span data-stu-id="7decc-482">2C00 - 2C5F</span></span></td>
<td><span data-ttu-id="7decc-483">глаголитик</span><span class="sxs-lookup"><span data-stu-id="7decc-483">Glagolitic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-484">98</span><span class="sxs-lookup"><span data-stu-id="7decc-484">98</span></span></td>
<td><span data-ttu-id="7decc-485">2D30 - 2D7F</span><span class="sxs-lookup"><span data-stu-id="7decc-485">2D30 - 2D7F</span></span></td>
<td><span data-ttu-id="7decc-486">Тифинаг</span><span class="sxs-lookup"><span data-stu-id="7decc-486">Tifinagh</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-487">99</span><span class="sxs-lookup"><span data-stu-id="7decc-487">99</span></span></td>
<td><span data-ttu-id="7decc-488">4DC0 - 4DFF</span><span class="sxs-lookup"><span data-stu-id="7decc-488">4DC0 - 4DFF</span></span></td>
<td><span data-ttu-id="7decc-489">Символы ижинг Цзин</span><span class="sxs-lookup"><span data-stu-id="7decc-489">Yijing Hexagram Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-490">100</span><span class="sxs-lookup"><span data-stu-id="7decc-490">100</span></span></td>
<td><span data-ttu-id="7decc-491">A800 - A82F</span><span class="sxs-lookup"><span data-stu-id="7decc-491">A800 - A82F</span></span></td>
<td><span data-ttu-id="7decc-492">Силоти нагри</span><span class="sxs-lookup"><span data-stu-id="7decc-492">Syloti Nagri</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="7decc-493">101 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-493">101${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-494">10000-1007F</span><span class="sxs-lookup"><span data-stu-id="7decc-494">10000 - 1007F</span></span></td>
<td><span data-ttu-id="7decc-495">Линейная B — слоговая</span><span class="sxs-lookup"><span data-stu-id="7decc-495">Linear B Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-496">10080-100FF</span><span class="sxs-lookup"><span data-stu-id="7decc-496">10080 - 100FF</span></span></td>
<td><span data-ttu-id="7decc-497">Линейная B Идеограмс</span><span class="sxs-lookup"><span data-stu-id="7decc-497">Linear B Ideograms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-498">10100-1013F</span><span class="sxs-lookup"><span data-stu-id="7decc-498">10100 - 1013F</span></span></td>
<td><span data-ttu-id="7decc-499">Эгейский университет числа</span><span class="sxs-lookup"><span data-stu-id="7decc-499">Aegean Numbers</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-500">102</span><span class="sxs-lookup"><span data-stu-id="7decc-500">102</span></span></td>
<td><span data-ttu-id="7decc-501">10140-1018F</span><span class="sxs-lookup"><span data-stu-id="7decc-501">10140 - 1018F</span></span></td>
<td><span data-ttu-id="7decc-502">Античного Греческий номер</span><span class="sxs-lookup"><span data-stu-id="7decc-502">Ancient Greek Numbers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-503">103</span><span class="sxs-lookup"><span data-stu-id="7decc-503">103</span></span></td>
<td><span data-ttu-id="7decc-504">10380-1039F</span><span class="sxs-lookup"><span data-stu-id="7decc-504">10380 - 1039F</span></span></td>
<td><span data-ttu-id="7decc-505">Угаритский</span><span class="sxs-lookup"><span data-stu-id="7decc-505">Ugaritic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-506">104</span><span class="sxs-lookup"><span data-stu-id="7decc-506">104</span></span></td>
<td><span data-ttu-id="7decc-507">103A0 - 103DF</span><span class="sxs-lookup"><span data-stu-id="7decc-507">103A0 - 103DF</span></span></td>
<td><span data-ttu-id="7decc-508">Старый Персидский</span><span class="sxs-lookup"><span data-stu-id="7decc-508">Old Persian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-509">105</span><span class="sxs-lookup"><span data-stu-id="7decc-509">105</span></span></td>
<td><span data-ttu-id="7decc-510">10450-1047F</span><span class="sxs-lookup"><span data-stu-id="7decc-510">10450 - 1047F</span></span></td>
<td><span data-ttu-id="7decc-511">шавиан</span><span class="sxs-lookup"><span data-stu-id="7decc-511">Shavian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-512">106</span><span class="sxs-lookup"><span data-stu-id="7decc-512">106</span></span></td>
<td><span data-ttu-id="7decc-513">10480-104AF</span><span class="sxs-lookup"><span data-stu-id="7decc-513">10480 - 104AF</span></span></td>
<td><span data-ttu-id="7decc-514">османя</span><span class="sxs-lookup"><span data-stu-id="7decc-514">Osmanya</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-515">107</span><span class="sxs-lookup"><span data-stu-id="7decc-515">107</span></span></td>
<td><span data-ttu-id="7decc-516">10800-1083F</span><span class="sxs-lookup"><span data-stu-id="7decc-516">10800 - 1083F</span></span></td>
<td><span data-ttu-id="7decc-517">Циприотская слоговая</span><span class="sxs-lookup"><span data-stu-id="7decc-517">Cypriot Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-518">108</span><span class="sxs-lookup"><span data-stu-id="7decc-518">108</span></span></td>
<td><span data-ttu-id="7decc-519">10A00 - 10A5F</span><span class="sxs-lookup"><span data-stu-id="7decc-519">10A00 - 10A5F</span></span></td>
<td><span data-ttu-id="7decc-520">кхарошси</span><span class="sxs-lookup"><span data-stu-id="7decc-520">Kharoshthi</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-521">109</span><span class="sxs-lookup"><span data-stu-id="7decc-521">109</span></span></td>
<td><span data-ttu-id="7decc-522">1D300 - 1D35F</span><span class="sxs-lookup"><span data-stu-id="7decc-522">1D300 - 1D35F</span></span></td>
<td><span data-ttu-id="7decc-523">Символы Тай Ксуан Цзин Чань</span><span class="sxs-lookup"><span data-stu-id="7decc-523">Tai Xuan Jing Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7decc-524">110 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-524">110${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-525">12000-123FF</span><span class="sxs-lookup"><span data-stu-id="7decc-525">12000 - 123FF</span></span></td>
<td><span data-ttu-id="7decc-526">кунеиформ</span><span class="sxs-lookup"><span data-stu-id="7decc-526">Cuneiform</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-527">12400-1247F</span><span class="sxs-lookup"><span data-stu-id="7decc-527">12400 - 1247F</span></span></td>
<td><span data-ttu-id="7decc-528">Кунеиформ цифры и пунктуация</span><span class="sxs-lookup"><span data-stu-id="7decc-528">Cuneiform Numbers and Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-529">111</span><span class="sxs-lookup"><span data-stu-id="7decc-529">111</span></span></td>
<td><span data-ttu-id="7decc-530">1D360 - 1D37F</span><span class="sxs-lookup"><span data-stu-id="7decc-530">1D360 - 1D37F</span></span></td>
<td><span data-ttu-id="7decc-531">Подсчет чисел</span><span class="sxs-lookup"><span data-stu-id="7decc-531">Counting Rod Numerals</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-532">112</span><span class="sxs-lookup"><span data-stu-id="7decc-532">112</span></span></td>
<td><span data-ttu-id="7decc-533">1B80 - 1BBF</span><span class="sxs-lookup"><span data-stu-id="7decc-533">1B80 - 1BBF</span></span></td>
<td><span data-ttu-id="7decc-534">Сунданская письменность</span><span class="sxs-lookup"><span data-stu-id="7decc-534">Sundanese</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-535">113</span><span class="sxs-lookup"><span data-stu-id="7decc-535">113</span></span></td>
<td><span data-ttu-id="7decc-536">1C00 - 1C4F</span><span class="sxs-lookup"><span data-stu-id="7decc-536">1C00 - 1C4F</span></span></td>
<td><span data-ttu-id="7decc-537">Лепча</span><span class="sxs-lookup"><span data-stu-id="7decc-537">Lepcha</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-538">114</span><span class="sxs-lookup"><span data-stu-id="7decc-538">114</span></span></td>
<td><span data-ttu-id="7decc-539">1C50 - 1C7F</span><span class="sxs-lookup"><span data-stu-id="7decc-539">1C50 - 1C7F</span></span></td>
<td><span data-ttu-id="7decc-540">Письменность ол-чики</span><span class="sxs-lookup"><span data-stu-id="7decc-540">Ol Chiki</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-541">115</span><span class="sxs-lookup"><span data-stu-id="7decc-541">115</span></span></td>
<td><span data-ttu-id="7decc-542">A880 - A8DF</span><span class="sxs-lookup"><span data-stu-id="7decc-542">A880 - A8DF</span></span></td>
<td><span data-ttu-id="7decc-543">Саураштра</span><span class="sxs-lookup"><span data-stu-id="7decc-543">Saurashtra</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-544">116</span><span class="sxs-lookup"><span data-stu-id="7decc-544">116</span></span></td>
<td><span data-ttu-id="7decc-545">A900 - A92F</span><span class="sxs-lookup"><span data-stu-id="7decc-545">A900 - A92F</span></span></td>
<td><span data-ttu-id="7decc-546">Письменность кайях-ли</span><span class="sxs-lookup"><span data-stu-id="7decc-546">Kayah Li</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-547">117</span><span class="sxs-lookup"><span data-stu-id="7decc-547">117</span></span></td>
<td><span data-ttu-id="7decc-548">A930 - A95F</span><span class="sxs-lookup"><span data-stu-id="7decc-548">A930 - A95F</span></span></td>
<td><span data-ttu-id="7decc-549">Реджангский</span><span class="sxs-lookup"><span data-stu-id="7decc-549">Rejang</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-550">118</span><span class="sxs-lookup"><span data-stu-id="7decc-550">118</span></span></td>
<td><span data-ttu-id="7decc-551">AA00 - AA5F</span><span class="sxs-lookup"><span data-stu-id="7decc-551">AA00 - AA5F</span></span></td>
<td><span data-ttu-id="7decc-552">Чамская письменность</span><span class="sxs-lookup"><span data-stu-id="7decc-552">Cham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-553">119</span><span class="sxs-lookup"><span data-stu-id="7decc-553">119</span></span></td>
<td><span data-ttu-id="7decc-554">10190-101CF</span><span class="sxs-lookup"><span data-stu-id="7decc-554">10190 - 101CF</span></span></td>
<td><span data-ttu-id="7decc-555">Античного символы</span><span class="sxs-lookup"><span data-stu-id="7decc-555">Ancient Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-556">120</span><span class="sxs-lookup"><span data-stu-id="7decc-556">120</span></span></td>
<td><span data-ttu-id="7decc-557">101D0 - 101FF</span><span class="sxs-lookup"><span data-stu-id="7decc-557">101D0 - 101FF</span></span></td>
<td><span data-ttu-id="7decc-558">Фаистос диск</span><span class="sxs-lookup"><span data-stu-id="7decc-558">Phaistos Disc</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="7decc-559">121 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-559">121${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-560">10280-1029F</span><span class="sxs-lookup"><span data-stu-id="7decc-560">10280 - 1029F</span></span></td>
<td><span data-ttu-id="7decc-561">Ликийский</span><span class="sxs-lookup"><span data-stu-id="7decc-561">Lycian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-562">102A0 - 102DF</span><span class="sxs-lookup"><span data-stu-id="7decc-562">102A0 - 102DF</span></span></td>
<td><span data-ttu-id="7decc-563">Карийский</span><span class="sxs-lookup"><span data-stu-id="7decc-563">Carian</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-564">10920-1093F</span><span class="sxs-lookup"><span data-stu-id="7decc-564">10920 - 1093F</span></span></td>
<td><span data-ttu-id="7decc-565">Лидийский</span><span class="sxs-lookup"><span data-stu-id="7decc-565">Lydian</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="7decc-566">122 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7decc-566">122${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7decc-567">1F000 - 1F02F</span><span class="sxs-lookup"><span data-stu-id="7decc-567">1F000 - 1F02F</span></span></td>
<td><span data-ttu-id="7decc-568">Плитки в маджонг</span><span class="sxs-lookup"><span data-stu-id="7decc-568">Mahjong Tiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-569">1F030 - 1F09F</span><span class="sxs-lookup"><span data-stu-id="7decc-569">1F030 - 1F09F</span></span></td>
<td><span data-ttu-id="7decc-570">Плитки Domino</span><span class="sxs-lookup"><span data-stu-id="7decc-570">Domino Tiles</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7decc-571">123</span><span class="sxs-lookup"><span data-stu-id="7decc-571">123</span></span></td>

<td><span data-ttu-id="7decc-572"><strong>Windows 2000 и более поздние версии:</strong> Ход выполнения макета, горизонтальный справа налево</span><span class="sxs-lookup"><span data-stu-id="7decc-572"><strong>Windows 2000 and later:</strong> Layout progress, horizontal from right to left</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-573">124</span><span class="sxs-lookup"><span data-stu-id="7decc-573">124</span></span></td>

<td><span data-ttu-id="7decc-574"><strong>Windows 2000 и более поздние версии:</strong> Ход выполнения макета, по вертикали перед горизонтальным</span><span class="sxs-lookup"><span data-stu-id="7decc-574"><strong>Windows 2000 and later:</strong> Layout progress, vertical before horizontal</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7decc-575">125</span><span class="sxs-lookup"><span data-stu-id="7decc-575">125</span></span></td>

<td><span data-ttu-id="7decc-576"><strong>Windows 2000 и более поздние версии:</strong> Ход выполнения макета, Вертикальный снизу вверх</span><span class="sxs-lookup"><span data-stu-id="7decc-576"><strong>Windows 2000 and later:</strong> Layout progress, vertical bottom to top</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7decc-577">126-127</span><span class="sxs-lookup"><span data-stu-id="7decc-577">126-127</span></span></td>

<td><span data-ttu-id="7decc-578">Зарезервировано для внутреннего использования процессом</span><span class="sxs-lookup"><span data-stu-id="7decc-578">Reserved for process-internal usage</span></span></td>
</tr>
</tbody>
</table>



 

 

 



