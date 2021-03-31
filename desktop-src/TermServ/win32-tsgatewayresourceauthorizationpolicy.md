---
title: Класс Win32_TSGatewayResourceAuthorizationPolicy
description: Описание политики авторизации ресурсов удаленный рабочий стол (RD \ 160; RAP). RD \ 160; Политика авторизации ресурсов позволяет определить, разрешено ли пользователю подключаться к указанному ресурсу через шлюз удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayResourceAuthorizationPolicy, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071546"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="18777-106">\_Класс Win32 тсгатевайресаурцеаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="18777-106">Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="18777-107">Описание политики авторизации ресурсов (RD RAP) удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="18777-107">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="18777-108">Политика авторизации ресурсов удаленных рабочих столов используется для принятия решения о том, разрешено ли пользователю подключаться к указанному ресурсу через шлюз удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="18777-108">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="18777-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18777-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a><span data-ttu-id="18777-110">Члены</span><span class="sxs-lookup"><span data-stu-id="18777-110">Members</span></span>

<span data-ttu-id="18777-111">Класс **Win32 \_ тсгатевайресаурцеаусоризатионполици** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="18777-111">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="18777-112">Методы</span><span class="sxs-lookup"><span data-stu-id="18777-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="18777-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="18777-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18777-114">Методы</span><span class="sxs-lookup"><span data-stu-id="18777-114">Methods</span></span>

