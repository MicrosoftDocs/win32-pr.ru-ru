---
description: Перечисляет типы ACE, определенные в данный момент.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647305"
---
# <a name="ace"></a><span data-ttu-id="485d3-103">ТУЗ</span><span class="sxs-lookup"><span data-stu-id="485d3-103">ACE</span></span>

<span data-ttu-id="485d3-104">**ACE** — это [*запись управления доступом*](/windows/desktop/SecGloss/a-gly) в [*списке управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="485d3-104">An **ACE** is an [*access control entry*](/windows/desktop/SecGloss/a-gly) in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span>

<span data-ttu-id="485d3-105">В следующей таблице перечислены определенные в данный момент типы **ACE** .</span><span class="sxs-lookup"><span data-stu-id="485d3-105">The following table lists the currently defined **ACE** types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="485d3-106">Тип ACE</span><span class="sxs-lookup"><span data-stu-id="485d3-106">ACE type</span></span></th>
<th><span data-ttu-id="485d3-107">Структура</span><span class="sxs-lookup"><span data-stu-id="485d3-107">Structure</span></span></th>
<th><span data-ttu-id="485d3-108">Тип ACL</span><span class="sxs-lookup"><span data-stu-id="485d3-108">ACL type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="485d3-109">Доступ разрешен</span><span class="sxs-lookup"><span data-stu-id="485d3-109">Access allowed</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-111">Разграничительного</span><span class="sxs-lookup"><span data-stu-id="485d3-111">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="485d3-112">Доступ разрешен</span><span class="sxs-lookup"><span data-stu-id="485d3-112">Access allowed</span></span></li>
<li><span data-ttu-id="485d3-113">Разрешает обратный вызов во время проверки доступа</span><span class="sxs-lookup"><span data-stu-id="485d3-113">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-115">Разграничительного</span><span class="sxs-lookup"><span data-stu-id="485d3-115">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="485d3-116">Доступ разрешен</span><span class="sxs-lookup"><span data-stu-id="485d3-116">Access allowed</span></span></li>
<li><span data-ttu-id="485d3-117">Для конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="485d3-117">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-119">Разграничительного</span><span class="sxs-lookup"><span data-stu-id="485d3-119">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="485d3-120">Доступ разрешен</span><span class="sxs-lookup"><span data-stu-id="485d3-120">Access allowed</span></span></li>
<li><span data-ttu-id="485d3-121">Для конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="485d3-121">Object specific</span></span></li>
<li><span data-ttu-id="485d3-122">Разрешает обратный вызов во время проверки доступа</span><span class="sxs-lookup"><span data-stu-id="485d3-122">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-124">Разграничительного</span><span class="sxs-lookup"><span data-stu-id="485d3-124">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="485d3-125">Доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="485d3-125">Access denied</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-127">Разграничительного</span><span class="sxs-lookup"><span data-stu-id="485d3-127">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="485d3-128">Доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="485d3-128">Access denied</span></span></li>
<li><span data-ttu-id="485d3-129">Разрешает обратный вызов во время проверки доступа</span><span class="sxs-lookup"><span data-stu-id="485d3-129">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-131">Разграничительного</span><span class="sxs-lookup"><span data-stu-id="485d3-131">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="485d3-132">Доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="485d3-132">Access denied</span></span></li>
<li><span data-ttu-id="485d3-133">Для конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="485d3-133">Object specific</span></span></li>
<li><span data-ttu-id="485d3-134">Разрешает обратный вызов во время проверки доступа</span><span class="sxs-lookup"><span data-stu-id="485d3-134">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-136">Разграничительного</span><span class="sxs-lookup"><span data-stu-id="485d3-136">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="485d3-137">Доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="485d3-137">Access denied</span></span></li>
<li><span data-ttu-id="485d3-138">Для конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="485d3-138">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-140">Разграничительного</span><span class="sxs-lookup"><span data-stu-id="485d3-140">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="485d3-141">Системный сигнал</span><span class="sxs-lookup"><span data-stu-id="485d3-141">System alarm</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-143">Система</span><span class="sxs-lookup"><span data-stu-id="485d3-143">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="485d3-144">Системный сигнал</span><span class="sxs-lookup"><span data-stu-id="485d3-144">System alarm</span></span></li>
<li><span data-ttu-id="485d3-145">Разрешает обратный вызов во время проверки доступа</span><span class="sxs-lookup"><span data-stu-id="485d3-145">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-147">Система</span><span class="sxs-lookup"><span data-stu-id="485d3-147">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="485d3-148">Системный сигнал</span><span class="sxs-lookup"><span data-stu-id="485d3-148">System alarm</span></span></li>
<li><span data-ttu-id="485d3-149">Для конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="485d3-149">Object specific</span></span></li>
<li><span data-ttu-id="485d3-150">Разрешает обратный вызов во время проверки доступа</span><span class="sxs-lookup"><span data-stu-id="485d3-150">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-152">Система</span><span class="sxs-lookup"><span data-stu-id="485d3-152">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="485d3-153">Системный сигнал</span><span class="sxs-lookup"><span data-stu-id="485d3-153">System alarm</span></span></li>
<li><span data-ttu-id="485d3-154">Для конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="485d3-154">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-156">Система</span><span class="sxs-lookup"><span data-stu-id="485d3-156">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="485d3-157">Аудит системы</span><span class="sxs-lookup"><span data-stu-id="485d3-157">System audit</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-159">Система</span><span class="sxs-lookup"><span data-stu-id="485d3-159">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="485d3-160">Аудит системы</span><span class="sxs-lookup"><span data-stu-id="485d3-160">System audit</span></span></li>
<li><span data-ttu-id="485d3-161">Разрешает обратный вызов во время проверки доступа</span><span class="sxs-lookup"><span data-stu-id="485d3-161">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-163">Система</span><span class="sxs-lookup"><span data-stu-id="485d3-163">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="485d3-164">Аудит системы</span><span class="sxs-lookup"><span data-stu-id="485d3-164">System audit</span></span></li>
<li><span data-ttu-id="485d3-165">Для конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="485d3-165">Object specific</span></span></li>
<li><span data-ttu-id="485d3-166">Разрешает обратный вызов во время проверки доступа</span><span class="sxs-lookup"><span data-stu-id="485d3-166">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-168">Система</span><span class="sxs-lookup"><span data-stu-id="485d3-168">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="485d3-169">Аудит системы</span><span class="sxs-lookup"><span data-stu-id="485d3-169">System audit</span></span></li>
<li><span data-ttu-id="485d3-170">Для конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="485d3-170">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="485d3-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="485d3-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="485d3-172">Система</span><span class="sxs-lookup"><span data-stu-id="485d3-172">System</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="485d3-173">Системные оповещения и элементы управления оповещениями системы не поддерживаются в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="485d3-173">System-alarm and object-specific system-alarm ACEs are not currently supported.</span></span>

> [!Note]  
> <span data-ttu-id="485d3-174">Каждая запись ACE начинается с [**структуры \_ заголовка ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="485d3-174">Each ACE starts with an [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="485d3-175">Формат данных, следующих за заголовком, различается в зависимости от типа ACE, указанного в заголовке.</span><span class="sxs-lookup"><span data-stu-id="485d3-175">The format of the data following the header varies according to the ACE type specified in the header.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="485d3-176">Требования</span><span class="sxs-lookup"><span data-stu-id="485d3-176">Requirements</span></span>



| <span data-ttu-id="485d3-177">Требование</span><span class="sxs-lookup"><span data-stu-id="485d3-177">Requirement</span></span> | <span data-ttu-id="485d3-178">Значение</span><span class="sxs-lookup"><span data-stu-id="485d3-178">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="485d3-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="485d3-179">Minimum supported client</span></span><br/> | <span data-ttu-id="485d3-180">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="485d3-180">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="485d3-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="485d3-181">Minimum supported server</span></span><br/> | <span data-ttu-id="485d3-182">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="485d3-182">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="485d3-183">Header</span><span class="sxs-lookup"><span data-stu-id="485d3-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="485d3-184"><dt>Файл Winnt. h (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="485d3-184"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="485d3-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="485d3-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="485d3-186">**аддаце**</span><span class="sxs-lookup"><span data-stu-id="485d3-186">**AddAce**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[<span data-ttu-id="485d3-187">**ДОСТУП к \_ разрешенному \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="485d3-187">**ACCESS\_ALLOWED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[<span data-ttu-id="485d3-188">**ДОСТУП \_ запрещен \_**</span><span class="sxs-lookup"><span data-stu-id="485d3-188">**ACCESS\_DENIED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[<span data-ttu-id="485d3-189">**СПИСКОМ**</span><span class="sxs-lookup"><span data-stu-id="485d3-189">**ACL**</span></span>](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[<span data-ttu-id="485d3-190">**\_ACE системного оповещения \_**</span><span class="sxs-lookup"><span data-stu-id="485d3-190">**SYSTEM\_ALARM\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[<span data-ttu-id="485d3-191">**\_ACE аудита \_ системы**</span><span class="sxs-lookup"><span data-stu-id="485d3-191">**SYSTEM\_AUDIT\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

