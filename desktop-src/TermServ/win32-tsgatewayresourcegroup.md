---
title: Класс Win32_TSGatewayResourceGroup
description: Описывает группу ресурсов, которая сопоставляет набор ресурсов (имен компьютеров) с одной сущностью.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayResourceGroup, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681865"
---
# <a name="win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="23634-105">\_Класс Win32 тсгатевайресаурцеграуп</span><span class="sxs-lookup"><span data-stu-id="23634-105">Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="23634-106">Описывает группу ресурсов, которая сопоставляет набор ресурсов (имен компьютеров) с одной сущностью.</span><span class="sxs-lookup"><span data-stu-id="23634-106">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="23634-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23634-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a><span data-ttu-id="23634-108">Члены</span><span class="sxs-lookup"><span data-stu-id="23634-108">Members</span></span>

<span data-ttu-id="23634-109">Класс **Win32 \_ тсгатевайресаурцеграуп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="23634-109">The **Win32\_TSGatewayResourceGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="23634-110">Методы</span><span class="sxs-lookup"><span data-stu-id="23634-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="23634-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="23634-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="23634-112">Методы</span><span class="sxs-lookup"><span data-stu-id="23634-112">Methods</span></span>

<span data-ttu-id="23634-113">Класс **Win32 \_ тсгатевайресаурцеграуп** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="23634-113">The **Win32\_TSGatewayResourceGroup** class has these methods.</span></span>



| <span data-ttu-id="23634-114">Метод</span><span class="sxs-lookup"><span data-stu-id="23634-114">Method</span></span>                                                                  | <span data-ttu-id="23634-115">Описание</span><span class="sxs-lookup"><span data-stu-id="23634-115">Description</span></span>                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="23634-116">**аддресаурцес**</span><span class="sxs-lookup"><span data-stu-id="23634-116">**AddResources**</span></span>](addresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="23634-117">Добавляет ресурсы в свойство **Resources** для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-117">Adds resources to the **Resources** property for this resource group.</span></span><br/>      |
| [<span data-ttu-id="23634-118">**Создать**</span><span class="sxs-lookup"><span data-stu-id="23634-118">**Create**</span></span>](create-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="23634-119">Создает группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-119">Creates a resource group.</span></span><br/>                                                  |
| [<span data-ttu-id="23634-120">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="23634-120">**Delete**</span></span>](delete-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="23634-121">Удаляет эту группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-121">Deletes this resource group.</span></span><br/>                                               |
| [<span data-ttu-id="23634-122">**ремовересаурцес**</span><span class="sxs-lookup"><span data-stu-id="23634-122">**RemoveResources**</span></span>](removeresources-win32-tsgatewayresourcegroup.md) | <span data-ttu-id="23634-123">Удаляет ресурсы из свойства **Resources** для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-123">Deletes resources from the **Resources** property for this resource group.</span></span><br/> |
| [<span data-ttu-id="23634-124">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="23634-124">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourcegroup.md)   | <span data-ttu-id="23634-125">Задает свойство **Description** для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-125">Sets the **Description** property for this resource group.</span></span><br/>                 |
| [<span data-ttu-id="23634-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="23634-126">**SetName**</span></span>](setname-win32-tsgatewayresourcegroup.md)                 | <span data-ttu-id="23634-127">Задает свойство **Name** для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-127">Sets the **Name** property for this resource group.</span></span><br/>                        |
| [<span data-ttu-id="23634-128">**сетресаурцес**</span><span class="sxs-lookup"><span data-stu-id="23634-128">**SetResources**</span></span>](setresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="23634-129">Задает свойство **Resources** для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-129">Sets the **Resources** property for this resource group.</span></span><br/>                   |
| [<span data-ttu-id="23634-130">**Обновляют**</span><span class="sxs-lookup"><span data-stu-id="23634-130">**Update**</span></span>](update-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="23634-131">Обновляет эту группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-131">Updates this resource group.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="23634-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="23634-132">Properties</span></span>

<span data-ttu-id="23634-133">Класс **Win32 \_ тсгатевайресаурцеграуп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="23634-133">The **Win32\_TSGatewayResourceGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23634-134">**ассоЦиатедрапс**</span><span class="sxs-lookup"><span data-stu-id="23634-134">**AssociatedRAPs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23634-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="23634-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23634-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="23634-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23634-137">Разделенный точками с запятой список службы удаленных рабочих столов политик авторизации ресурсов (RD RAP), связанных с этой группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-137">Semicolon-separated list of Remote Desktop Services resource authorization policies (RD RAPs) that are associated with this resource group.</span></span>

</dd> <dt>

<span data-ttu-id="23634-138">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23634-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23634-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="23634-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23634-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="23634-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23634-141">Описание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-141">Description of the resource group.</span></span> <span data-ttu-id="23634-142">Это свойство можно изменить с помощью метода [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="23634-142">This property can be changed with the [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="23634-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="23634-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23634-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="23634-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23634-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="23634-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23634-146">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="23634-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="23634-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-147">Name of the resource group.</span></span> <span data-ttu-id="23634-148">Это свойство можно изменить с помощью метода [**SetName**](setname-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="23634-148">This property can be changed with the [**SetName**](setname-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="23634-149">**Ресурсы**</span><span class="sxs-lookup"><span data-stu-id="23634-149">**Resources**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23634-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="23634-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23634-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="23634-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23634-152">Разделенный точками с запятой список ресурсов в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23634-152">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="23634-153">" \* " Означает все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="23634-153">An "\*" means all resources.</span></span> <span data-ttu-id="23634-154">Это свойство можно изменить с помощью методов [**сетресаурцес**](setresources-win32-tsgatewayresourcegroup.md), [**аддресаурцес**](addresources-win32-tsgatewayresourcegroup.md), [**ремовересаурцес**](removeresources-win32-tsgatewayresourcegroup.md)и [**Update**](update-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="23634-154">This property can be changed with the [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md), and [**Update**](update-win32-tsgatewayresourcegroup.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23634-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23634-155">Remarks</span></span>

<span data-ttu-id="23634-156">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="23634-156">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="23634-157">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="23634-157">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="23634-158">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="23634-158">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="23634-159">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="23634-159">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="23634-160">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="23634-160">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="23634-161">Требования</span><span class="sxs-lookup"><span data-stu-id="23634-161">Requirements</span></span>



| <span data-ttu-id="23634-162">Требование</span><span class="sxs-lookup"><span data-stu-id="23634-162">Requirement</span></span> | <span data-ttu-id="23634-163">Значение</span><span class="sxs-lookup"><span data-stu-id="23634-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="23634-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23634-164">Minimum supported client</span></span><br/> | <span data-ttu-id="23634-165">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="23634-165">None supported</span></span><br/>                                                                |
| <span data-ttu-id="23634-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23634-166">Minimum supported server</span></span><br/> | <span data-ttu-id="23634-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23634-167">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="23634-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="23634-168">Namespace</span></span><br/>                | <span data-ttu-id="23634-169">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="23634-169">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="23634-170">MOF</span><span class="sxs-lookup"><span data-stu-id="23634-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23634-171"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23634-171"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="23634-172">DLL</span><span class="sxs-lookup"><span data-stu-id="23634-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23634-173"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23634-173"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="23634-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23634-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23634-175">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="23634-175">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="23634-176">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="23634-176">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="23634-177">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="23634-177">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="23634-178">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="23634-178">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="23634-179">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="23634-179">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="23634-180">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="23634-180">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

