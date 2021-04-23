---
description: 'Дополнительные сведения: параметры журнала событий'
title: Параметры журнала событий
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080971"
---
# <a name="event-log-parameters"></a><span data-ttu-id="b198d-103">Параметры журнала событий</span><span class="sxs-lookup"><span data-stu-id="b198d-103">Event Log Parameters</span></span>


<span data-ttu-id="b198d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b198d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-log-parameters"></a><span data-ttu-id="b198d-105">Параметры журнала событий</span><span class="sxs-lookup"><span data-stu-id="b198d-105">Event Log Parameters</span></span>

<span data-ttu-id="b198d-106">Этот раздел содержит параметры, которые используются для журнала событий.</span><span class="sxs-lookup"><span data-stu-id="b198d-106">This topic contains parameters that are used for the event log.</span></span>

<span data-ttu-id="b198d-107">JET_paramEventLogCache</span><span class="sxs-lookup"><span data-stu-id="b198d-107">JET_paramEventLogCache</span></span>  
<span data-ttu-id="b198d-108">Этот параметр определяет размер (в байтах) кэша сообщений EventLog, который будет содержать сообщения EventLog, созданные ядром СУБД при остановке службы EventLog.</span><span class="sxs-lookup"><span data-stu-id="b198d-108">This parameter controls the size (in bytes) of an eventlog message cache that will hold eventlog messages emitted by the database engine while the eventlog service is stopped.</span></span> <span data-ttu-id="b198d-109">Эти кэшированные сообщения будут записаны в журнал событий, когда служба станет работоспособной.</span><span class="sxs-lookup"><span data-stu-id="b198d-109">These cached messages will be flushed to the eventlog when the service becomes operational.</span></span> <span data-ttu-id="b198d-110">Все сообщения, превышающие размер кэша, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="b198d-110">Any messages that overflow the cache will be dropped.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b198d-111">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="b198d-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b198d-112">0</span><span class="sxs-lookup"><span data-stu-id="b198d-112">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="b198d-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="b198d-114">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="b198d-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-115">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="b198d-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b198d-116">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="b198d-116">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-117">Область.</span><span class="sxs-lookup"><span data-stu-id="b198d-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b198d-118">Глобальный</span><span class="sxs-lookup"><span data-stu-id="b198d-118">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-119">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-120">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-121">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-122">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-123">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="b198d-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b198d-124">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-125">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="b198d-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-126">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-127">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="b198d-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b198d-128">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-129">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="b198d-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b198d-130">Да</span><span class="sxs-lookup"><span data-stu-id="b198d-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-131">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="b198d-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-132">Все</span><span class="sxs-lookup"><span data-stu-id="b198d-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b198d-133">*JET_paramEventLoggingLevel*</span><span class="sxs-lookup"><span data-stu-id="b198d-133">*JET_paramEventLoggingLevel*</span></span>  
  
<span data-ttu-id="b198d-134">Этот параметр задает уровень детализации сообщений журнала событий, которые передаются в журнал событий ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="b198d-134">This parameter configures the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="b198d-135">Более высокие значения приводят к более подробным сообщениям журнала событий.</span><span class="sxs-lookup"><span data-stu-id="b198d-135">Higher numbers will result in more detailed eventlog messages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b198d-136">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="b198d-136">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b198d-137">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="b198d-137">JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-138">Тип:</span><span class="sxs-lookup"><span data-stu-id="b198d-138">Type:</span></span></p></td>
<td><p><span data-ttu-id="b198d-139">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="b198d-139">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-140">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="b198d-140">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b198d-141">JET_EventLoggingDisable — JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="b198d-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-142">Область.</span><span class="sxs-lookup"><span data-stu-id="b198d-142">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b198d-143">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="b198d-143">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-144">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-144">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-145">Да</span><span class="sxs-lookup"><span data-stu-id="b198d-145">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-146">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-146">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-147">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-147">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-148">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="b198d-148">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b198d-149">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-150">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="b198d-150">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-151">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-151">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-152">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="b198d-152">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b198d-153">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-154">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="b198d-154">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b198d-155">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-155">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-156">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="b198d-156">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-157">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="b198d-157">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b198d-158">*JET_paramEventSource*</span><span class="sxs-lookup"><span data-stu-id="b198d-158">*JET_paramEventSource*</span></span>  
<span data-ttu-id="b198d-159">4</span><span class="sxs-lookup"><span data-stu-id="b198d-159">4</span></span>  

