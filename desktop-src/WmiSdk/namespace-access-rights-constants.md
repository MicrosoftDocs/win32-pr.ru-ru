---
description: 'WMI содержит константы безопасности, используемые для проверки доступа к пространству имен с помощью \_ \_ системсекурити:: жеткаллеракцессригхтс.'
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Константы прав доступа к пространству имен (Вбемкли. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072602"
---
# <a name="namespace-access-rights-constants"></a><span data-ttu-id="021bb-103">Константы прав доступа к пространству имен</span><span class="sxs-lookup"><span data-stu-id="021bb-103">Namespace Access Rights Constants</span></span>

<span data-ttu-id="021bb-104">WMI содержит константы безопасности, используемые для проверки доступа к пространству имен с помощью [**\_ \_ системсекурити:: жеткаллеракцессригхтс**](--systemsecurity-getcalleraccessrights.md).</span><span class="sxs-lookup"><span data-stu-id="021bb-104">WMI has security constants used for namespace access checking by [**\_\_SystemSecurity::GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span></span> <span data-ttu-id="021bb-105">Сведения о безопасности списков управления доступом (ACL, DACL и SACL) см. в разделе [списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) и [**стандартные права доступа**](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="021bb-105">For security information about access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [**Standard Access Rights**](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="021bb-106">Эти константы определяются в перечислении **\_ \_ флагов безопасности WBEM** .</span><span class="sxs-lookup"><span data-stu-id="021bb-106">These constants are defined in the **WBEM\_SECURITY\_FLAGS** enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="021bb-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**\_Включение WBEM**</span><span class="sxs-lookup"><span data-stu-id="021bb-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="021bb-108">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="021bb-108">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="021bb-109">Включает учетную запись и предоставляет пользователю разрешения на чтение.</span><span class="sxs-lookup"><span data-stu-id="021bb-109">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="021bb-110">Это право доступа по умолчанию для всех пользователей и соответствует разрешению «включение учетной записи» на вкладке «Безопасность» [*элемента управления WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="021bb-110">This is a default access right for all users and corresponds to the Enable Account permission on the Security tab of the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="021bb-111">Дополнительные сведения см. [в разделе Настройка безопасности пространства имен с помощью элемента управления WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="021bb-111">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="021bb-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**\_выполнение метода \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="021bb-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="021bb-113">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="021bb-113">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="021bb-114">Разрешает выполнение методов.</span><span class="sxs-lookup"><span data-stu-id="021bb-114">Allows the execution of methods.</span></span> <span data-ttu-id="021bb-115">Поставщики могут выполнять дополнительные проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="021bb-115">Providers can perform additional access checks.</span></span> <span data-ttu-id="021bb-116">Это право доступа по умолчанию для всех пользователей и соответствует разрешению «выполнение методов» на вкладке «Безопасность» элемента управления WMI.</span><span class="sxs-lookup"><span data-stu-id="021bb-116">This is a default access right for all users and corresponds to the Execute Methods permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="021bb-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**Менеджер WBEM с \_ полной \_ записью \_**</span><span class="sxs-lookup"><span data-stu-id="021bb-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="021bb-118">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="021bb-118">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="021bb-119">Позволяет учетной записи пользователя выполнять запись в классы в репозитории WMI и экземплярах.</span><span class="sxs-lookup"><span data-stu-id="021bb-119">Allows a user account to write to classes in the WMI repository as well as instances.</span></span> <span data-ttu-id="021bb-120">Пользователь не может выполнять запись в системные классы.</span><span class="sxs-lookup"><span data-stu-id="021bb-120">A user cannot write to system classes.</span></span> <span data-ttu-id="021bb-121">Только члены группы "Администраторы" имеют это разрешение.</span><span class="sxs-lookup"><span data-stu-id="021bb-121">Only members of the Administrators group have this permission.</span></span> <span data-ttu-id="021bb-122">**WBEM \_ \_ \_ Представитель полной записи** соответствует разрешению на запись для всей записи на вкладке Безопасность элемента управления WMI.</span><span class="sxs-lookup"><span data-stu-id="021bb-122">**WBEM\_FULL\_WRITE\_REP** corresponds to the Full Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="021bb-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_представитель с частичным \_ НАПИСАНием WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="021bb-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="021bb-124">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="021bb-124">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="021bb-125">Позволяет записывать данные только в экземпляры, а не классы.</span><span class="sxs-lookup"><span data-stu-id="021bb-125">Allows you to write data to instances only, not classes.</span></span> <span data-ttu-id="021bb-126">Пользователь не может записывать классы в [*репозиторий WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="021bb-126">A user cannot write classes to the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="021bb-127">Это право имеют только члены группы "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="021bb-127">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="021bb-128">**WBEM \_ \_ \_ Представитель частичной записи** соответствует разрешению частичной записи на вкладке Безопасность элемента управления WMI.</span><span class="sxs-lookup"><span data-stu-id="021bb-128">**WBEM\_PARTIAL\_WRITE\_REP** corresponds to the Partial Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="021bb-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_поставщик записи \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="021bb-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="021bb-130">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="021bb-130">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="021bb-131">Позволяет создавать классы и экземпляры для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="021bb-131">Allows writing classes and instances to providers.</span></span> <span data-ttu-id="021bb-132">Обратите внимание, что поставщики могут выполнять дополнительные проверки доступа при олицетворении пользователя.</span><span class="sxs-lookup"><span data-stu-id="021bb-132">Note that providers can do additional access checks when impersonating a user.</span></span> <span data-ttu-id="021bb-133">Это право доступа по умолчанию для всех пользователей и соответствует разрешению на запись для поставщика на вкладке Безопасность элемента управления WMI.</span><span class="sxs-lookup"><span data-stu-id="021bb-133">This is a default access right for all users and corresponds to the Provider Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="021bb-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_Удаленный \_ доступ WBEM**</span><span class="sxs-lookup"><span data-stu-id="021bb-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="021bb-135">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="021bb-135">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="021bb-136">Позволяет учетной записи пользователя удаленно выполнять любые операции, разрешенные описанными выше разрешениями.</span><span class="sxs-lookup"><span data-stu-id="021bb-136">Allows a user account to remotely perform any operations allowed by the permissions described above.</span></span> <span data-ttu-id="021bb-137">Это право имеют только члены группы "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="021bb-137">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="021bb-138">**WBEM \_ УДАЛЕННЫЙ \_ доступ** соответствует разрешению Remote Enable на вкладке Безопасность элемента управления WMI.</span><span class="sxs-lookup"><span data-stu-id="021bb-138">**WBEM\_REMOTE\_ACCESS** corresponds to the Remote Enable permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="021bb-139">Требования</span><span class="sxs-lookup"><span data-stu-id="021bb-139">Requirements</span></span>



| <span data-ttu-id="021bb-140">Требование</span><span class="sxs-lookup"><span data-stu-id="021bb-140">Requirement</span></span> | <span data-ttu-id="021bb-141">Значение</span><span class="sxs-lookup"><span data-stu-id="021bb-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="021bb-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="021bb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="021bb-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="021bb-143">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="021bb-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="021bb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="021bb-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="021bb-145">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="021bb-146">Header</span><span class="sxs-lookup"><span data-stu-id="021bb-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="021bb-147"><dt>Вбемкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="021bb-147"><dt>Wbemcli.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="021bb-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="021bb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021bb-149">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="021bb-149">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="021bb-150">Защита пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="021bb-150">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="021bb-151">Доступ к пространствам имен WMI</span><span class="sxs-lookup"><span data-stu-id="021bb-151">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="021bb-152">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="021bb-152">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="021bb-153">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="021bb-153">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

