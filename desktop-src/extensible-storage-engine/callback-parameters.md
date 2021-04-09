---
description: 'Дополнительные сведения: параметры обратного вызова'
title: Параметры обратного вызова
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
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
ms.openlocfilehash: 4e06ed65bbeae195060e4de10424a76a4228f20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155058"
---
# <a name="callback-parameters"></a><span data-ttu-id="3f002-103">Параметры обратного вызова</span><span class="sxs-lookup"><span data-stu-id="3f002-103">Callback Parameters</span></span>


<span data-ttu-id="3f002-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3f002-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="callback-parameters"></a><span data-ttu-id="3f002-105">Параметры обратного вызова</span><span class="sxs-lookup"><span data-stu-id="3f002-105">Callback Parameters</span></span>

<span data-ttu-id="3f002-106">Этот раздел содержит параметры, используемые для обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="3f002-106">This topic contains parameters that are used for callbacks.</span></span>

<span data-ttu-id="3f002-107">*JET_paramDisableCallbacks*</span><span class="sxs-lookup"><span data-stu-id="3f002-107">*JET_paramDisableCallbacks*</span></span>  
<span data-ttu-id="3f002-108">65</span><span class="sxs-lookup"><span data-stu-id="3f002-108">65</span></span>  

<span data-ttu-id="3f002-109">Этот параметр отключает все обратные вызовы ядра СУБД к функциям, предоставляемым приложением.</span><span class="sxs-lookup"><span data-stu-id="3f002-109">This parameter disables all database engine callbacks to application provided functions.</span></span> <span data-ttu-id="3f002-110">В основном она предназначена для поддержки служебных программ ядра СУБД и не предназначена для использования в приложении.</span><span class="sxs-lookup"><span data-stu-id="3f002-110">It is primarily intended to support the database engine utilities and is not intended to be used in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f002-111">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="3f002-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3f002-112">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f002-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="3f002-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="3f002-114">Логическое</span><span class="sxs-lookup"><span data-stu-id="3f002-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-115">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="3f002-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3f002-116">False, true</span><span class="sxs-lookup"><span data-stu-id="3f002-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-117">Область.</span><span class="sxs-lookup"><span data-stu-id="3f002-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3f002-118">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="3f002-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-119">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="3f002-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3f002-120">Да</span><span class="sxs-lookup"><span data-stu-id="3f002-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-121">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="3f002-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3f002-122">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-123">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="3f002-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3f002-124">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-125">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="3f002-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3f002-126">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-127">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="3f002-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3f002-128">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-129">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="3f002-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3f002-130">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-131">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="3f002-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3f002-132">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3f002-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3f002-133">*JET_paramEnablePersistedCallbacks*</span><span class="sxs-lookup"><span data-stu-id="3f002-133">*JET_paramEnablePersistedCallbacks*</span></span>  
<span data-ttu-id="3f002-134">156</span><span class="sxs-lookup"><span data-stu-id="3f002-134">156</span></span>  

