---
description: Собственные разрешения API WiFi
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Собственные разрешения API WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afafec7619e0920a17e3769a430c8c79aeff3828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264379"
---
# <a name="native-wifi-api-permissions"></a><span data-ttu-id="afddb-103">Собственные разрешения API WiFi</span><span class="sxs-lookup"><span data-stu-id="afddb-103">Native Wifi API Permissions</span></span>

<span data-ttu-id="afddb-104">Неуправляемый вызов API WiFi может завершиться ошибкой, если вызывающий объект не имеет достаточных разрешений для выполнения запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="afddb-104">A Native Wifi API call may fail with when a caller does not have adequate permissions to perform the requested operation.</span></span>

<span data-ttu-id="afddb-105">Разрешения хранятся в [списках управления доступом на уровне пользователей (DACL)](../secauthz/access-control-lists.md) , связанных с [**\_ защищаемым \_ объектом WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span><span class="sxs-lookup"><span data-stu-id="afddb-105">Permissions are stored in a [discretionary access control lists (DACL)](../secauthz/access-control-lists.md) associated with a [**WLAN\_SECURABLE\_OBJECT**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span></span> <span data-ttu-id="afddb-106">Дополнительные сведения о DACL и защищаемых объектах см. [в статье Управление доступом к объекту в DACL](../secauthz/how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="afddb-106">For more information about DACLs and securable objects, see [How DACLs Control Access to an Object](../secauthz/how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="afddb-107">В следующей таблице показаны собственные функции WiFi, использующие защищаемые объекты для определения наличия у вызывающего объекта достаточных разрешений для выполнения запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="afddb-107">The following table shows the Native Wifi functions that use securable objects to determine if the caller has sufficient permissions to perform the requested operation.</span></span> <span data-ttu-id="afddb-108">В нем также показаны защищаемые объекты, используемые каждой функцией.</span><span class="sxs-lookup"><span data-stu-id="afddb-108">It also shows the securable objects used by each function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="afddb-109">Функция</span><span class="sxs-lookup"><span data-stu-id="afddb-109">Function</span></span></th>
<th><span data-ttu-id="afddb-110">Защищаемый объект</span><span class="sxs-lookup"><span data-stu-id="afddb-110">Securable object</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="afddb-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>Вланжетфилтерлист</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>влансетфилтерлист</strong></a></span><span class="sxs-lookup"><span data-stu-id="afddb-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"><strong>WlanSetFilterList</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="afddb-112">wlan_secure_deny_list</span><span class="sxs-lookup"><span data-stu-id="afddb-112">wlan_secure_deny_list</span></span></li>
<li><span data-ttu-id="afddb-113">wlan_secure_permit_list</span><span class="sxs-lookup"><span data-stu-id="afddb-113">wlan_secure_permit_list</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afddb-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>вланихвконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="afddb-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="afddb-115">wlan_secure_ihv_control</span><span class="sxs-lookup"><span data-stu-id="afddb-115">wlan_secure_ihv_control</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="afddb-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>Вланкуеряутоконфигпараметер</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>влансетаутоконфигпараметер</strong></a></span><span class="sxs-lookup"><span data-stu-id="afddb-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"><strong>WlanSetAutoConfigParameter</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="afddb-117">wlan_secure_show_denied</span><span class="sxs-lookup"><span data-stu-id="afddb-117">wlan_secure_show_denied</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afddb-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>Вланкуеринтерфаце</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>влансетинтерфаце</strong></a></span><span class="sxs-lookup"><span data-stu-id="afddb-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"><strong>WlanSetInterface</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="afddb-119">wlan_secure_ac_enabled</span><span class="sxs-lookup"><span data-stu-id="afddb-119">wlan_secure_ac_enabled</span></span></li>
<li><span data-ttu-id="afddb-120">wlan_secure_bc_scan_enabled</span><span class="sxs-lookup"><span data-stu-id="afddb-120">wlan_secure_bc_scan_enabled</span></span></li>
<li><span data-ttu-id="afddb-121">wlan_secure_bss_type</span><span class="sxs-lookup"><span data-stu-id="afddb-121">wlan_secure_bss_type</span></span></li>
<li><span data-ttu-id="afddb-122">wlan_secure_current_operation_mode</span><span class="sxs-lookup"><span data-stu-id="afddb-122">wlan_secure_current_operation_mode</span></span></li>
<li><span data-ttu-id="afddb-123">wlan_secure_interface_properties</span><span class="sxs-lookup"><span data-stu-id="afddb-123">wlan_secure_interface_properties</span></span></li>
<li><span data-ttu-id="afddb-124">wlan_secure_media_streaming_mode_enabled</span><span class="sxs-lookup"><span data-stu-id="afddb-124">wlan_secure_media_streaming_mode_enabled</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="afddb-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>влансетпрофиле</strong></a></span><span class="sxs-lookup"><span data-stu-id="afddb-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="afddb-126">wlan_secure_add_new_all_user_profiles</span><span class="sxs-lookup"><span data-stu-id="afddb-126">wlan_secure_add_new_all_user_profiles</span></span></li>
<li><span data-ttu-id="afddb-127">wlan_secure_add_new_per_user_profiles</span><span class="sxs-lookup"><span data-stu-id="afddb-127">wlan_secure_add_new_per_user_profiles</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afddb-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>Влансетпрофилелист</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>влансетпрофилепоситион</strong></a></span><span class="sxs-lookup"><span data-stu-id="afddb-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"><strong>WlanSetProfilePosition</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="afddb-129">wlan_secure_all_user_profiles_order</span><span class="sxs-lookup"><span data-stu-id="afddb-129">wlan_secure_all_user_profiles_order</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="afddb-130">Прежде чем одна из указанных выше функций завершит свою работу, она получает список DACL, хранящийся в соответствующем защищаемом объекте.</span><span class="sxs-lookup"><span data-stu-id="afddb-130">Before one of the above-named functions completes its operation, the function retrieves the DACL stored in the appropriate securable object.</span></span> <span data-ttu-id="afddb-131">Затем функция проверяет DACL, чтобы узнать, достаточно ли у вызывающего объекта разрешений.</span><span class="sxs-lookup"><span data-stu-id="afddb-131">The function then checks the DACL to see if the caller has sufficient permissions.</span></span> <span data-ttu-id="afddb-132">Для \* функций вланжет и вланкуери \* требуется, чтобы список DACL содержал [запись управления доступом (ACE)](../secauthz/access-control-entries.md) , которая предоставляет [маркер доступа](../secauthz/access-tokens.md) вызывающему потоку \_ доступ на чтение \_ для функции WLAN.</span><span class="sxs-lookup"><span data-stu-id="afddb-132">The WlanGet\* and WlanQuery\* functions require that the DACL contains an [access control entry (ACE)](../secauthz/access-control-entries.md) that grants the [access token](../secauthz/access-tokens.md) of the calling thread WLAN\_READ\_ACCESS to the function.</span></span> <span data-ttu-id="afddb-133">\*Функциям набора WLAN требуется ACE, который предоставляет маркер доступа для доступа на запись WLAN вызывающего потока \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="afddb-133">The WlanSet\* functions require an ACE that grants the access token of the calling thread WLAN\_WRITE\_ACCESS.</span></span> <span data-ttu-id="afddb-134">Если вызывающий объект не имеет достаточных разрешений, вызов функции завершится ошибкой с ошибкой " \_ доступ \_ запрещен".</span><span class="sxs-lookup"><span data-stu-id="afddb-134">If the caller does not have sufficient permissions, the function call fails with the error ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="afddb-135">С каждым защищаемым объектом связан список DACL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="afddb-135">Each securable object has a DACL associated with it by default.</span></span> <span data-ttu-id="afddb-136">Разрешения по умолчанию, хранящиеся в списке DACL, можно изменить с помощью функции [**влансетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) .</span><span class="sxs-lookup"><span data-stu-id="afddb-136">The default permissions stored in the DACL can be changed using the [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) function.</span></span> <span data-ttu-id="afddb-137">Чтобы определить действующие права пользователя, необходимые для выполнения операции в определенной системе, вызовите [**вланжетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="afddb-137">To determine the effective user rights required to perform an operation on a particular system, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="afddb-138">Профили всех пользователей имеют дополнительные разрешения, связанные с самим профилем.</span><span class="sxs-lookup"><span data-stu-id="afddb-138">All-user profiles have additional permissions associated with the profile itself.</span></span> <span data-ttu-id="afddb-139">Разрешения для профиля "все пользователи" устанавливаются при создании или изменении профиля с помощью [**влансетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) или [**влансаветемпорарипрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span><span class="sxs-lookup"><span data-stu-id="afddb-139">The permissions on an all-user profile are established when the profile is created or modified using [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) or [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span></span> <span data-ttu-id="afddb-140">Параметр *страллусерпрофилесекурити* указывает необходимые разрешения для изменения профиля, удаления профиля или подключения к сети с помощью профиля.</span><span class="sxs-lookup"><span data-stu-id="afddb-140">The *strAllUserProfileSecurity* parameter specifies the required permissions for modifying a profile, deleting a profile, or connecting to a network using a profile.</span></span> <span data-ttu-id="afddb-141">Для удаления или изменения профиля требуется \_ разрешение на запись WLAN \_ .</span><span class="sxs-lookup"><span data-stu-id="afddb-141">Deleting or modifying a profile requires WLAN\_WRITE\_ACCESS permission.</span></span> <span data-ttu-id="afddb-142">Для подключения к сети, использующей профиль, требуется разрешение на выполнение беспроводной сети \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="afddb-142">Connecting to a network using a profile requires WLAN\_EXECUTE\_ACCESS permission.</span></span>

<span data-ttu-id="afddb-143">\* \* Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2): \* \* функции [**вланжетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) и [**влансетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="afddb-143">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* The [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) and [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) functions are not supported.</span></span> <span data-ttu-id="afddb-144">Параметр *страллусерпрофилесекурити* не используется.</span><span class="sxs-lookup"><span data-stu-id="afddb-144">The *strAllUserProfileSecurity* parameter is not used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afddb-145">См. также</span><span class="sxs-lookup"><span data-stu-id="afddb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afddb-146">Управление доступом к объекту с помощью списков DACL</span><span class="sxs-lookup"><span data-stu-id="afddb-146">How DACLs Control Access to an Object</span></span>](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="afddb-147">**\_защищаемый \_ объект WLAN**</span><span class="sxs-lookup"><span data-stu-id="afddb-147">**WLAN\_SECURABLE\_OBJECT**</span></span>](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
