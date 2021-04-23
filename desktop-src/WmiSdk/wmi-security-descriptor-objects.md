---
description: Инструментарий WMI содержит объекты и методы, позволяющие считывать дескрипторы безопасности и управлять ими, чтобы определить, кто имеет доступ к защищаемым объектам.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Объекты дескрипторов безопасности WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568000"
---
# <a name="wmi-security-descriptor-objects"></a><span data-ttu-id="aa67b-103">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="aa67b-103">WMI Security Descriptor Objects</span></span>

<span data-ttu-id="aa67b-104">Инструментарий WMI содержит объекты и методы, позволяющие считывать дескрипторы безопасности и управлять ими, чтобы определить, кто имеет доступ к защищаемым объектам.</span><span class="sxs-lookup"><span data-stu-id="aa67b-104">WMI has objects and methods that allow you to read and manipulate security descriptors to determine who has access to securable objects.</span></span>

-   [<span data-ttu-id="aa67b-105">Роль дескрипторов безопасности</span><span class="sxs-lookup"><span data-stu-id="aa67b-105">The Role of Security Descriptors</span></span>](#the-role-of-security-descriptors)
-   [<span data-ttu-id="aa67b-106">Управление доступом и объекты безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="aa67b-106">Access Control and WMI Security Objects</span></span>](#access-control-and-wmi-security-objects)
-   [<span data-ttu-id="aa67b-107">\_Объект Win32 SecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="aa67b-107">Win32\_SecurityDescriptor Object</span></span>](/windows)
-   [<span data-ttu-id="aa67b-108">Списки DACL и SACL</span><span class="sxs-lookup"><span data-stu-id="aa67b-108">DACL and SACL</span></span>](#dacl-and-sacl)
-   [<span data-ttu-id="aa67b-109">\_ACE Win32, \_ доверенное лицо Win32, \_ идентификатор безопасности Win32</span><span class="sxs-lookup"><span data-stu-id="aa67b-109">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>](/windows)
-   [<span data-ttu-id="aa67b-110">Пример: Проверка доступа к принтерам</span><span class="sxs-lookup"><span data-stu-id="aa67b-110">Example: Checking Who has Access to Printers</span></span>](#example-checking-who-has-access-to-printers)
-   [<span data-ttu-id="aa67b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="aa67b-111">Related topics</span></span>](#related-topics)

## <a name="the-role-of-security-descriptors"></a><span data-ttu-id="aa67b-112">Роль дескрипторов безопасности</span><span class="sxs-lookup"><span data-stu-id="aa67b-112">The Role of Security Descriptors</span></span>

<span data-ttu-id="aa67b-113">Дескрипторы безопасности определяют атрибуты безопасности защищаемых объектов, таких как файлы, разделы реестра, пространства имен WMI, принтеры, службы или общие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aa67b-113">Security descriptors define the security attributes of securable objects such as files, registry keys, WMI namespaces, printers, services, or shares.</span></span> <span data-ttu-id="aa67b-114">Дескриптор безопасности содержит сведения о владельце и основной группе объекта.</span><span class="sxs-lookup"><span data-stu-id="aa67b-114">A security descriptor contains information about the owner and primary group of an object.</span></span> <span data-ttu-id="aa67b-115">Поставщик может сравнить дескриптор безопасности ресурса с удостоверением запрашивающего пользователя и определить, имеет ли пользователь право на доступ к ресурсу, запрашиваемому пользователем.</span><span class="sxs-lookup"><span data-stu-id="aa67b-115">A provider can compare the resource security descriptor to the identity of a requesting user, and determine whether or not the user has the right to access the resource that a user is requesting.</span></span> <span data-ttu-id="aa67b-116">Дополнительные сведения см. [в разделе доступ к защищаемым ОБЪЕКТАМ WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="aa67b-116">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="aa67b-117">Некоторые методы WMI, например [**Получение**](--systemsecurity-getsd.md), возвращают дескриптор безопасности в двоичном формате байтового массива.</span><span class="sxs-lookup"><span data-stu-id="aa67b-117">Some WMI methods, such as [**GetSD**](--systemsecurity-getsd.md), return a security descriptor in the binary byte array format.</span></span> <span data-ttu-id="aa67b-118">Начиная с Windows Vista, используйте методы класса [**Win32 \_ секуритидескрипторхелпер**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) для преобразования двоичного дескриптора безопасности в экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), который можно легко манипулировать.</span><span class="sxs-lookup"><span data-stu-id="aa67b-118">Starting with Windows Vista, use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to convert a binary security descriptor to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), which can be manipulated more easily.</span></span> <span data-ttu-id="aa67b-119">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="aa67b-119">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="access-control-and-wmi-security-objects"></a><span data-ttu-id="aa67b-120">Управление доступом и объекты безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="aa67b-120">Access Control and WMI Security Objects</span></span>

<span data-ttu-id="aa67b-121">Ниже приведен список объектов безопасности WMI.</span><span class="sxs-lookup"><span data-stu-id="aa67b-121">The following is a list of WMI security objects:</span></span>

-   [<span data-ttu-id="aa67b-122">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="aa67b-122">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [<span data-ttu-id="aa67b-123">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="aa67b-123">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [<span data-ttu-id="aa67b-124">**\_Доверенное лицо Win32**</span><span class="sxs-lookup"><span data-stu-id="aa67b-124">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [<span data-ttu-id="aa67b-125">**\_Идентификатор безопасности Win32**</span><span class="sxs-lookup"><span data-stu-id="aa67b-125">**Win32\_SID**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

<span data-ttu-id="aa67b-126">На следующей схеме показаны связи между объектами безопасности WMI.</span><span class="sxs-lookup"><span data-stu-id="aa67b-126">The following diagram shows the relationships among WMI security objects.</span></span>

![отношения между объектами безопасности WMI](images/security-descriptor.png)

<span data-ttu-id="aa67b-128">Дополнительные сведения о роли безопасности доступа см. в разделе [рекомендации по обеспечению безопасности](/windows/desktop/SecBP/best-practices-for-the-security-apis), [обеспечению безопасности WMI](maintaining-wmi-security.md)и [контролю доступа](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="aa67b-128">For more information about the role of access security, see [Security Best Practices](/windows/desktop/SecBP/best-practices-for-the-security-apis), [Maintaining WMI Security](maintaining-wmi-security.md), and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

## <a name="win32_securitydescriptor-object"></a><span data-ttu-id="aa67b-129">\_Объект Win32 SecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="aa67b-129">Win32\_SecurityDescriptor Object</span></span>

<span data-ttu-id="aa67b-130">В следующей таблице перечислены свойства класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="aa67b-130">The following table lists the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class properties.</span></span>



| <span data-ttu-id="aa67b-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="aa67b-131">Property</span></span>         | <span data-ttu-id="aa67b-132">Описание</span><span class="sxs-lookup"><span data-stu-id="aa67b-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa67b-133">**контролфлагс**</span><span class="sxs-lookup"><span data-stu-id="aa67b-133">**ControlFlags**</span></span> | <span data-ttu-id="aa67b-134">Набор контрольных битов, соответствующих значению SD или его отдельным элементам.</span><span class="sxs-lookup"><span data-stu-id="aa67b-134">Set of control bits that qualify the meaning of an SD or its individual members.</span></span> <span data-ttu-id="aa67b-135">Дополнительные сведения о задании значений битов **контролфлагс** см. в разделе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="aa67b-135">For more information about setting the **ControlFlags** bit values, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span><br/>                                                                                                                                                                      |
| <span data-ttu-id="aa67b-136">**КОНТРОЛЯ**</span><span class="sxs-lookup"><span data-stu-id="aa67b-136">**DACL**</span></span>         | <span data-ttu-id="aa67b-137">[Избирательный список управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) для пользователей и групп, а также права доступа к защищенному объекту.</span><span class="sxs-lookup"><span data-stu-id="aa67b-137">[Discretionary Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) of users and groups, and their access rights to a secured object.</span></span> <span data-ttu-id="aa67b-138">Это свойство содержит массив экземпляров [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , которые представляют [записи управления доступом](/windows/desktop/SecAuthZ/access-control-entries).</span><span class="sxs-lookup"><span data-stu-id="aa67b-138">This property contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent [Access Control Entries](/windows/desktop/SecAuthZ/access-control-entries).</span></span> <span data-ttu-id="aa67b-139">Дополнительные сведения см. [в разделе Создание списка DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="aa67b-139">For more information, see [Creating a DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span><br/> |
| <span data-ttu-id="aa67b-140">**Группа**</span><span class="sxs-lookup"><span data-stu-id="aa67b-140">**Group**</span></span>        | <span data-ttu-id="aa67b-141">Группа, к которой принадлежит этот защищенный объект.</span><span class="sxs-lookup"><span data-stu-id="aa67b-141">Group to which this secured object belongs.</span></span> <span data-ttu-id="aa67b-142">Это свойство содержит экземпляр [**\_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , который содержит имя, домен и идентификатор безопасности (SID) группы, которой принадлежит владелец.</span><span class="sxs-lookup"><span data-stu-id="aa67b-142">This property contains an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the group to which the owner belongs.</span></span><br/>                                                                                                                                                             |
| <span data-ttu-id="aa67b-143">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="aa67b-143">**Owner**</span></span>        | <span data-ttu-id="aa67b-144">Владелец защищенного объекта.</span><span class="sxs-lookup"><span data-stu-id="aa67b-144">Owner of this secured object.</span></span> <span data-ttu-id="aa67b-145">Это свойство содержит экземпляр [ \_ доверенного лица Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , который содержит имя, домен и идентификатор безопасности (SID) владельца.</span><span class="sxs-lookup"><span data-stu-id="aa67b-145">This property contains an instance of [Win32\_Trustee](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the owner.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="aa67b-146">**СИСТЕМНЫЙ**</span><span class="sxs-lookup"><span data-stu-id="aa67b-146">**SACL**</span></span>         | <span data-ttu-id="aa67b-147">[Системный список управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) содержит массив экземпляров [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , которые представляют тип попыток доступа, создающих записи аудита для пользователей или групп.</span><span class="sxs-lookup"><span data-stu-id="aa67b-147">[System Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent the type of access attempts that generate audit records for users or groups.</span></span> <span data-ttu-id="aa67b-148">Дополнительные сведения см. [в разделе SACL для нового объекта](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span><span class="sxs-lookup"><span data-stu-id="aa67b-148">For more information, see [SACL for a New Object](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span></span><br/>                                                                        |



 

## <a name="dacl-and-sacl"></a><span data-ttu-id="aa67b-149">Списки DACL и SACL</span><span class="sxs-lookup"><span data-stu-id="aa67b-149">DACL and SACL</span></span>

<span data-ttu-id="aa67b-150">Массивы объектов [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) в списке управления доступом на уровне пользователей (DACL) и системном списке управления доступом (SACL) создают связь между пользователем или группой и их правами доступа.</span><span class="sxs-lookup"><span data-stu-id="aa67b-150">The arrays of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) objects in the discretionary access control list (DACL) and system access control list {SACL) create a link between a user or group and their access rights.</span></span>

<span data-ttu-id="aa67b-151">Если свойство DACL не содержит записи управления доступом (ACE), права доступа не предоставляются и доступ к объекту будет запрещен.</span><span class="sxs-lookup"><span data-stu-id="aa67b-151">When a DACL property does not contain an access control entry (ACE), access rights are not granted and access to the object is denied.</span></span>

> [!Note]  
> <span data-ttu-id="aa67b-152">**Пустой** список DACL предоставляет полный доступ всем, что является серьезной угрозой безопасности.</span><span class="sxs-lookup"><span data-stu-id="aa67b-152">A **NULL** DACL gives full access to everyone, which is a serious security risk.</span></span> <span data-ttu-id="aa67b-153">Дополнительные сведения см. [в разделе Создание списка DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="aa67b-153">For more information, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

## <a name="win32_ace-win32_trustee-win32_sid"></a><span data-ttu-id="aa67b-154">\_ACE Win32, \_ доверенное лицо Win32, \_ идентификатор безопасности Win32</span><span class="sxs-lookup"><span data-stu-id="aa67b-154">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>

<span data-ttu-id="aa67b-155">Объект [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) содержит экземпляр класса [**\_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , который определяет пользователя или группу, и свойство **AccessMask** , которое является битовой маской, указывающей действия, которые может выполнять пользователь или группа.</span><span class="sxs-lookup"><span data-stu-id="aa67b-155">A [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object contains an instance of the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class that identifies a user or group, and an **AccessMask** property that is a bitmask, which specifies the actions that a user or group can take.</span></span> <span data-ttu-id="aa67b-156">Например, пользователю или группе может быть предоставлено право на чтение файла, но не на запись в файл.</span><span class="sxs-lookup"><span data-stu-id="aa67b-156">For example, a user or group might be granted the right to read a file but not write to the file.</span></span> <span data-ttu-id="aa67b-157">Объект **\_ ACE Win32** также содержит запись ACE, которая указывает, является ли это разрешение или запретом доступа.</span><span class="sxs-lookup"><span data-stu-id="aa67b-157">A **Win32\_ACE** object also contains an ACE that indicates whether or not it is an allow or a deny access.</span></span>

> [!Note]  
> <span data-ttu-id="aa67b-158">Порядок элементов [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) в списке DACL важен, так как в списке DACL разрешены и запрещены запись контроля доступа (ACE).</span><span class="sxs-lookup"><span data-stu-id="aa67b-158">The [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) order in a DACL is important because both allow and deny access control entry (ACE) are permitted in a DACL.</span></span> <span data-ttu-id="aa67b-159">Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="aa67b-159">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="aa67b-160">Каждая учетная запись пользователя или группа, представленная [**\_ доверенным лицом Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , имеет идентификатор безопасности (SID), однозначно определяющий учетную запись, и указывает привилегии доступа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="aa67b-160">Each user account or group represented by a [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) has a security identifier (SID) that uniquely identifies an account, and specifies the access privileges of the account.</span></span> <span data-ttu-id="aa67b-161">Определение данных SID зависит от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="aa67b-161">How you specify the SID data depends on the operating system.</span></span> <span data-ttu-id="aa67b-162">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="aa67b-162">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="aa67b-163">На следующей диаграмме показано содержимое одного экземпляра [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="aa67b-163">The following diagram shows the contents of one [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instance.</span></span>

![содержимое одного \- экземпляра ACE Win32](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a><span data-ttu-id="aa67b-165">Пример: Проверка доступа к принтерам</span><span class="sxs-lookup"><span data-stu-id="aa67b-165">Example: Checking Who has Access to Printers</span></span>

<span data-ttu-id="aa67b-166">В следующем примере кода VBScript показано, как использовать дескриптор безопасности принтера.</span><span class="sxs-lookup"><span data-stu-id="aa67b-166">The following VBScript code example shows how to use the printer security descriptor.</span></span> <span data-ttu-id="aa67b-167">Скрипт вызывает метод [**жетсекуритидескриптор**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) в классе [**\_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) для получения дескриптора, а затем определяет, присутствует ли в дескрипторе безопасности список управления доступом на уровне пользователей (DACL).</span><span class="sxs-lookup"><span data-stu-id="aa67b-167">The script calls the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method in the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class to obtain the descriptor then determines if there is a Discretionary Access Control List (DACL) present in the security descriptor.</span></span> <span data-ttu-id="aa67b-168">При наличии списка DACL сценарий получает список записей управления доступом (ACE) из списка DACL.</span><span class="sxs-lookup"><span data-stu-id="aa67b-168">If there is a DACL, then the script obtains the list of Access Control Entries (ACE) from the DACL.</span></span> <span data-ttu-id="aa67b-169">Каждый элемент ACE представлен экземпляром [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span><span class="sxs-lookup"><span data-stu-id="aa67b-169">Each ACE is represented by an instance of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span></span> <span data-ttu-id="aa67b-170">Сценарий проверяет каждый ACE, чтобы получить имя пользователя и определить, имеет ли пользователь доступ к принтеру.</span><span class="sxs-lookup"><span data-stu-id="aa67b-170">The script checks every ACE to get the name of the user and determine whether the user has access to the printer.</span></span> <span data-ttu-id="aa67b-171">Пользователь представлен в экземпляре [**\_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , внедренного в экземпляр **\_ ACE Win32** .</span><span class="sxs-lookup"><span data-stu-id="aa67b-171">The user is represented in by an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded in the **Win32\_ACE** instance.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a><span data-ttu-id="aa67b-172">См. также</span><span class="sxs-lookup"><span data-stu-id="aa67b-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa67b-173">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="aa67b-173">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> <dt>

[<span data-ttu-id="aa67b-174">Вспомогательный класс дескриптора безопасности</span><span class="sxs-lookup"><span data-stu-id="aa67b-174">Security Descriptor Helper Class</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[<span data-ttu-id="aa67b-175">Рекомендации по обеспечению безопасности</span><span class="sxs-lookup"><span data-stu-id="aa67b-175">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[<span data-ttu-id="aa67b-176">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="aa67b-176">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="aa67b-177">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="aa67b-177">Access Control</span></span>](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[<span data-ttu-id="aa67b-178">Доступ к пространствам имен WMI</span><span class="sxs-lookup"><span data-stu-id="aa67b-178">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

