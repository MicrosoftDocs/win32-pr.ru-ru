---
title: Безопасность настольных систем и права доступа
description: Безопасность позволяет управлять доступом к объектам настольных систем. Дополнительные сведения о безопасности см. в разделе Модель Access-Control.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413284"
---
# <a name="desktop-security-and-access-rights"></a><span data-ttu-id="6efef-104">Безопасность настольных систем и права доступа</span><span class="sxs-lookup"><span data-stu-id="6efef-104">Desktop Security and Access Rights</span></span>

<span data-ttu-id="6efef-105">Безопасность позволяет управлять доступом к объектам настольных систем.</span><span class="sxs-lookup"><span data-stu-id="6efef-105">Security enables you to control access to desktop objects.</span></span> <span data-ttu-id="6efef-106">Дополнительные сведения о безопасности см. в разделе [модель управления доступом](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="6efef-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="6efef-107">При вызове функции [**креатедесктоп**](/windows/win32/api/winuser/nf-winuser-createdesktopa) или [**креатедесктопекс**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) можно указать [дескриптор безопасности](/windows/desktop/SecAuthZ/security-descriptors) для объекта Desktop.</span><span class="sxs-lookup"><span data-stu-id="6efef-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a desktop object when you call the [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function.</span></span> <span data-ttu-id="6efef-108">Если указано значение NULL, Рабочий стол получает дескриптор безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6efef-108">If you specify NULL, the desktop gets a default security descriptor.</span></span> <span data-ttu-id="6efef-109">Списки ACL в дескрипторе безопасности рабочего стола по умолчанию поступают от его родительской станции.</span><span class="sxs-lookup"><span data-stu-id="6efef-109">The ACLs in the default security descriptor for a desktop come from its parent window station.</span></span>

<span data-ttu-id="6efef-110">Чтобы получить или задать дескриптор безопасности объекта Windows Station, вызовите функции [**жетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) и [**сетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="6efef-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="6efef-111">При вызове функции [**опендесктоп**](/windows/win32/api/winuser/nf-winuser-opendesktopa) или [**опенинпутдесктоп**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) система проверяет запрошенные права доступа к дескриптору безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="6efef-111">When you call the [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) or [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="6efef-112">Допустимые права доступа для объектов рабочего стола включают [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights) и некоторые права доступа для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="6efef-112">The valid access rights for desktop objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="6efef-113">В следующей таблице перечислены стандартные права доступа, используемые всеми объектами.</span><span class="sxs-lookup"><span data-stu-id="6efef-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="6efef-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6efef-114">Value</span></span>                       | <span data-ttu-id="6efef-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6efef-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6efef-116">DELETE (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="6efef-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="6efef-117">Требуется для удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="6efef-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="6efef-118">\_Управление чтением (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="6efef-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="6efef-119">Требуется для чтения сведений в дескрипторе безопасности объекта, не включая сведения из списка SACL.</span><span class="sxs-lookup"><span data-stu-id="6efef-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="6efef-120">Для чтения или записи списка SACL необходимо запросить право доступа к \_ системе безопасности системы доступа \_ .</span><span class="sxs-lookup"><span data-stu-id="6efef-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="6efef-121">Дополнительные сведения см. в статье [право доступа к SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="6efef-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="6efef-122">Синхронизация (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="6efef-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="6efef-123">Не поддерживается для объектов настольных систем.</span><span class="sxs-lookup"><span data-stu-id="6efef-123">Not supported for desktop objects.</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="6efef-124">ЗАПИСЬ \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="6efef-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="6efef-125">Требуется для изменения списка DACL в дескрипторе безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="6efef-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="6efef-126">\_Владелец записи (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="6efef-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="6efef-127">Требуется для изменения владельца в дескрипторе безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="6efef-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="6efef-128">В следующей таблице перечислены права доступа для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="6efef-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="6efef-129">Право доступа</span><span class="sxs-lookup"><span data-stu-id="6efef-129">Access right</span></span>                       | <span data-ttu-id="6efef-130">Описание</span><span class="sxs-lookup"><span data-stu-id="6efef-130">Description</span></span>                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6efef-131">DESKTOP \_ креатемену (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="6efef-131">DESKTOP\_CREATEMENU (0x0004L)</span></span>      | <span data-ttu-id="6efef-132">Требуется для создания меню на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="6efef-132">Required to create a menu on the desktop.</span></span>                                                   |
| <span data-ttu-id="6efef-133">DESKTOP \_ CREATEWINDOW (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="6efef-133">DESKTOP\_CREATEWINDOW (0x0002L)</span></span>    | <span data-ttu-id="6efef-134">Требуется для создания окна на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="6efef-134">Required to create a window on the desktop.</span></span>                                                 |
| <span data-ttu-id="6efef-135">\_Перечисление Desktop (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="6efef-135">DESKTOP\_ENUMERATE (0x0040L)</span></span>       | <span data-ttu-id="6efef-136">Требуется для перечисления рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="6efef-136">Required for the desktop to be enumerated.</span></span>                                                  |
| <span data-ttu-id="6efef-137">DESKTOP \_ хукконтрол (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="6efef-137">DESKTOP\_HOOKCONTROL (0x0008L)</span></span>     | <span data-ttu-id="6efef-138">Требуется для установки любого обработчика окна.</span><span class="sxs-lookup"><span data-stu-id="6efef-138">Required to establish any of the window hooks.</span></span>                                              |
| <span data-ttu-id="6efef-139">DESKTOP \_ жаурналплайбакк (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="6efef-139">DESKTOP\_JOURNALPLAYBACK (0x0020L)</span></span> | <span data-ttu-id="6efef-140">Требуется для выполнения воспроизведения журнала на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="6efef-140">Required to perform journal playback on a desktop.</span></span>                                          |
| <span data-ttu-id="6efef-141">DESKTOP \_ жаурналрекорд (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="6efef-141">DESKTOP\_JOURNALRECORD (0x0010L)</span></span>   | <span data-ttu-id="6efef-142">Требуется для выполнения записи журнала на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="6efef-142">Required to perform journal recording on a desktop.</span></span>                                         |
| <span data-ttu-id="6efef-143">DESKTOP \_ READOBJECTS (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="6efef-143">DESKTOP\_READOBJECTS (0x0001L)</span></span>     | <span data-ttu-id="6efef-144">Требуется для чтения объектов на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="6efef-144">Required to read objects on the desktop.</span></span>                                                    |
| <span data-ttu-id="6efef-145">DESKTOP \_ свитчдесктоп (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="6efef-145">DESKTOP\_SWITCHDESKTOP (0x0100L)</span></span>   | <span data-ttu-id="6efef-146">Требуется для активации рабочего стола с помощью функции [**свитчдесктоп**](/windows/win32/api/winuser/nf-winuser-switchdesktop) .</span><span class="sxs-lookup"><span data-stu-id="6efef-146">Required to activate the desktop using the [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) function.</span></span> |
| <span data-ttu-id="6efef-147">DESKTOP \_ вритеобжектс (0x0080L)</span><span class="sxs-lookup"><span data-stu-id="6efef-147">DESKTOP\_WRITEOBJECTS (0x0080L)</span></span>    | <span data-ttu-id="6efef-148">Требуется для записи объектов на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="6efef-148">Required to write objects on the desktop.</span></span>                                                   |



 

<span data-ttu-id="6efef-149">Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для объекта Desktop, содержащегося в интерактивной рабочей станции сеанса входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="6efef-149">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a desktop object contained in the interactive window station of the user's logon session.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6efef-150">Право доступа</span><span class="sxs-lookup"><span data-stu-id="6efef-150">Access right</span></span></th>
<th><span data-ttu-id="6efef-151">Описание</span><span class="sxs-lookup"><span data-stu-id="6efef-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6efef-152">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="6efef-152">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="6efef-153">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="6efef-153">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="6efef-154">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6efef-154">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="6efef-155">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="6efef-155">STANDARD_RIGHTS_READ</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6efef-156">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="6efef-156">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="6efef-157">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="6efef-157">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="6efef-158">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="6efef-158">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="6efef-159">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="6efef-159">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="6efef-160">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="6efef-160">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="6efef-161">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="6efef-161">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="6efef-162">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6efef-162">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="6efef-163">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="6efef-163">STANDARD_RIGHTS_WRITE</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6efef-164">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="6efef-164">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="6efef-165">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="6efef-165">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="6efef-166">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="6efef-166">STANDARD_RIGHTS_EXECUTE</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6efef-167">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="6efef-167">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="6efef-168">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="6efef-168">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="6efef-169">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="6efef-169">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="6efef-170">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="6efef-170">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="6efef-171">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="6efef-171">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="6efef-172">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="6efef-172">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="6efef-173">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="6efef-173">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="6efef-174">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6efef-174">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="6efef-175">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="6efef-175">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="6efef-176">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6efef-176">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="6efef-177">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="6efef-177">STANDARD_RIGHTS_REQUIRED</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6efef-178">Можно запросить \_ право доступа к системе \_ безопасности системы доступа к объекту рабочего стола, если вы хотите прочитать или записать список SACL объекта.</span><span class="sxs-lookup"><span data-stu-id="6efef-178">You can request the ACCESS\_SYSTEM\_SECURITY access right to a desktop object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="6efef-179">Дополнительные сведения см. в разделе [списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) и [права доступа к спискам SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="6efef-179">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 