<span data-ttu-id="3f002-135">Этот параметр позволяет использовать постоянные обратные вызовы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3f002-135">This parameter enables the use of persistent callbacks in the database.</span></span> <span data-ttu-id="3f002-136">В выпусках до Windows Vista использование постоянных обратных вызовов было включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3f002-136">In releases prior to Windows Vista, the use of persistent callbacks was enabled by default.</span></span> <span data-ttu-id="3f002-137">Теперь приложения должны явно разрешить использование постоянных обратных вызовов во время выполнения с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="3f002-137">Applications must now explicitly enable the use of persistent callbacks at runtime using this parameter.</span></span> <span data-ttu-id="3f002-138">Если этот параметр не задан, то любая операция с базой данных, которая требует вызова обратного вызова, завершится с JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="3f002-138">If this parameter is not set, then any database operation that requires the invocation of a callback will fail with JET_errCallbackFailed.</span></span> <span data-ttu-id="3f002-139">Этот параметр не влияет на обратные вызовы, указанные во время выполнения со следующими механизмами: JET_paramRuntimeCallback, [жетрегистеркаллбакк](./jetregistercallback-function.md)или явный параметр обратного вызова для Jet API.</span><span class="sxs-lookup"><span data-stu-id="3f002-139">This parameter does not affect any callbacks that are specified at runtime with the following mechanisms: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md), or an explicit callback parameter to a JET API.</span></span> <span data-ttu-id="3f002-140">Можно создавать элементы схемы, содержащие постоянные обратные вызовы, даже если использование этих постоянных обратных вызовов запрещено.</span><span class="sxs-lookup"><span data-stu-id="3f002-140">It is still possible to create schema elements that contain persistent callbacks even when the use of those persistent callbacks is disallowed.</span></span> <span data-ttu-id="3f002-141">Если этот параметр имеет значение false, он переопределяет JET_paramDisableCallbacks.</span><span class="sxs-lookup"><span data-stu-id="3f002-141">When this parameter is set to false it overrides JET_paramDisableCallbacks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f002-142">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="3f002-142">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3f002-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="3f002-143">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-144">Тип:</span><span class="sxs-lookup"><span data-stu-id="3f002-144">Type:</span></span></p></td>
<td><p><span data-ttu-id="3f002-145">Логическое</span><span class="sxs-lookup"><span data-stu-id="3f002-145">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-146">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="3f002-146">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3f002-147">False, true</span><span class="sxs-lookup"><span data-stu-id="3f002-147">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-148">Область.</span><span class="sxs-lookup"><span data-stu-id="3f002-148">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3f002-149">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="3f002-149">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-150">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="3f002-150">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3f002-151">Да</span><span class="sxs-lookup"><span data-stu-id="3f002-151">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-152">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="3f002-152">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3f002-153">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-154">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="3f002-154">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3f002-155">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-156">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="3f002-156">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3f002-157">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-158">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="3f002-158">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3f002-159">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-159">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-160">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="3f002-160">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3f002-161">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-161">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-162">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="3f002-162">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3f002-163">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3f002-163">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3f002-164">*JET_paramRuntimeCallback*</span><span class="sxs-lookup"><span data-stu-id="3f002-164">*JET_paramRuntimeCallback*</span></span>  
<span data-ttu-id="3f002-165">73</span><span class="sxs-lookup"><span data-stu-id="3f002-165">73</span></span>  

<span data-ttu-id="3f002-166">Этот параметр настраивает подсистему с помощью функции обратного вызова среды выполнения, реализующей интерфейс [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="3f002-166">This parameter configures the engine with a runtime callback function implementing the [JET_CALLBACK](./jet-callback-callback-function.md) interface.</span></span> <span data-ttu-id="3f002-167">Этот обратный вызов можно вызвать по следующим причинам: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)или [JET_cbtypNull](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="3f002-167">This callback may be called for the following reasons: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md), or [JET_cbtypNull](./jet-cbtyp.md).</span></span> <span data-ttu-id="3f002-168">Дополнительные сведения см. в разделе [жетсетлс](./jetsetls-function.md) .</span><span class="sxs-lookup"><span data-stu-id="3f002-168">Please see [JetSetLS](./jetsetls-function.md) for more information.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f002-169">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="3f002-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="3f002-170">NULL</span><span class="sxs-lookup"><span data-stu-id="3f002-170">NULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-171">Тип:</span><span class="sxs-lookup"><span data-stu-id="3f002-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="3f002-172">Указатель функции (JET_API_PTR)</span><span class="sxs-lookup"><span data-stu-id="3f002-172">Function Pointer (JET_API_PTR)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-173">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="3f002-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="3f002-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span><span class="sxs-lookup"><span data-stu-id="3f002-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-175">Область.</span><span class="sxs-lookup"><span data-stu-id="3f002-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="3f002-176">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="3f002-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-177">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="3f002-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="3f002-178">Да</span><span class="sxs-lookup"><span data-stu-id="3f002-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-179">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="3f002-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="3f002-180">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-181">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="3f002-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="3f002-182">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-183">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="3f002-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="3f002-184">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-185">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="3f002-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="3f002-186">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-187">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="3f002-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="3f002-188">Нет</span><span class="sxs-lookup"><span data-stu-id="3f002-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-189">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="3f002-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="3f002-190">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3f002-190">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="3f002-191">Требования</span><span class="sxs-lookup"><span data-stu-id="3f002-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f002-192"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="3f002-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3f002-193">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f002-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f002-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3f002-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3f002-195">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3f002-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f002-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3f002-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3f002-197">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3f002-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3f002-198">См. также:</span><span class="sxs-lookup"><span data-stu-id="3f002-198">See Also</span></span>

[<span data-ttu-id="3f002-199">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="3f002-199">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="3f002-200">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="3f002-200">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="3f002-201">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="3f002-201">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="3f002-202">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="3f002-202">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="3f002-203">жетинит</span><span class="sxs-lookup"><span data-stu-id="3f002-203">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="3f002-204">жетсетлс</span><span class="sxs-lookup"><span data-stu-id="3f002-204">JetSetLS</span></span>](./jetsetls-function.md)
