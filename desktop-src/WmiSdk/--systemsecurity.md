---
description: Содержит методы, позволяющие получать доступ и изменять параметры безопасности для пространства имен.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: Класс __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156930"
---
# <a name="__systemsecurity-class"></a><span data-ttu-id="af843-103">\_\_Класс Системсекурити</span><span class="sxs-lookup"><span data-stu-id="af843-103">\_\_SystemSecurity class</span></span>

<span data-ttu-id="af843-104">Класс System **\_ \_ системсекурити** содержит методы, позволяющие получать доступ к параметрам безопасности пространства имен и изменять их.</span><span class="sxs-lookup"><span data-stu-id="af843-104">The **\_\_SystemSecurity** system class contains methods that let you access and modify the security settings for a namespace.</span></span> <span data-ttu-id="af843-105">Класс **\_ \_ системсекурити** является Singleton-классом в каждом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="af843-105">The **\_\_SystemSecurity** class is a singleton class in each namespace.</span></span>

> [!Note]  
> <span data-ttu-id="af843-106">Дополнительные сведения см. в разделе [Настройка дескрипторов безопасности намепаце](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="af843-106">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

 

<span data-ttu-id="af843-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="af843-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="af843-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="af843-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af843-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af843-109">Syntax</span></span>

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a><span data-ttu-id="af843-110">Члены</span><span class="sxs-lookup"><span data-stu-id="af843-110">Members</span></span>

<span data-ttu-id="af843-111">Класс **\_ \_ системсекурити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="af843-111">The **\_\_SystemSecurity** class has these types of members:</span></span>

-   [<span data-ttu-id="af843-112">Методы</span><span class="sxs-lookup"><span data-stu-id="af843-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="af843-113">Методы</span><span class="sxs-lookup"><span data-stu-id="af843-113">Methods</span></span>

<span data-ttu-id="af843-114">Класс **\_ \_ системсекурити** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="af843-114">The **\_\_SystemSecurity** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="af843-115">Метод</span><span class="sxs-lookup"><span data-stu-id="af843-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="af843-116">Описание</span><span class="sxs-lookup"><span data-stu-id="af843-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="af843-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="af843-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="af843-118">Возвращает список пользователей, которым разрешен удаленный доступ.</span><span class="sxs-lookup"><span data-stu-id="af843-118">Gets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="af843-119">Этот метод не работает в поддерживаемых версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="af843-119">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="af843-120">Вместо этого используйте <a href="--systemsecurity-getsd.md"><strong>возвращает</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="af843-120">Use <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="af843-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>жеткаллеракцессригхтс</strong></a></span><span class="sxs-lookup"><span data-stu-id="af843-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="af843-122">Возвращает маску для каждого бита, соответствующего право доступа.</span><span class="sxs-lookup"><span data-stu-id="af843-122">Returns a mask with each bit that corresponds to an access right.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="af843-123"><a href="--systemsecurity-getsd.md"><strong>Получает</strong></a></span><span class="sxs-lookup"><span data-stu-id="af843-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="af843-124">Возвращает <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> для пространства имен, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="af843-124">Gets the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="af843-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>жетсекуритидескриптор</strong></a></span><span class="sxs-lookup"><span data-stu-id="af843-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="af843-126">Возвращает дескриптор безопасности, управляющий доступом к пространству имен WMI, связанному с экземпляром <strong>__SystemSecurity</strong>.</span><span class="sxs-lookup"><span data-stu-id="af843-126">Gets the security descriptor that controls access to the WMI namespace associated with the instance of <strong>__SystemSecurity</strong>.</span></span> <span data-ttu-id="af843-127">Дескриптор безопасности возвращается как экземпляр<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="af843-127">The security descriptor is returned as an instance of<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="af843-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="af843-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="af843-129">Задает список пользователей, которым разрешен удаленный доступ.</span><span class="sxs-lookup"><span data-stu-id="af843-129">Sets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="af843-130">Этот метод не работает в поддерживаемых версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="af843-130">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="af843-131">Вместо этого используйте <a href="--systemsecurity-setsd.md"><strong>набор</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="af843-131">Use <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="af843-132"><a href="--systemsecurity-setsd.md"><strong>Устанавливается</strong></a></span><span class="sxs-lookup"><span data-stu-id="af843-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="af843-133">Задает дескриптор безопасности для пространства имен, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="af843-133">Sets the security descriptor for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="af843-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>сетсекуритидескриптор</strong></a></span><span class="sxs-lookup"><span data-stu-id="af843-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="af843-135">Записывает обновленную версию дескриптора безопасности, которая управляет доступом к принтеру.</span><span class="sxs-lookup"><span data-stu-id="af843-135">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="af843-136">Дескриптор безопасности представлен экземпляром <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="af843-136">The security descriptor is represented by an instance of <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="af843-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af843-137">Remarks</span></span>

<span data-ttu-id="af843-138">Можно потребовать, чтобы клиентские скрипты и приложения использовали зашифрованное соединение для проверки подлинности, добавив квалификатор **рекуиресенкриптион** в MOF-файл, который создает пространство имен.</span><span class="sxs-lookup"><span data-stu-id="af843-138">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="af843-139">Можно также изменить существующее пространство имен, добавив этот атрибут и повторно скомпилировать MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="af843-139">You can also modify an existing namespace by adding this attribute and compile the .mof file again.</span></span> <span data-ttu-id="af843-140">Дополнительные сведения об использовании **рекуиресенкриптион** см. в разделе [запрос зашифрованного соединения с пространством имен](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="af843-140">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af843-141">Требования</span><span class="sxs-lookup"><span data-stu-id="af843-141">Requirements</span></span>



| <span data-ttu-id="af843-142">Требование</span><span class="sxs-lookup"><span data-stu-id="af843-142">Requirement</span></span> | <span data-ttu-id="af843-143">Значение</span><span class="sxs-lookup"><span data-stu-id="af843-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="af843-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af843-144">Minimum supported client</span></span><br/> | <span data-ttu-id="af843-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af843-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="af843-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af843-146">Minimum supported server</span></span><br/> | <span data-ttu-id="af843-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af843-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="af843-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="af843-148">Namespace</span></span><br/>                | <span data-ttu-id="af843-149">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="af843-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="af843-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af843-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af843-151">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="af843-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="af843-152">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="af843-152">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="af843-153">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="af843-153">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="af843-154">Защита пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="af843-154">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="af843-155">Установка наследования безопасности пространства имен</span><span class="sxs-lookup"><span data-stu-id="af843-155">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="af843-156">Списки управления доступом (ACL)</span><span class="sxs-lookup"><span data-stu-id="af843-156">Access Control Lists (ACLs)</span></span>](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[<span data-ttu-id="af843-157">**\_Дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="af843-157">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