<span data-ttu-id="b198d-160">Этот параметр предоставляет строку конкретного приложения, которая будет добавлена в любые сообщения журнала событий, созданные ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="b198d-160">This parameter supplies an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="b198d-161">Это позволяет легко сопоставить сообщения журнала событий с исходным приложением.</span><span class="sxs-lookup"><span data-stu-id="b198d-161">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="b198d-162">Если указана пустая строка (как по умолчанию), будет использоваться имя исполняемого файла ведущего приложения.</span><span class="sxs-lookup"><span data-stu-id="b198d-162">If an empty string is specified (as is the default) then the host application executable name will be used.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b198d-163">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="b198d-163">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-164">Тип:</span><span class="sxs-lookup"><span data-stu-id="b198d-164">Type:</span></span></p></td>
<td><p><span data-ttu-id="b198d-165">Строка</span><span class="sxs-lookup"><span data-stu-id="b198d-165">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-166">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="b198d-166">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b198d-167">0 – 259 символов</span><span class="sxs-lookup"><span data-stu-id="b198d-167">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-168">Область.</span><span class="sxs-lookup"><span data-stu-id="b198d-168">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b198d-169">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="b198d-169">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-170">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-170">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-171">Да</span><span class="sxs-lookup"><span data-stu-id="b198d-171">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-172">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-172">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-173">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-173">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-174">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="b198d-174">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b198d-175">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-175">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-176">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="b198d-176">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-177">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-178">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="b198d-178">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b198d-179">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-180">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="b198d-180">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b198d-181">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-182">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="b198d-182">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-183">Все</span><span class="sxs-lookup"><span data-stu-id="b198d-183">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b198d-184">*JET_paramEventSourceKey*</span><span class="sxs-lookup"><span data-stu-id="b198d-184">*JET_paramEventSourceKey*</span></span>  
<span data-ttu-id="b198d-185">49</span><span class="sxs-lookup"><span data-stu-id="b198d-185">49</span></span>  

<span data-ttu-id="b198d-186">Этот параметр можно использовать для управления журналом событий, который ядро СУБД использует для сообщений журнала событий.</span><span class="sxs-lookup"><span data-stu-id="b198d-186">This parameter can be used to control which event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="b198d-187">По умолчанию все сообщения журнала событий перемещаются в журнал событий приложений.</span><span class="sxs-lookup"><span data-stu-id="b198d-187">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="b198d-188">Если будет настроено имя раздела реестра для другого журнала событий, вместо этого будут отправлены сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="b198d-188">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b198d-189">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="b198d-189">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-190">Тип:</span><span class="sxs-lookup"><span data-stu-id="b198d-190">Type:</span></span></p></td>
<td><p><span data-ttu-id="b198d-191">Строка</span><span class="sxs-lookup"><span data-stu-id="b198d-191">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-192">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="b198d-192">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b198d-193">0 – 259 символов</span><span class="sxs-lookup"><span data-stu-id="b198d-193">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-194">Область.</span><span class="sxs-lookup"><span data-stu-id="b198d-194">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b198d-195">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="b198d-195">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-196">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-196">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-197">Да</span><span class="sxs-lookup"><span data-stu-id="b198d-197">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-198">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-198">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-199">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-199">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-200">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="b198d-200">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b198d-201">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-201">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-202">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="b198d-202">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-203">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-203">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-204">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="b198d-204">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b198d-205">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-205">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-206">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="b198d-206">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b198d-207">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-208">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="b198d-208">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-209">Все</span><span class="sxs-lookup"><span data-stu-id="b198d-209">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b198d-210">*JET_paramNoInformationEvent*</span><span class="sxs-lookup"><span data-stu-id="b198d-210">*JET_paramNoInformationEvent*</span></span>  
<span data-ttu-id="b198d-211">50</span><span class="sxs-lookup"><span data-stu-id="b198d-211">50</span></span>  

<span data-ttu-id="b198d-212">Если этот параметр имеет значение true, сообщения журнала событий, обычно создаваемые ядром СУБД, будут подавлены.</span><span class="sxs-lookup"><span data-stu-id="b198d-212">When this parameter is true, informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b198d-213">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="b198d-213">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b198d-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="b198d-214">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-215">Тип:</span><span class="sxs-lookup"><span data-stu-id="b198d-215">Type:</span></span></p></td>
<td><p><span data-ttu-id="b198d-216">Логическое</span><span class="sxs-lookup"><span data-stu-id="b198d-216">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-217">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="b198d-217">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b198d-218">False, true</span><span class="sxs-lookup"><span data-stu-id="b198d-218">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-219">Область.</span><span class="sxs-lookup"><span data-stu-id="b198d-219">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b198d-220">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="b198d-220">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-221">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-221">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-222">Да</span><span class="sxs-lookup"><span data-stu-id="b198d-222">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-223">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="b198d-223">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b198d-224">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-224">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-225">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="b198d-225">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b198d-226">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-226">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-227">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="b198d-227">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-228">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-228">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-229">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="b198d-229">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b198d-230">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-231">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="b198d-231">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b198d-232">Нет</span><span class="sxs-lookup"><span data-stu-id="b198d-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-233">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="b198d-233">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b198d-234">Все</span><span class="sxs-lookup"><span data-stu-id="b198d-234">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="b198d-235">Требования</span><span class="sxs-lookup"><span data-stu-id="b198d-235">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b198d-236"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="b198d-236"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b198d-237">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b198d-237">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b198d-238"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b198d-238"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b198d-239">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b198d-239">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b198d-240"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b198d-240"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b198d-241">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b198d-241">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b198d-242">См. также:</span><span class="sxs-lookup"><span data-stu-id="b198d-242">See Also</span></span>

[<span data-ttu-id="b198d-243">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="b198d-243">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="b198d-244">жетинит</span><span class="sxs-lookup"><span data-stu-id="b198d-244">JetInit</span></span>](./jetinit-function.md)
