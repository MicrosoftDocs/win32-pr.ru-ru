---
description: Приложения и скрипты C++, работающие под полной учетной записью администратора, могут изменять дескриптор безопасности пространства имен.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Задание дескрипторов безопасности пространства имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703176"
---
# <a name="setting-namespace-security-descriptors"></a><span data-ttu-id="1bd09-103">Задание дескрипторов безопасности пространства имен</span><span class="sxs-lookup"><span data-stu-id="1bd09-103">Setting Namespace Security Descriptors</span></span>

<span data-ttu-id="1bd09-104">Приложения и скрипты C++, работающие под полной учетной записью администратора, могут изменять дескриптор безопасности пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1bd09-104">Both C++ applications and scripts running under a full administrator account can change a namespace security descriptor.</span></span>

## <a name="namespace-security-descriptors"></a><span data-ttu-id="1bd09-105">Дескрипторы безопасности пространства имен</span><span class="sxs-lookup"><span data-stu-id="1bd09-105">Namespace Security Descriptors</span></span>

<span data-ttu-id="1bd09-106">Каждое пространство имен WMI имеет [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly), который позволяет каждому пространству имен иметь уникальные параметры безопасности, определяющие, кто имеет доступ к данным и методам пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1bd09-106">Each WMI namespace has a [*security descriptor*](/windows/desktop/SecGloss/s-gly), which allows each namespace to have unique security settings that determine who has access to the namespace data and methods.</span></span> <span data-ttu-id="1bd09-107">Дополнительные сведения о безопасности доступа WMI см. [в разделе доступ к защищаемым ОБЪЕКТАМ WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1bd09-107">For more information about WMI access security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span> <span data-ttu-id="1bd09-108">[Доступ к пространствам имен WMI](access-to-wmi-namespaces.md) описывает параметры безопасности по умолчанию для пространств имен WMI и аудита безопасности в WMI.</span><span class="sxs-lookup"><span data-stu-id="1bd09-108">[Access to WMI Namespaces](access-to-wmi-namespaces.md) describes the default security settings for WMI namespaces and security auditing in WMI.</span></span>

<span data-ttu-id="1bd09-109">Разрешения учетной записи для каждого пространства имен WMI в репозитории WMI (CIM) можно задать следующими способами.</span><span class="sxs-lookup"><span data-stu-id="1bd09-109">You can set account permissions for each WMI namespace in the WMI (CIM) repository in the following ways:</span></span>