<span data-ttu-id="18777-115">Класс **Win32 \_ тсгатевайресаурцеаусоризатионполици** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="18777-115">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="18777-116">Метод</span><span class="sxs-lookup"><span data-stu-id="18777-116">Method</span></span>                                                                                          | <span data-ttu-id="18777-117">Описание</span><span class="sxs-lookup"><span data-stu-id="18777-117">Description</span></span>                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18777-118">**аддусерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="18777-118">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="18777-119">Добавляет указанные имена групп пользователей в существующие группы пользователей в свойстве **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="18777-119">Adds the specified user group names to the existing user groups in the **UserGroupNames** property.</span></span><br/>      |
| [<span data-ttu-id="18777-120">**Создать**</span><span class="sxs-lookup"><span data-stu-id="18777-120">**Create**</span></span>](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="18777-121">Создает политику авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-121">Creates an RD RAP.</span></span><br/>                                                                                       |
| [<span data-ttu-id="18777-122">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="18777-122">**Delete**</span></span>](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="18777-123">Удаляет текущую политику авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-123">Deletes the current RD RAP.</span></span><br/>                                                                              |
| [<span data-ttu-id="18777-124">**ремовеусерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="18777-124">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | <span data-ttu-id="18777-125">Удаляет указанные имена групп пользователей из существующих групп пользователей в свойстве **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="18777-125">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span><br/> |
| [<span data-ttu-id="18777-126">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="18777-126">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="18777-127">Задает свойство **Description** для политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-127">Sets the **Description** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="18777-128">**сетенаблед**</span><span class="sxs-lookup"><span data-stu-id="18777-128">**SetEnabled**</span></span>](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | <span data-ttu-id="18777-129">Включает или отключает политику авторизации ресурсов удаленных рабочих столов, устанавливая свойство **Enabled** .</span><span class="sxs-lookup"><span data-stu-id="18777-129">Enables or disables the RD RAP by setting the **Enabled** property.</span></span><br/>                                      |
| [<span data-ttu-id="18777-130">**SetName**</span><span class="sxs-lookup"><span data-stu-id="18777-130">**SetName**</span></span>](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | <span data-ttu-id="18777-131">Задает свойство **Name** для политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-131">Sets the **Name** property for the RD RAP.</span></span><br/>                                                               |
| [<span data-ttu-id="18777-132">**сетпортнумберс**</span><span class="sxs-lookup"><span data-stu-id="18777-132">**SetPortNumbers**</span></span>](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="18777-133">Задает свойство **портнумберс** для политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-133">Sets the **PortNumbers** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="18777-134">**сетресаурцеграуп**</span><span class="sxs-lookup"><span data-stu-id="18777-134">**SetResourceGroup**</span></span>](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | <span data-ttu-id="18777-135">Задает свойства **ресаурцеграуптипе** и **ResourceGroupName** .</span><span class="sxs-lookup"><span data-stu-id="18777-135">Sets the **ResourceGroupType** and **ResourceGroupName** properties.</span></span><br/>                                     |
| [<span data-ttu-id="18777-136">**сетусерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="18777-136">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="18777-137">Задает свойство **усерграупнамес** для политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-137">Sets the **UserGroupNames** property for the RD RAP.</span></span><br/>                                                     |
| [<span data-ttu-id="18777-138">**Обновляют**</span><span class="sxs-lookup"><span data-stu-id="18777-138">**Update**</span></span>](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="18777-139">Обновляет текущую политику авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-139">Updates the current RD RAP.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="18777-140">Свойства</span><span class="sxs-lookup"><span data-stu-id="18777-140">Properties</span></span>

<span data-ttu-id="18777-141">Класс **Win32 \_ тсгатевайресаурцеаусоризатионполици** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="18777-141">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18777-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="18777-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18777-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18777-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18777-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18777-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18777-145">Описание политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-145">Description of the RD RAP.</span></span> <span data-ttu-id="18777-146">Это свойство изменяется с помощью метода [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="18777-146">This property is changed with the [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="18777-147">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="18777-147">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18777-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18777-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18777-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18777-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18777-150">Указывает, включена ли политика авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-150">Indicates whether this RD RAP is enabled.</span></span> <span data-ttu-id="18777-151">Это свойство изменяется с помощью метода [**сетенаблед**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="18777-151">This property is changed with the [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="18777-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="18777-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18777-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18777-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18777-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18777-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18777-155">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18777-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18777-156">Имя политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="18777-156">Name of the RD RAP.</span></span> <span data-ttu-id="18777-157">Это свойство изменяется с помощью метода [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="18777-157">This property is changed with the [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="18777-158">**портнумберс**</span><span class="sxs-lookup"><span data-stu-id="18777-158">**PortNumbers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18777-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18777-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18777-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18777-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18777-161">Список номеров портов, разделенных точкой с запятой, которые разрешены для этой политики.</span><span class="sxs-lookup"><span data-stu-id="18777-161">List of semicolon-separated port numbers that are allowed for this policy.</span></span> <span data-ttu-id="18777-162">Чтобы разрешить любой номер порта, установите " \* ".</span><span class="sxs-lookup"><span data-stu-id="18777-162">To allow any port number, set "\*".</span></span>

</dd> <dt>

<span data-ttu-id="18777-163">**протоколнамес**</span><span class="sxs-lookup"><span data-stu-id="18777-163">**ProtocolNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18777-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18777-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18777-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18777-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18777-166">Список имен протоколов, разделенных точкой с запятой, которые включены для этой политики.</span><span class="sxs-lookup"><span data-stu-id="18777-166">List of semicolon-separated protocol names that are enabled for this policy.</span></span> <span data-ttu-id="18777-167">Имена должны соответствовать возвращаемому методу [**жетпротоколнаме**](getprotocolname-win32-tsgatewayserversettings.md) класса [**Win32 \_ тсгатевайсерверсеттингс**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="18777-167">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="18777-168">**ResourceGroupName**</span><span class="sxs-lookup"><span data-stu-id="18777-168">**ResourceGroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18777-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18777-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18777-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18777-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18777-171">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18777-171">Resource group name.</span></span> <span data-ttu-id="18777-172">Это свойство изменяется с помощью метода [**сетресаурцеграуп**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="18777-172">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="18777-173">**ресаурцеграуптипе**</span><span class="sxs-lookup"><span data-stu-id="18777-173">**ResourceGroupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18777-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18777-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18777-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18777-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18777-176">Определяет тип группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18777-176">Identifies the type of the resource group.</span></span> <span data-ttu-id="18777-177">Это свойство изменяется с помощью метода [**сетресаурцеграуп**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="18777-177">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

<dt>

<span data-ttu-id="18777-178">RG</span><span class="sxs-lookup"><span data-stu-id="18777-178">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="18777-179">группа ресурсов;</span><span class="sxs-lookup"><span data-stu-id="18777-179">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="18777-180">CG</span><span class="sxs-lookup"><span data-stu-id="18777-180">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="18777-181">Группа компьютеров, сохраненная в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="18777-181">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="18777-182">КАЖДОГО</span><span class="sxs-lookup"><span data-stu-id="18777-182">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="18777-183">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="18777-183">All resources.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18777-184">**усерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="18777-184">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18777-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18777-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18777-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18777-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18777-187">Разделенный точками с запятой список имен групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="18777-187">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="18777-188">Если пользователь принадлежит к любой из этих групп пользователей, доступ будет разрешен.</span><span class="sxs-lookup"><span data-stu-id="18777-188">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="18777-189">Это свойство изменяется с помощью методов [**сетусерграупнамес**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**аддусерграупнамес**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)и [**ремовеусерграупнамес**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="18777-189">This property is changed with the [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), and [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18777-190">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18777-190">Remarks</span></span>

<span data-ttu-id="18777-191">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="18777-191">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="18777-192">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="18777-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="18777-193">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="18777-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="18777-194">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="18777-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="18777-195">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="18777-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="18777-196">Требования</span><span class="sxs-lookup"><span data-stu-id="18777-196">Requirements</span></span>



| <span data-ttu-id="18777-197">Требование</span><span class="sxs-lookup"><span data-stu-id="18777-197">Requirement</span></span> | <span data-ttu-id="18777-198">Значение</span><span class="sxs-lookup"><span data-stu-id="18777-198">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18777-199">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18777-199">Minimum supported client</span></span><br/> | <span data-ttu-id="18777-200">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="18777-200">None supported</span></span><br/>                                                                |
| <span data-ttu-id="18777-201">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18777-201">Minimum supported server</span></span><br/> | <span data-ttu-id="18777-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18777-202">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="18777-203">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18777-203">Namespace</span></span><br/>                | <span data-ttu-id="18777-204">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="18777-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="18777-205">MOF</span><span class="sxs-lookup"><span data-stu-id="18777-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18777-206"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18777-206"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="18777-207">DLL</span><span class="sxs-lookup"><span data-stu-id="18777-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18777-208"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18777-208"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="18777-209">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18777-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18777-210">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="18777-210">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="18777-211">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="18777-211">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="18777-212">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="18777-212">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="18777-213">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="18777-213">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="18777-214">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="18777-214">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="18777-215">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="18777-215">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

