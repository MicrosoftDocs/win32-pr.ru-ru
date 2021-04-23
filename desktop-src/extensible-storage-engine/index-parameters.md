---
description: 'Дополнительные сведения: параметры индекса'
title: Параметры индекса
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081548"
---
# <a name="index-parameters"></a><span data-ttu-id="416c2-103">Параметры индекса</span><span class="sxs-lookup"><span data-stu-id="416c2-103">Index Parameters</span></span>


<span data-ttu-id="416c2-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="416c2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="index-parameters"></a><span data-ttu-id="416c2-105">Параметры индекса</span><span class="sxs-lookup"><span data-stu-id="416c2-105">Index Parameters</span></span>

<span data-ttu-id="416c2-106">Этот раздел содержит параметры, используемые для индекса.</span><span class="sxs-lookup"><span data-stu-id="416c2-106">This topic contains parameters that are used for the index.</span></span>

<span data-ttu-id="416c2-107">*JET_paramIndexTupleIncrement*</span><span class="sxs-lookup"><span data-stu-id="416c2-107">*JET_paramIndexTupleIncrement*</span></span>  
<span data-ttu-id="416c2-108">132</span><span class="sxs-lookup"><span data-stu-id="416c2-108">132</span></span>  

<span data-ttu-id="416c2-109">Этот параметр задает значение по умолчанию для шага смещения, используемого для пошагового перехода к значению исходного столбца при создании каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="416c2-109">This parameter specifies the default for the offset increment used to step through the source column value while generating each tuple.</span></span> <span data-ttu-id="416c2-110">Дополнительные сведения см. в разделе Структура [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="416c2-110">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="416c2-111">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="416c2-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="416c2-112">1</span><span class="sxs-lookup"><span data-stu-id="416c2-112">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="416c2-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="416c2-114">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="416c2-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-115">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="416c2-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="416c2-116">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="416c2-116">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-117">Область.</span><span class="sxs-lookup"><span data-stu-id="416c2-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="416c2-118">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="416c2-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-119">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-120">Да</span><span class="sxs-lookup"><span data-stu-id="416c2-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-121">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-122">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-123">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="416c2-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="416c2-124">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-125">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="416c2-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-126">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-127">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="416c2-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="416c2-128">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-129">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="416c2-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="416c2-130">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-131">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="416c2-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-132">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="416c2-132">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="416c2-133">*JET_paramIndexTupleStart*</span><span class="sxs-lookup"><span data-stu-id="416c2-133">*JET_paramIndexTupleStart*</span></span>  
<span data-ttu-id="416c2-134">133</span><span class="sxs-lookup"><span data-stu-id="416c2-134">133</span></span>  

<span data-ttu-id="416c2-135">Этот параметр задает значение по умолчанию для смещения в значении исходного столбца, с которого начнется создание кортежей.</span><span class="sxs-lookup"><span data-stu-id="416c2-135">This parameter specifies the default for the offset in the source column value at which tuple generation will start.</span></span> <span data-ttu-id="416c2-136">Дополнительные сведения см. в разделе Структура [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="416c2-136">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="416c2-137">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="416c2-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="416c2-138">0</span><span class="sxs-lookup"><span data-stu-id="416c2-138">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-139">Тип:</span><span class="sxs-lookup"><span data-stu-id="416c2-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="416c2-140">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="416c2-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-141">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="416c2-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="416c2-142">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="416c2-142">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-143">Область.</span><span class="sxs-lookup"><span data-stu-id="416c2-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="416c2-144">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="416c2-144">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-145">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-146">Да</span><span class="sxs-lookup"><span data-stu-id="416c2-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-147">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-148">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-148">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-149">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="416c2-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="416c2-150">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-151">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="416c2-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-152">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-153">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="416c2-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="416c2-154">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-155">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="416c2-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="416c2-156">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-157">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="416c2-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-158">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="416c2-158">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="416c2-159">*JET_paramIndexTuplesLengthMax*</span><span class="sxs-lookup"><span data-stu-id="416c2-159">*JET_paramIndexTuplesLengthMax*</span></span>  
<span data-ttu-id="416c2-160">111</span><span class="sxs-lookup"><span data-stu-id="416c2-160">111</span></span>  

<span data-ttu-id="416c2-161">Этот параметр задает значение по умолчанию для максимальной длины кортежа в индексе кортежа.</span><span class="sxs-lookup"><span data-stu-id="416c2-161">This parameter specifies the default for the maximum tuple length in a tuple index.</span></span> <span data-ttu-id="416c2-162">Дополнительные сведения см. в разделе Структура [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="416c2-162">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<span data-ttu-id="416c2-163">**Windows Vista:**  До выхода Windows Vista установка этого параметра в нулевое значение применяет его к значению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="416c2-163">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="416c2-164">Для Windows Vista это больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="416c2-164">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="416c2-165">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="416c2-165">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="416c2-166">10</span><span class="sxs-lookup"><span data-stu-id="416c2-166">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-167">Тип:</span><span class="sxs-lookup"><span data-stu-id="416c2-167">Type:</span></span></p></td>
<td><p><span data-ttu-id="416c2-168">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="416c2-168">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-169">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="416c2-169">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="416c2-170"><strong>Windows 2000, Windows XP и Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="416c2-170"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="416c2-171"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="416c2-171"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-172">Область.</span><span class="sxs-lookup"><span data-stu-id="416c2-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="416c2-173">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="416c2-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-174">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-175">Да</span><span class="sxs-lookup"><span data-stu-id="416c2-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-176">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-177">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-178">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="416c2-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="416c2-179">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-180">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="416c2-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-181">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-182">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="416c2-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="416c2-183">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-183">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-184">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="416c2-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="416c2-185">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-185">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-186">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="416c2-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-187">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="416c2-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="416c2-188">*JET_paramIndexTuplesLengthMin*</span><span class="sxs-lookup"><span data-stu-id="416c2-188">*JET_paramIndexTuplesLengthMin*</span></span>  
<span data-ttu-id="416c2-189">110</span><span class="sxs-lookup"><span data-stu-id="416c2-189">110</span></span>  

<span data-ttu-id="416c2-190">Этот параметр задает значение по умолчанию для минимальной длины кортежа в индексе кортежа.</span><span class="sxs-lookup"><span data-stu-id="416c2-190">This parameter specifies the default for the minimum tuple length in a tuple index.</span></span> <span data-ttu-id="416c2-191">Дополнительные сведения см. в разделе [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="416c2-191">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="416c2-192">**Windows Vista:**  До выхода Windows Vista установка этого параметра в нулевое значение применяет его к значению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="416c2-192">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="416c2-193">Для Windows Vista это больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="416c2-193">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="416c2-194">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="416c2-194">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="416c2-195">3</span><span class="sxs-lookup"><span data-stu-id="416c2-195">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-196">Тип:</span><span class="sxs-lookup"><span data-stu-id="416c2-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="416c2-197">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="416c2-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-198">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="416c2-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="416c2-199"><strong>Windows 2000, Windows XP и Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="416c2-199"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="416c2-200"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="416c2-200"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-201">Область.</span><span class="sxs-lookup"><span data-stu-id="416c2-201">Scope:</span></span></p></td>
<td><p><span data-ttu-id="416c2-202">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="416c2-202">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-203">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-203">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-204">Да</span><span class="sxs-lookup"><span data-stu-id="416c2-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-205">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-205">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-206">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-206">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-207">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="416c2-207">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="416c2-208">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-209">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="416c2-209">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-210">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-210">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-211">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="416c2-211">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="416c2-212">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-212">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-213">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="416c2-213">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="416c2-214">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-215">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="416c2-215">Availability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-216">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="416c2-216">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="416c2-217">*JET_paramIndexTuplesToIndexMax*</span><span class="sxs-lookup"><span data-stu-id="416c2-217">*JET_paramIndexTuplesToIndexMax*</span></span>  
<span data-ttu-id="416c2-218">112</span><span class="sxs-lookup"><span data-stu-id="416c2-218">112</span></span>  

<span data-ttu-id="416c2-219">Этот параметр задает значение по умолчанию для максимальной длины исходной строки, которая должна быть разбита на кортежи для индекса кортежа.</span><span class="sxs-lookup"><span data-stu-id="416c2-219">This parameter specifies the default for the maximum length of a source string to break into tuples for a tuple index.</span></span> <span data-ttu-id="416c2-220">Дополнительные сведения см. в разделе [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="416c2-220">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="416c2-221">**Windows Vista:**  До выхода Windows Vista установка этого параметра в нулевое значение применяет его к значению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="416c2-221">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="416c2-222">Для Windows Vista это больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="416c2-222">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="416c2-223">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="416c2-223">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="416c2-224">32767</span><span class="sxs-lookup"><span data-stu-id="416c2-224">32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-225">Тип:</span><span class="sxs-lookup"><span data-stu-id="416c2-225">Type:</span></span></p></td>
<td><p><span data-ttu-id="416c2-226">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="416c2-226">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-227">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="416c2-227">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="416c2-228"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  0 – 32767</span><span class="sxs-lookup"><span data-stu-id="416c2-228"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 32767</span></span></p>
<p><span data-ttu-id="416c2-229"><strong>Windows Vista:</strong>  1 – 32767</span><span class="sxs-lookup"><span data-stu-id="416c2-229"><strong>Windows Vista:</strong>  1 – 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-230">Область.</span><span class="sxs-lookup"><span data-stu-id="416c2-230">Scope:</span></span></p></td>
<td><p><span data-ttu-id="416c2-231">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="416c2-231">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-232">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-232">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-233">Да</span><span class="sxs-lookup"><span data-stu-id="416c2-233">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-234">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-234">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-235">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-235">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-236">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="416c2-236">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="416c2-237">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-237">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-238">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="416c2-238">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-239">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-239">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-240">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="416c2-240">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="416c2-241">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-241">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-242">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="416c2-242">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="416c2-243">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-243">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-244">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="416c2-244">Availability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-245">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="416c2-245">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="416c2-246">*JET_paramUnicodeIndexDefault*</span><span class="sxs-lookup"><span data-stu-id="416c2-246">*JET_paramUnicodeIndexDefault*</span></span>  
<span data-ttu-id="416c2-247">72</span><span class="sxs-lookup"><span data-stu-id="416c2-247">72</span></span>  

<span data-ttu-id="416c2-248">Этот параметр управляет параметрами Юникода по умолчанию, используемыми любым индексом для ключевого столбца Юникода.</span><span class="sxs-lookup"><span data-stu-id="416c2-248">This parameter controls the default Unicode parameters used by any index over a Unicode key column.</span></span> <span data-ttu-id="416c2-249">Тип этого параметра — [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) и фактически передается с помощью указателя буфера, хранящегося в целочисленном параметре [жетжетсистемпараметер](./jetgetsystemparameter-function.md) и [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="416c2-249">The type of this parameter is [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and is actually passed using a buffer pointer stored in the integer parameter of [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="416c2-250">Размер буфера должен равняться размеру [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) и должен передаваться в [жетжетсистемпараметер](./jetgetsystemparameter-function.md) с помощью параметра размера буфера строки.</span><span class="sxs-lookup"><span data-stu-id="416c2-250">The size of the buffer must equal the size of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and must be passed to [JetGetSystemParameter](./jetgetsystemparameter-function.md) using the string buffer size parameter.</span></span> <span data-ttu-id="416c2-251">Это явное несоответствие, но это поведение этого параметра.</span><span class="sxs-lookup"><span data-stu-id="416c2-251">This is clearly inconsistent but that is the behavior of this parameter.</span></span>

<span data-ttu-id="416c2-252">Значение этого параметра по умолчанию содержит код языка для английского языка (США) и следующие флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa): LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="416c2-252">The default value of this parameter contains an LCID for the U.S. English locale and the following [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="416c2-253">**Windows 2000:**  СОРТИД в LCID игнорируется.</span><span class="sxs-lookup"><span data-stu-id="416c2-253">**Windows 2000:**  The SORTID in the LCID is ignored.</span></span> <span data-ttu-id="416c2-254">Всегда используется СОРТИД SORT_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="416c2-254">A SORTID of SORT_DEFAULT is always used.</span></span>

<span data-ttu-id="416c2-255">**Windows 2000:**  Флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa) должны содержать следующие флаги: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="416c2-255">**Windows 2000:**  The [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) flags must contain the following flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="416c2-256">Кроме того, флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa)могут содержать следующие флаги: NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="416c2-256">In addition, the [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags may contain the following flags: NORM_IGNORENONSPACE.</span></span>

<span data-ttu-id="416c2-257">**Примечание**  .  Если приложению требуется хранить данные в Юникоде, настоятельно рекомендуется не полагаться на параметры Юникода по умолчанию для индексов.</span><span class="sxs-lookup"><span data-stu-id="416c2-257">**Note**  If your application wishes to store Unicode data, then it is strongly recommended that you do not rely on the default Unicode parameters for your indexes.</span></span> <span data-ttu-id="416c2-258">Использование языка "Английский (США)" — запереть использования инвариантного языкового стандарта, и флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa)по умолчанию могут серьезно мешать работе некоторых языков.</span><span class="sxs-lookup"><span data-stu-id="416c2-258">The use of U.S. English is tantamount to using the invariant locale and the default [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags are known to seriously interfere with some languages.</span></span> <span data-ttu-id="416c2-259">Необходимо всегда указывать собственные параметры для параметров Юникода в JetCreateIndex2 с помощью [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="416c2-259">You should always specify your own settings for the Unicode parameters to JetCreateIndex2 using [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="416c2-260">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="416c2-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="416c2-261">Специальные функции</span><span class="sxs-lookup"><span data-stu-id="416c2-261">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-262">Тип:</span><span class="sxs-lookup"><span data-stu-id="416c2-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="416c2-263">JET_UNICODEINDEX \* (JET_UNICODEINDEX)</span><span class="sxs-lookup"><span data-stu-id="416c2-263">JET_UNICODEINDEX\* (JET_UNICODEINDEX)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-264">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="416c2-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="416c2-265">Специальные функции</span><span class="sxs-lookup"><span data-stu-id="416c2-265">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-266">Область.</span><span class="sxs-lookup"><span data-stu-id="416c2-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="416c2-267">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="416c2-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-268">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-269">Да</span><span class="sxs-lookup"><span data-stu-id="416c2-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-270">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="416c2-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="416c2-271">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-272">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="416c2-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="416c2-273">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-273">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-274">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="416c2-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-275">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-276">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="416c2-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="416c2-277">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-278">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="416c2-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="416c2-279">Нет</span><span class="sxs-lookup"><span data-stu-id="416c2-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-280">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="416c2-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="416c2-281">Все</span><span class="sxs-lookup"><span data-stu-id="416c2-281">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="416c2-282">Требования</span><span class="sxs-lookup"><span data-stu-id="416c2-282">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="416c2-283"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="416c2-283"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="416c2-284">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="416c2-284">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="416c2-285"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="416c2-285"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="416c2-286">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="416c2-286">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="416c2-287"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="416c2-287"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="416c2-288">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="416c2-288">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="416c2-289">См. также:</span><span class="sxs-lookup"><span data-stu-id="416c2-289">See Also</span></span>

[<span data-ttu-id="416c2-290">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="416c2-290">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="416c2-291">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="416c2-291">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="416c2-292">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="416c2-292">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="416c2-293">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="416c2-293">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="416c2-294">жетжетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="416c2-294">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="416c2-295">жетинит</span><span class="sxs-lookup"><span data-stu-id="416c2-295">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="416c2-296">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="416c2-296">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
