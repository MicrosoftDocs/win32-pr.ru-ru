---
title: Права доступа и безопасность оконной станции
description: Безопасность позволяет управлять доступом к объектам Windows Station. Дополнительные сведения о безопасности см. в разделе Модель Access-Control.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710291"
---
# <a name="window-station-security-and-access-rights"></a><span data-ttu-id="71f99-104">Права доступа и безопасность оконной станции</span><span class="sxs-lookup"><span data-stu-id="71f99-104">Window Station Security and Access Rights</span></span>

<span data-ttu-id="71f99-105">Безопасность позволяет управлять доступом к объектам Windows Station.</span><span class="sxs-lookup"><span data-stu-id="71f99-105">Security enables you to control access to window station objects.</span></span> <span data-ttu-id="71f99-106">Дополнительные сведения о безопасности см. в разделе [модель управления доступом](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="71f99-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="71f99-107">При вызове функции [**креатевиндовстатион**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) можно указать [дескриптор безопасности](/windows/desktop/SecAuthZ/security-descriptors) для объекта Windows Station.</span><span class="sxs-lookup"><span data-stu-id="71f99-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a window station object when you call the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function.</span></span> <span data-ttu-id="71f99-108">При указании значения NULL станция окна получает дескриптор безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71f99-108">If you specify NULL, the window station gets a default security descriptor.</span></span> <span data-ttu-id="71f99-109">Списки ACL в дескрипторе безопасности по умолчанию для станции Windows поступают из основного маркера или токена олицетворения создателя.</span><span class="sxs-lookup"><span data-stu-id="71f99-109">The ACLs in the default security descriptor for a window station come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="71f99-110">Чтобы получить или задать дескриптор безопасности объекта Windows Station, вызовите функции [**жетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) и [**сетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="71f99-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="71f99-111">При вызове функции [**опенвиндовстатион**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) система проверяет запрошенные права доступа к дескриптору безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="71f99-111">When you call the [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="71f99-112">Допустимые права доступа для объектов Windows Station включают [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights) и некоторые права доступа для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="71f99-112">The valid access rights for window station objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="71f99-113">В следующей таблице перечислены стандартные права доступа, используемые всеми объектами.</span><span class="sxs-lookup"><span data-stu-id="71f99-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="71f99-114">Значение</span><span class="sxs-lookup"><span data-stu-id="71f99-114">Value</span></span>                       | <span data-ttu-id="71f99-115">Значение</span><span class="sxs-lookup"><span data-stu-id="71f99-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f99-116">DELETE (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="71f99-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="71f99-117">Требуется для удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="71f99-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="71f99-118">\_Управление чтением (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="71f99-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="71f99-119">Требуется для чтения сведений в дескрипторе безопасности объекта, не включая сведения из списка SACL.</span><span class="sxs-lookup"><span data-stu-id="71f99-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="71f99-120">Для чтения или записи списка SACL необходимо запросить право доступа к \_ системе безопасности системы доступа \_ .</span><span class="sxs-lookup"><span data-stu-id="71f99-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="71f99-121">Дополнительные сведения см. в статье [право доступа к SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="71f99-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="71f99-122">Синхронизация (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="71f99-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="71f99-123">Не поддерживается для объектов оконной станции.</span><span class="sxs-lookup"><span data-stu-id="71f99-123">Not supported for window station objects.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="71f99-124">ЗАПИСЬ \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="71f99-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="71f99-125">Требуется для изменения списка DACL в дескрипторе безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="71f99-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="71f99-126">\_Владелец записи (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="71f99-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="71f99-127">Требуется для изменения владельца в дескрипторе безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="71f99-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="71f99-128">В следующей таблице перечислены права доступа для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="71f99-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="71f99-129">Право доступа</span><span class="sxs-lookup"><span data-stu-id="71f99-129">Access right</span></span>                        | <span data-ttu-id="71f99-130">Описание</span><span class="sxs-lookup"><span data-stu-id="71f99-130">Description</span></span>                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f99-131">ВИНСТА \_ все \_ доступ (0x37F)</span><span class="sxs-lookup"><span data-stu-id="71f99-131">WINSTA\_ALL\_ACCESS (0x37F)</span></span>         | <span data-ttu-id="71f99-132">Все возможные права доступа для станции Windows.</span><span class="sxs-lookup"><span data-stu-id="71f99-132">All possible access rights for the window station.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="71f99-133">ВИНСТА \_ акцессклипбоард (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="71f99-133">WINSTA\_ACCESSCLIPBOARD (0x0004L)</span></span>   | <span data-ttu-id="71f99-134">Требуется для использования буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="71f99-134">Required to use the clipboard.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="71f99-135">ВИНСТА \_ акцессглобалатомс (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="71f99-135">WINSTA\_ACCESSGLOBALATOMS (0x0020L)</span></span> | <span data-ttu-id="71f99-136">Требуется для управления глобальными атомами.</span><span class="sxs-lookup"><span data-stu-id="71f99-136">Required to manipulate global atoms.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="71f99-137">ВИНСТА \_ креатедесктоп (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="71f99-137">WINSTA\_CREATEDESKTOP (0x0008L)</span></span>     | <span data-ttu-id="71f99-138">Требуется для создания новых объектов рабочего стола на станции Windows.</span><span class="sxs-lookup"><span data-stu-id="71f99-138">Required to create new desktop objects on the window station.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="71f99-139">ВИНСТА \_ енумдесктопс (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="71f99-139">WINSTA\_ENUMDESKTOPS (0x0001L)</span></span>      | <span data-ttu-id="71f99-140">Требуется для перечисления существующих объектов Desktop.</span><span class="sxs-lookup"><span data-stu-id="71f99-140">Required to enumerate existing desktop objects.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="71f99-141">\_Перечисление винста (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="71f99-141">WINSTA\_ENUMERATE (0x0100L)</span></span>         | <span data-ttu-id="71f99-142">Требуется для перечисления станции окон.</span><span class="sxs-lookup"><span data-stu-id="71f99-142">Required for the window station to be enumerated.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="71f99-143">ВИНСТА \_ екситвиндовс (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="71f99-143">WINSTA\_EXITWINDOWS (0x0040L)</span></span>       | <span data-ttu-id="71f99-144">Требуется для успешного вызова функции [**екситвиндовс**](/windows/desktop/api/winuser/nf-winuser-exitwindows) или [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="71f99-144">Required to successfully call the [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span> <span data-ttu-id="71f99-145">Windows-станции могут совместно использоваться пользователями, а этот тип доступа может препятствовать выходу из системы владельца Windows-станции другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="71f99-145">Window stations can be shared by users and this access type can prevent other users of a window station from logging off the window station owner.</span></span> |
| <span data-ttu-id="71f99-146">ВИНСТА \_ реадаттрибутес (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="71f99-146">WINSTA\_READATTRIBUTES (0x0002L)</span></span>    | <span data-ttu-id="71f99-147">Требуется для чтения атрибутов объекта Windows Station.</span><span class="sxs-lookup"><span data-stu-id="71f99-147">Required to read the attributes of a window station object.</span></span> <span data-ttu-id="71f99-148">Этот атрибут включает параметры цвета и другие глобальные свойства Windows Station.</span><span class="sxs-lookup"><span data-stu-id="71f99-148">This attribute includes color settings and other global window station properties.</span></span>                                                                                                                                |
| <span data-ttu-id="71f99-149">ВИНСТА \_ реадскрин (0x0200L)</span><span class="sxs-lookup"><span data-stu-id="71f99-149">WINSTA\_READSCREEN (0x0200L)</span></span>        | <span data-ttu-id="71f99-150">Требуется для доступа к содержимому экрана.</span><span class="sxs-lookup"><span data-stu-id="71f99-150">Required to access screen contents.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="71f99-151">ВИНСТА \_ вритеаттрибутес (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="71f99-151">WINSTA\_WRITEATTRIBUTES (0x0010L)</span></span>   | <span data-ttu-id="71f99-152">Требуется для изменения атрибутов объекта Windows Station.</span><span class="sxs-lookup"><span data-stu-id="71f99-152">Required to modify the attributes of a window station object.</span></span> <span data-ttu-id="71f99-153">Атрибуты включают параметры цвета и другие глобальные свойства Windows Station.</span><span class="sxs-lookup"><span data-stu-id="71f99-153">The attributes include color settings and other global window station properties.</span></span>                                                                                                                               |



 

<span data-ttu-id="71f99-154">Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для объекта интерактивной рабочей станции, который является станцией окна, назначенной сеансу входа текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="71f99-154">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the interactive window station object, which is the window station assigned to the logon session of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="71f99-155">Право доступа</span><span class="sxs-lookup"><span data-stu-id="71f99-155">Access right</span></span></th>
<th><span data-ttu-id="71f99-156">Описание</span><span class="sxs-lookup"><span data-stu-id="71f99-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71f99-157">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="71f99-157">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="71f99-158">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="71f99-158">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="71f99-159">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="71f99-159">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="71f99-160">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="71f99-160">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="71f99-161">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="71f99-161">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="71f99-162">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="71f99-162">WINSTA_READSCREEN</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f99-163">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="71f99-163">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="71f99-164">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="71f99-164">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="71f99-165">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="71f99-165">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="71f99-166">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="71f99-166">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="71f99-167">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="71f99-167">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f99-168">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="71f99-168">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="71f99-169">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="71f99-169">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="71f99-170">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="71f99-170">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="71f99-171">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="71f99-171">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f99-172">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="71f99-172">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="71f99-173">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="71f99-173">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="71f99-174">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="71f99-174">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="71f99-175">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="71f99-175">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="71f99-176">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="71f99-176">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="71f99-177">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="71f99-177">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="71f99-178">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="71f99-178">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="71f99-179">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="71f99-179">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="71f99-180">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="71f99-180">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="71f99-181">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="71f99-181">WINSTA_READSCREEN</span></span><br />
<span data-ttu-id="71f99-182">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="71f99-182">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="71f99-183">Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для неинтерактивного объекта Windows Station.</span><span class="sxs-lookup"><span data-stu-id="71f99-183">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a noninteractive window station object.</span></span> <span data-ttu-id="71f99-184">Система назначает неинтерактивные станции окон всем сеансам входа, кроме текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="71f99-184">The system assigns noninteractive window stations to all logon sessions other than that of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="71f99-185">Право доступа</span><span class="sxs-lookup"><span data-stu-id="71f99-185">Access right</span></span></th>
<th><span data-ttu-id="71f99-186">Описание</span><span class="sxs-lookup"><span data-stu-id="71f99-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71f99-187">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="71f99-187">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="71f99-188">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="71f99-188">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="71f99-189">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="71f99-189">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="71f99-190">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="71f99-190">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="71f99-191">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="71f99-191">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f99-192">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="71f99-192">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="71f99-193">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="71f99-193">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="71f99-194">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="71f99-194">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="71f99-195">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="71f99-195">WINSTA_CREATEDESKTOP</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f99-196">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="71f99-196">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="71f99-197">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="71f99-197">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="71f99-198">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="71f99-198">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="71f99-199">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="71f99-199">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f99-200">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="71f99-200">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="71f99-201">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="71f99-201">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="71f99-202">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="71f99-202">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="71f99-203">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="71f99-203">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="71f99-204">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="71f99-204">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="71f99-205">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="71f99-205">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="71f99-206">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="71f99-206">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="71f99-207">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="71f99-207">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="71f99-208">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="71f99-208">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="71f99-209">Вы можете запросить право доступа к \_ системе безопасности системы доступа \_ к объекту Windows Station, если хотите прочитать или записать список SACL объекта.</span><span class="sxs-lookup"><span data-stu-id="71f99-209">You can request the ACCESS\_SYSTEM\_SECURITY access right to a window station object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="71f99-210">Дополнительные сведения см. в разделе [списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) и [права доступа к спискам SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="71f99-210">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 