---
description: 'Подробнее: информационные параметры'
title: Информационные параметры
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811140"
---
# <a name="informational-parameters"></a><span data-ttu-id="c0b3f-103">Информационные параметры</span><span class="sxs-lookup"><span data-stu-id="c0b3f-103">Informational Parameters</span></span>


<span data-ttu-id="c0b3f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c0b3f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="informational-parameters"></a><span data-ttu-id="c0b3f-105">Информационные параметры</span><span class="sxs-lookup"><span data-stu-id="c0b3f-105">Informational Parameters</span></span>

<span data-ttu-id="c0b3f-106">Этот раздел содержит параметры, используемые для предоставления сведений о ядре СУБД.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-106">This topic contains parameters that are used to expose information about the database engine.</span></span>

<span data-ttu-id="c0b3f-107">*JET_paramKeyMost*</span><span class="sxs-lookup"><span data-stu-id="c0b3f-107">*JET_paramKeyMost*</span></span>  
<span data-ttu-id="c0b3f-108">134</span><span class="sxs-lookup"><span data-stu-id="c0b3f-108">134</span></span>  

<span data-ttu-id="c0b3f-109">Этот параметр только для чтения указывает максимальную допустимую длину ключа индекса, которую можно выбрать для текущего размера страницы базы данных (согласно настройкам JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="c0b3f-109">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by JET_paramDatabasePageSize).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-110">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-110">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-111">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="c0b3f-111">JET_cbKeyMost4KBytePage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-112">Тип:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-112">Type:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-113">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c0b3f-113">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-114">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-114">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-115">255 – 65535</span><span class="sxs-lookup"><span data-stu-id="c0b3f-115">255 – 65535</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-116">Область.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-116">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-117">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c0b3f-117">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-118">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-118">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-119">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c0b3f-119">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-120">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-120">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-121">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c0b3f-121">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-122">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-122">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-123">Нет</span><span class="sxs-lookup"><span data-stu-id="c0b3f-123">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-124">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-124">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-125">Нет</span><span class="sxs-lookup"><span data-stu-id="c0b3f-125">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-126">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-126">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-127">Нет</span><span class="sxs-lookup"><span data-stu-id="c0b3f-127">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-128">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-128">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-129">Нет</span><span class="sxs-lookup"><span data-stu-id="c0b3f-129">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-130">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c0b3f-130">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-131">Начиная с Windows Server 2008 и Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0b3f-131">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c0b3f-132">*JET_paramMaxColtyp*</span><span class="sxs-lookup"><span data-stu-id="c0b3f-132">*JET_paramMaxColtyp*</span></span>  
<span data-ttu-id="c0b3f-133">131</span><span class="sxs-lookup"><span data-stu-id="c0b3f-133">131</span></span>  

<span data-ttu-id="c0b3f-134">Этот параметр только для чтения возвращает максимальное [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) для этой версии ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-134">This read only parameter returns the maximum [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) for that version of the database engine.</span></span> <span data-ttu-id="c0b3f-135">Это значение можно использовать для проверки поддержки определенного [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="c0b3f-135">This value can be used to test for support of a specific [JET_COLTYP](./jet-coltyp.md).</span></span> <span data-ttu-id="c0b3f-136">Если данный параметр [JET_COLTYP](./jet-coltyp.md) меньше значения этого параметра, он поддерживается ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-136">If a given [JET_COLTYP](./jet-coltyp.md) is less than the value of this parameter then it is supported by the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-137">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-138">JET_coltypUnsignedShort + 1</span><span class="sxs-lookup"><span data-stu-id="c0b3f-138">JET_coltypUnsignedShort + 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-139">Тип:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-140">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c0b3f-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-141">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-142">0 – 255</span><span class="sxs-lookup"><span data-stu-id="c0b3f-142">0 – 255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-143">Область.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-144">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c0b3f-144">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-145">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-146">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c0b3f-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-147">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-148">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c0b3f-148">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-149">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-150">Нет</span><span class="sxs-lookup"><span data-stu-id="c0b3f-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-151">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-152">Нет</span><span class="sxs-lookup"><span data-stu-id="c0b3f-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-153">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-154">Нет</span><span class="sxs-lookup"><span data-stu-id="c0b3f-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-155">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-156">Нет</span><span class="sxs-lookup"><span data-stu-id="c0b3f-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-157">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c0b3f-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-158">Начиная с Windows Server 2008 и Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0b3f-158">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c0b3f-159">*JET_paramLVChunkSizeMost*</span><span class="sxs-lookup"><span data-stu-id="c0b3f-159">*JET_paramLVChunkSizeMost*</span></span>  
<span data-ttu-id="c0b3f-160">163</span><span class="sxs-lookup"><span data-stu-id="c0b3f-160">163</span></span>  

<span data-ttu-id="c0b3f-161">Параметр только для чтения, возвращающий размер фрагмента длинных значений на основе настроенного размера страницы.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-161">Read only parameter that returns the long-value chunk size based on configured page size.</span></span> <span data-ttu-id="c0b3f-162">Если длинное значение должно быть считано или записано несколькими вызовами Jet {Set, reby}, то использование буфера с размером, кратным размеру блока, является более эффективным.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-162">If a long-value is to be read or written with multiple Jet{Set,Retrieve}Column calls then using a buffer whose size is a multiple of the chunk size is more efficient.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-163">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-163">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-164">2 КБ страница = 1966 байт</span><span class="sxs-lookup"><span data-stu-id="c0b3f-164">2kb page = 1966 bytes</span></span><br />
<span data-ttu-id="c0b3f-165">4 КБ страница = 4014 байт</span><span class="sxs-lookup"><span data-stu-id="c0b3f-165">4kb page = 4014 bytes</span></span><br />
<span data-ttu-id="c0b3f-166">8 КБ страница = 8110 байт</span><span class="sxs-lookup"><span data-stu-id="c0b3f-166">8kb page = 8110 bytes</span></span><br />
<span data-ttu-id="c0b3f-167">16 КБ страница = 4050 байт</span><span class="sxs-lookup"><span data-stu-id="c0b3f-167">16kb page = 4050 bytes</span></span><br />
<span data-ttu-id="c0b3f-168">32 КБ страница = 8150 байт</span><span class="sxs-lookup"><span data-stu-id="c0b3f-168">32kb page = 8150 bytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-169">Тип:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-170">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c0b3f-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-171">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c0b3f-172">0-10000</span><span class="sxs-lookup"><span data-stu-id="c0b3f-172">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-173">Область.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-173">Scope:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-174">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-175">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-175">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-176">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-176">Affects Physical Layout:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-177">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-177">Affects Reliability:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-178">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-178">Affects Performance:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-179">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-179">Affects Resources:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-180">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c0b3f-180">Availability:</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="c0b3f-181">Требования</span><span class="sxs-lookup"><span data-stu-id="c0b3f-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-182"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c0b3f-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c0b3f-183">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-183">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b3f-184"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c0b3f-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c0b3f-185">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-185">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b3f-186"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c0b3f-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c0b3f-187">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c0b3f-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c0b3f-188">См. также:</span><span class="sxs-lookup"><span data-stu-id="c0b3f-188">See Also</span></span>

[<span data-ttu-id="c0b3f-189">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="c0b3f-189">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c0b3f-190">жетинит</span><span class="sxs-lookup"><span data-stu-id="c0b3f-190">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="c0b3f-191">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="c0b3f-191">JET_COLTYP</span></span>](./jet-coltyp.md)