-   <span data-ttu-id="1bd09-110">При создании пространства имен в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="1bd09-110">When the namespace is created in the MOF file.</span></span> <span data-ttu-id="1bd09-111">Дополнительные сведения см. [в разделе Настройка безопасности пространства имен при создании пространства имен](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="1bd09-111">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>
-   <span data-ttu-id="1bd09-112">Вручную, используя элемент управления WMI.</span><span class="sxs-lookup"><span data-stu-id="1bd09-112">Manually, using the WMI Control.</span></span> <span data-ttu-id="1bd09-113">Дополнительные сведения см. [в разделе Настройка безопасности пространства имен с помощью элемента управления WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="1bd09-113">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>
-   <span data-ttu-id="1bd09-114">Программно, путем вызова методов класса [**\_ \_ системсекурити**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="1bd09-114">Programmatically, by calling the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span>

<span data-ttu-id="1bd09-115">Следующие методы объекта [**\_ \_ системсекурити**](--systemsecurity.md) , связанного с каждым пространством имен, позволяют считывать или изменять безопасность пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1bd09-115">The following methods of the [**\_\_SystemSecurity**](--systemsecurity.md) object associated with each namespace allow you to read or change security on a namespace.</span></span>

<dl> <dt>

<span data-ttu-id="1bd09-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**жеткаллеракцессригхтс**](--systemsecurity-getcalleraccessrights.md)</span><span class="sxs-lookup"><span data-stu-id="1bd09-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span></span>
</dt> <dd>

<span data-ttu-id="1bd09-117">Устанавливает параметр *прав* в виде точечного рисунка с каждым битом, соответствующим прав доступа.</span><span class="sxs-lookup"><span data-stu-id="1bd09-117">Sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span>

</dd> <dt>

<span data-ttu-id="1bd09-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**Получает**](--systemsecurity-getsd.md)</span><span class="sxs-lookup"><span data-stu-id="1bd09-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="1bd09-119">Возвращает дескриптор безопасности для пространства имен, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="1bd09-119">Gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="1bd09-120">Этот метод возвращает дескриптор безопасности в двоичном формате массива байтов.</span><span class="sxs-lookup"><span data-stu-id="1bd09-120">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="1bd09-121">При написании скрипта используйте метод [**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="1bd09-121">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="1bd09-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**Устанавливается**](--systemsecurity-setsd.md)</span><span class="sxs-lookup"><span data-stu-id="1bd09-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="1bd09-123">Задает дескриптор безопасности (SD) для пространства имен, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="1bd09-123">Sets the security descriptor (SD) for the namespace to which a user is connected.</span></span> <span data-ttu-id="1bd09-124">Этот метод требует наличия дескриптора безопасности в двоичном формате массива байтов.</span><span class="sxs-lookup"><span data-stu-id="1bd09-124">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="1bd09-125">При написании скрипта используйте метод [**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="1bd09-125">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="1bd09-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span><span class="sxs-lookup"><span data-stu-id="1bd09-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span></span>
</dt> <dd>

<span data-ttu-id="1bd09-127">Возвращает дескриптор безопасности, управляющий доступом к пространству имен WMI, связанному с экземпляром [**\_ \_ системсекурити**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="1bd09-127">Gets the security descriptor that controls access to the WMI namespace associated with the instance of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="1bd09-128">Дескриптор безопасности возвращается в виде экземпляра [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="1bd09-128">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bd09-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span><span class="sxs-lookup"><span data-stu-id="1bd09-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span></span>
</dt> <dd>

<span data-ttu-id="1bd09-130">Записывает обновленную версию дескриптора безопасности, которая управляет доступом к принтеру.</span><span class="sxs-lookup"><span data-stu-id="1bd09-130">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="1bd09-131">Дескриптор безопасности представлен экземпляром [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="1bd09-131">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bd09-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="1bd09-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="1bd09-133">Получает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="1bd09-133">Gets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> <dt>

<span data-ttu-id="1bd09-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="1bd09-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="1bd09-135">Задает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="1bd09-135">Sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> </dl>

<span data-ttu-id="1bd09-136">При написании скриптов используйте [**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class---systemsecurity-.md) и [**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="1bd09-136">If you are writing scripts, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) and [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span></span> <span data-ttu-id="1bd09-137">Для изменения дескрипторов безопасности можно использовать методы класса [**\_ Секуритидескрипторхелпер в Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) .</span><span class="sxs-lookup"><span data-stu-id="1bd09-137">You can use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to alter the security descriptors.</span></span>

<span data-ttu-id="1bd09-138">При программировании на C++ можно манипулировать двоичным дескриптором безопасности с помощью [языка определения дескрипторов безопасности (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)и методов преобразования [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) и [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="1bd09-138">If you are programming in C++, you can manipulate the binary security descriptor using [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="1bd09-139">Имейте в виду, что начиная с Windows Vista [Управление учетными записями пользователей](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) влияет на доступ к данным WMI и что может быть настроено с помощью [*элемента управления WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="1bd09-139">Be aware that, starting with Windows Vista, [User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="1bd09-140">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="1bd09-140">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bd09-141">См. также</span><span class="sxs-lookup"><span data-stu-id="1bd09-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bd09-142">Защита пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="1bd09-142">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="1bd09-143">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="1bd09-143">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="1bd09-144">Доступ к пространствам имен WMI</span><span class="sxs-lookup"><span data-stu-id="1bd09-144">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="1bd09-145">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="1bd09-145">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
