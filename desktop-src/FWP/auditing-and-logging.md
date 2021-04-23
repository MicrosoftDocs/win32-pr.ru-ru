---
title: Аудит
description: Платформа фильтрации Windows (WFP) обеспечивает аудит событий брандмауэра и IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "103988058"
---
# <a name="auditing"></a><span data-ttu-id="4293c-103">Аудит</span><span class="sxs-lookup"><span data-stu-id="4293c-103">Auditing</span></span>

<span data-ttu-id="4293c-104">Платформа фильтрации Windows (WFP) обеспечивает аудит событий брандмауэра и IPsec.</span><span class="sxs-lookup"><span data-stu-id="4293c-104">The Windows Filtering Platform (WFP) provides auditing of firewall and IPsec related events.</span></span> <span data-ttu-id="4293c-105">Эти события хранятся в системном журнале безопасности.</span><span class="sxs-lookup"><span data-stu-id="4293c-105">These events are stored in the system security log.</span></span>

<span data-ttu-id="4293c-106">Аудит событий выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4293c-106">The audited events are as follows.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4293c-107">Категория аудита</span><span class="sxs-lookup"><span data-stu-id="4293c-107">Auditing category</span></span></th>
<th><span data-ttu-id="4293c-108">Подкатегория аудита</span><span class="sxs-lookup"><span data-stu-id="4293c-108">Auditing subcategory</span></span></th>
<th><span data-ttu-id="4293c-109">События аудита</span><span class="sxs-lookup"><span data-stu-id="4293c-109">Audited events</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4293c-110">Изменение политики</span><span class="sxs-lookup"><span data-stu-id="4293c-110">Policy Change</span></span><br/> <span data-ttu-id="4293c-111">{6997984D-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-111">{6997984D-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-112">Изменение политики платформы фильтрации</span><span class="sxs-lookup"><span data-stu-id="4293c-112">Filtering Platform Policy Change</span></span><br/> <span data-ttu-id="4293c-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4293c-114">Числа представляют идентификаторы событий, отображаемые Просмотр событий (eventvwr.exe).</span><span class="sxs-lookup"><span data-stu-id="4293c-114">The numbers represent the Event IDs as displayed by Event Viewer (eventvwr.exe).</span></span>
</blockquote>
<br/> <span data-ttu-id="4293c-115">Добавление и удаление объектов WFP:</span><span class="sxs-lookup"><span data-stu-id="4293c-115">WFP object addition and removal:</span></span><br/>
<ul>
<li><span data-ttu-id="4293c-116">Добавлена устойчивая выноска 5440</span><span class="sxs-lookup"><span data-stu-id="4293c-116">5440 Persistent callout added</span></span></li>
<li><span data-ttu-id="4293c-117">5441. Добавлен фильтр времени загрузки или постоянного фильтра</span><span class="sxs-lookup"><span data-stu-id="4293c-117">5441 Boot-time or persistent filter added</span></span></li>
<li><span data-ttu-id="4293c-118">Добавлен постоянный поставщик 5442</span><span class="sxs-lookup"><span data-stu-id="4293c-118">5442 Persistent provider added</span></span></li>
<li><span data-ttu-id="4293c-119">Добавлен контекст постоянного поставщика 5443</span><span class="sxs-lookup"><span data-stu-id="4293c-119">5443 Persistent provider context added</span></span></li>
<li><span data-ttu-id="4293c-120">Добавлен постоянный подслой 5444</span><span class="sxs-lookup"><span data-stu-id="4293c-120">5444 Persistent sub-layer added</span></span></li>
<li><span data-ttu-id="4293c-121">5446. выноска времени выполнения добавлена или удалена</span><span class="sxs-lookup"><span data-stu-id="4293c-121">5446 Run-time callout added or removed</span></span></li>
<li><span data-ttu-id="4293c-122">5447 фильтр времени выполнения добавлен или удален</span><span class="sxs-lookup"><span data-stu-id="4293c-122">5447 Run-time filter added or removed</span></span></li>
<li><span data-ttu-id="4293c-123">5448 поставщик времени выполнения добавлен или удален</span><span class="sxs-lookup"><span data-stu-id="4293c-123">5448 Run-time provider added or removed</span></span></li>
<li><span data-ttu-id="4293c-124">5449. Добавление или удаление контекста поставщика времени выполнения</span><span class="sxs-lookup"><span data-stu-id="4293c-124">5449 Run-time provider context added or removed</span></span></li>
<li><span data-ttu-id="4293c-125">5450. подслой времени выполнения добавлен или удален</span><span class="sxs-lookup"><span data-stu-id="4293c-125">5450 Run-time sub-layer added or removed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4293c-126">Доступ к объектам</span><span class="sxs-lookup"><span data-stu-id="4293c-126">Object Access</span></span><br/> <span data-ttu-id="4293c-127">{6997984A-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-127">{6997984A-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-128">Удаление пакета платформы для фильтрации</span><span class="sxs-lookup"><span data-stu-id="4293c-128">Filtering Platform Packet Drop</span></span> <br/> <span data-ttu-id="4293c-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-130">Пакеты, отброшенные WFP:</span><span class="sxs-lookup"><span data-stu-id="4293c-130">Packets dropped by WFP:</span></span><br/>
<ul>
<li><span data-ttu-id="4293c-131">пакет 5152 удален</span><span class="sxs-lookup"><span data-stu-id="4293c-131">5152 Packet dropped</span></span></li>
<li><span data-ttu-id="4293c-132">пакет 5153 с запретом</span><span class="sxs-lookup"><span data-stu-id="4293c-132">5153 Packet vetoed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4293c-133">Доступ к объектам</span><span class="sxs-lookup"><span data-stu-id="4293c-133">Object Access</span></span><br/></td>
<td><span data-ttu-id="4293c-134">Подключение платформы фильтрации</span><span class="sxs-lookup"><span data-stu-id="4293c-134">Filtering Platform Connection</span></span> <br/> <span data-ttu-id="4293c-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-136">Разрешенные и заблокированные подключения:</span><span class="sxs-lookup"><span data-stu-id="4293c-136">Allowed and blocked connections:</span></span><br/>
<ul>
<li><span data-ttu-id="4293c-137">5154 прослушивание разрешено</span><span class="sxs-lookup"><span data-stu-id="4293c-137">5154 Listen permitted</span></span></li>
<li><span data-ttu-id="4293c-138">5155 прослушивание заблокировано</span><span class="sxs-lookup"><span data-stu-id="4293c-138">5155 Listen blocked</span></span></li>
<li><span data-ttu-id="4293c-139">5156 подключение разрешено</span><span class="sxs-lookup"><span data-stu-id="4293c-139">5156 Connection permitted</span></span></li>
<li><span data-ttu-id="4293c-140">5157 подключение заблокировано</span><span class="sxs-lookup"><span data-stu-id="4293c-140">5157 Connection blocked</span></span></li>
<li><span data-ttu-id="4293c-141">5158. разрешенная привязка</span><span class="sxs-lookup"><span data-stu-id="4293c-141">5158 Bind permitted</span></span></li>
<li><span data-ttu-id="4293c-142">5159 привязка заблокирована</span><span class="sxs-lookup"><span data-stu-id="4293c-142">5159 Bind blocked</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="4293c-143">Разрешенные подключения не всегда выполняют аудит идентификатора связанного фильтра.</span><span class="sxs-lookup"><span data-stu-id="4293c-143">Permitted connections do not always audit the ID of the associated filter.</span></span> <span data-ttu-id="4293c-144">Филтерид для TCP будет иметь значение 0, если не используется подмножество этих условий фильтрации: UserID, AppID, Protocol, удаленный порт.</span><span class="sxs-lookup"><span data-stu-id="4293c-144">The FilterID for TCP will be 0 unless a subset of these filtering conditions are used: UserID, AppID, Protocol, Remote Port.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4293c-145">Доступ к объектам</span><span class="sxs-lookup"><span data-stu-id="4293c-145">Object Access</span></span><br/></td>
<td><span data-ttu-id="4293c-146">Другие события доступа к объекту</span><span class="sxs-lookup"><span data-stu-id="4293c-146">Other Object Access Events</span></span><br/> <span data-ttu-id="4293c-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4293c-148">Эта подкатегория включает много аудитов.</span><span class="sxs-lookup"><span data-stu-id="4293c-148">This subcategory enables many audits.</span></span> <span data-ttu-id="4293c-149">Аудиты, относящиеся к WFP, перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="4293c-149">WFP specific audits are listed below.</span></span>
</blockquote>
<br/> <span data-ttu-id="4293c-150">Состояние предотвращения отказа в обслуживании:</span><span class="sxs-lookup"><span data-stu-id="4293c-150">Denial of Service prevention status:</span></span><br/>
<ul>
<li><span data-ttu-id="4293c-151">5148 режим предотвращения DoS WFP запущен</span><span class="sxs-lookup"><span data-stu-id="4293c-151">5148 WFP DoS prevention mode started</span></span></li>
<li><span data-ttu-id="4293c-152">5149 режим предотвращения DoS WFP остановлен</span><span class="sxs-lookup"><span data-stu-id="4293c-152">5149 WFP DoS prevention mode stopped</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4293c-153">Вход и выход из системы</span><span class="sxs-lookup"><span data-stu-id="4293c-153">Logon/Logoff</span></span><br/> <span data-ttu-id="4293c-154">{69979849-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-154">{69979849-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-155">Основной режим IPsec</span><span class="sxs-lookup"><span data-stu-id="4293c-155">IPsec Main Mode</span></span><br/> <span data-ttu-id="4293c-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-157">Согласование основного режима IKE и AuthIP:</span><span class="sxs-lookup"><span data-stu-id="4293c-157">IKE and AuthIP Main Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="4293c-158">4650, установлено сопоставление безопасности 4651</span><span class="sxs-lookup"><span data-stu-id="4293c-158">4650, 4651 Security association established</span></span></li>
<li><span data-ttu-id="4293c-159">4652, сбой согласования 4653</span><span class="sxs-lookup"><span data-stu-id="4293c-159">4652, 4653 Negotiation failed</span></span></li>
<li><span data-ttu-id="4293c-160">4655 сопоставление безопасности завершено</span><span class="sxs-lookup"><span data-stu-id="4293c-160">4655 Security association ended</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4293c-161">Вход и выход из системы</span><span class="sxs-lookup"><span data-stu-id="4293c-161">Logon/Logoff</span></span><br/></td>
<td><span data-ttu-id="4293c-162">Быстрый режим IPsec</span><span class="sxs-lookup"><span data-stu-id="4293c-162">IPsec Quick Mode</span></span> <br/> <span data-ttu-id="4293c-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-164">Согласование быстрого режима IKE и AuthIP:</span><span class="sxs-lookup"><span data-stu-id="4293c-164">IKE and AuthIP Quick Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="4293c-165">установлено сопоставление безопасности 5451</span><span class="sxs-lookup"><span data-stu-id="4293c-165">5451 Security association established</span></span></li>
<li><span data-ttu-id="4293c-166">5452 сопоставление безопасности завершено</span><span class="sxs-lookup"><span data-stu-id="4293c-166">5452 Security association ended</span></span></li>
<li><span data-ttu-id="4293c-167">сбой согласования 4654</span><span class="sxs-lookup"><span data-stu-id="4293c-167">4654 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4293c-168">Вход и выход из системы</span><span class="sxs-lookup"><span data-stu-id="4293c-168">Logon/Logoff</span></span> <br/></td>
<td><span data-ttu-id="4293c-169">Расширенный режим IPsec</span><span class="sxs-lookup"><span data-stu-id="4293c-169">IPsec Extended Mode</span></span><br/> <span data-ttu-id="4293c-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-171">Согласование расширенного режима AuthIP:</span><span class="sxs-lookup"><span data-stu-id="4293c-171">AuthIP Extended Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="4293c-172">4978 недопустимый пакет согласования</span><span class="sxs-lookup"><span data-stu-id="4293c-172">4978 Invalid negotiation packet</span></span></li>
<li><span data-ttu-id="4293c-173">4979, 4980, 4981, установлена Ассоциация безопасности 4982</span><span class="sxs-lookup"><span data-stu-id="4293c-173">4979, 4980, 4981, 4982 Security association established</span></span></li>
<li><span data-ttu-id="4293c-174">4983, сбой согласования 4984</span><span class="sxs-lookup"><span data-stu-id="4293c-174">4983, 4984 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4293c-175">Система</span><span class="sxs-lookup"><span data-stu-id="4293c-175">System</span></span><br/> <span data-ttu-id="4293c-176">{69979848-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-176">{69979848-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-177">Драйвер IPsec</span><span class="sxs-lookup"><span data-stu-id="4293c-177">IPsec Driver</span></span><br/> <span data-ttu-id="4293c-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4293c-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4293c-179">Пакеты, отброшенные драйвером IPsec:</span><span class="sxs-lookup"><span data-stu-id="4293c-179">Packets dropped by the IPsec driver:</span></span><br/>
<ul>
<li><span data-ttu-id="4293c-180">4963 входящих пакетов с открытым текстом отброшено</span><span class="sxs-lookup"><span data-stu-id="4293c-180">4963 Inbound clear text packet dropped</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4293c-181">По умолчанию аудит для WFP отключен.</span><span class="sxs-lookup"><span data-stu-id="4293c-181">By default, auditing for WFP is disabled.</span></span>

<span data-ttu-id="4293c-182">Аудит можно включить для отдельных категорий с помощью оснастки консоли управления редактор объектов групповой политики MMC, оснастки локальной политики безопасности MMC или команды auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="4293c-182">Auditing can be enabled on a per-category basis through either the Group Policy Object Editor MMC snap-in, the Local Security Policy MMC snap-in, or the auditpol.exe command.</span></span>

<span data-ttu-id="4293c-183">Например, чтобы включить аудит событий изменения политики, вы можете:</span><span class="sxs-lookup"><span data-stu-id="4293c-183">For example, to enable the auditing of Policy Change events you may:</span></span>

-   <span data-ttu-id="4293c-184">Использование редактор объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="4293c-184">Use the Group Policy Object Editor</span></span>

    1.  <span data-ttu-id="4293c-185">Запустите **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="4293c-185">Run **gpedit.msc**.</span></span>
    2.  <span data-ttu-id="4293c-186">Разверните узел Политика локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="4293c-186">Expand Local Computer Policy.</span></span>
    3.  <span data-ttu-id="4293c-187">Разверните узел Конфигурация компьютера.</span><span class="sxs-lookup"><span data-stu-id="4293c-187">Expand Computer Configuration.</span></span>
    4.  <span data-ttu-id="4293c-188">Разверните узел Параметры Windows.</span><span class="sxs-lookup"><span data-stu-id="4293c-188">Expand Windows Settings.</span></span>
    5.  <span data-ttu-id="4293c-189">Разверните узел Параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="4293c-189">Expand Security Settings.</span></span>
    6.  <span data-ttu-id="4293c-190">Разверните узел Локальные политики.</span><span class="sxs-lookup"><span data-stu-id="4293c-190">Expand Local Policies.</span></span>
    7.  <span data-ttu-id="4293c-191">Щелкните Политика аудита.</span><span class="sxs-lookup"><span data-stu-id="4293c-191">Click Audit Policy.</span></span>
    8.  <span data-ttu-id="4293c-192">Чтобы открыть диалоговое окно "Свойства", дважды щелкните Аудит изменение политики.</span><span class="sxs-lookup"><span data-stu-id="4293c-192">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    9.  <span data-ttu-id="4293c-193">Установите флажки успешные и неудачные.</span><span class="sxs-lookup"><span data-stu-id="4293c-193">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="4293c-194">Использование локальной политики безопасности</span><span class="sxs-lookup"><span data-stu-id="4293c-194">Use the Local Security Policy</span></span>

    1.  <span data-ttu-id="4293c-195">Выполните команду **secpol. msc**.</span><span class="sxs-lookup"><span data-stu-id="4293c-195">Run **secpol.msc**.</span></span>
    2.  <span data-ttu-id="4293c-196">Разверните узел Локальные политики.</span><span class="sxs-lookup"><span data-stu-id="4293c-196">Expand Local Policies.</span></span>
    3.  <span data-ttu-id="4293c-197">Щелкните Политика аудита.</span><span class="sxs-lookup"><span data-stu-id="4293c-197">Click Audit Policy.</span></span>
    4.  <span data-ttu-id="4293c-198">Чтобы открыть диалоговое окно "Свойства", дважды щелкните Аудит изменение политики.</span><span class="sxs-lookup"><span data-stu-id="4293c-198">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    5.  <span data-ttu-id="4293c-199">Установите флажки успешные и неудачные.</span><span class="sxs-lookup"><span data-stu-id="4293c-199">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="4293c-200">Использование команды auditpol.exe</span><span class="sxs-lookup"><span data-stu-id="4293c-200">Use the auditpol.exe command</span></span>

    -   <span data-ttu-id="4293c-201">**auditpol/Set/Category: "изменение политики"/сукцесс: включение/фаилуре: enable**</span><span class="sxs-lookup"><span data-stu-id="4293c-201">**auditpol /set /category:"Policy Change" /success:enable /failure:enable**</span></span>

<span data-ttu-id="4293c-202">Аудит можно включить для отдельных категорий, только с помощью команды auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="4293c-202">Auditing can be enabled on a per-subcategory basis only through the auditpol.exe command.</span></span>

<span data-ttu-id="4293c-203">Имена категорий аудита и подкатегорий локализованы.</span><span class="sxs-lookup"><span data-stu-id="4293c-203">The auditing category and subcategory names are localized.</span></span> <span data-ttu-id="4293c-204">Чтобы избежать локализации сценариев аудита, вместо имен можно использовать соответствующие идентификаторы GUID.</span><span class="sxs-lookup"><span data-stu-id="4293c-204">To avoid localization for auditing scripts, the corresponding GUIDs may be used in place of the names.</span></span>

<span data-ttu-id="4293c-205">Например, чтобы включить аудит событий изменения политики платформы фильтрации, можно использовать одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="4293c-205">For example, to enable the auditing of Filtering Platform Policy Change events you may use either one of the following commands:</span></span>

-   <span data-ttu-id="4293c-206">**auditpol/Set/субкатегори: "изменение политики платформы фильтрации"/сукцесс: включение/фаилуре: enable**</span><span class="sxs-lookup"><span data-stu-id="4293c-206">**auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**</span></span>
-   <span data-ttu-id="4293c-207">**auditpol/Set/субкатегори: "{0CCE9233-69AE-11D9-BED3-505054503030}"/сукцесс: enable/фаилуре: enable**</span><span class="sxs-lookup"><span data-stu-id="4293c-207">**auditpol /set /subcategory:"{0CCE9233-69AE-11D9-BED3-505054503030}" /success:enable /failure:enable**</span></span>

## <a name="related-topics"></a><span data-ttu-id="4293c-208">См. также</span><span class="sxs-lookup"><span data-stu-id="4293c-208">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4293c-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="4293c-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="4293c-210">[Журнал событий](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4293c-210">[Event Log](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="4293c-211">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="4293c-211">Group Policy</span></span>](/windows/deployment/deploy-whats-new)
</dt> </dl>

