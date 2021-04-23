---
title: Класс Win32_TSGatewayLoadBalancer
description: Описывает набор серверов балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов). Они используются для балансировки нагрузки подключений к шлюзу удаленных рабочих столов на нескольких серверах.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayLoadBalancer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayLoadBalancer, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802087"
---
# <a name="win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="44f49-106">\_Класс Win32 тсгатевайлоадбаланцер</span><span class="sxs-lookup"><span data-stu-id="44f49-106">Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="44f49-107">Описывает набор серверов балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="44f49-107">Describes a set of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span> <span data-ttu-id="44f49-108">Они используются для балансировки нагрузки подключений к шлюзу удаленных рабочих столов на нескольких серверах.</span><span class="sxs-lookup"><span data-stu-id="44f49-108">These are used to load balance RD Gateway connections across multiple servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f49-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44f49-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a><span data-ttu-id="44f49-110">Члены</span><span class="sxs-lookup"><span data-stu-id="44f49-110">Members</span></span>

<span data-ttu-id="44f49-111">Класс **Win32 \_ тсгатевайлоадбаланцер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="44f49-111">The **Win32\_TSGatewayLoadBalancer** class has these types of members:</span></span>

-   [<span data-ttu-id="44f49-112">Методы</span><span class="sxs-lookup"><span data-stu-id="44f49-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="44f49-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="44f49-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="44f49-114">Методы</span><span class="sxs-lookup"><span data-stu-id="44f49-114">Methods</span></span>

<span data-ttu-id="44f49-115">Класс **Win32 \_ тсгатевайлоадбаланцер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="44f49-115">The **Win32\_TSGatewayLoadBalancer** class has these methods.</span></span>



| <span data-ttu-id="44f49-116">Метод</span><span class="sxs-lookup"><span data-stu-id="44f49-116">Method</span></span>                                                                             | <span data-ttu-id="44f49-117">Описание</span><span class="sxs-lookup"><span data-stu-id="44f49-117">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44f49-118">**аддсерверс**</span><span class="sxs-lookup"><span data-stu-id="44f49-118">**AddServers**</span></span>](addservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="44f49-119">Добавляет серверы в свойство **Servers** .</span><span class="sxs-lookup"><span data-stu-id="44f49-119">Adds servers to the **Servers** property.</span></span><br/>                                                             |
| [<span data-ttu-id="44f49-120">**делетеаллсерверс**</span><span class="sxs-lookup"><span data-stu-id="44f49-120">**DeleteAllServers**</span></span>](deleteallservers-win32-tsgatewayloadbalancer.md)           | <span data-ttu-id="44f49-121">Удаляет все серверы балансировки нагрузки шлюза удаленных рабочих столов, участвующие в ферме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="44f49-121">Deletes all RD Gateway load-balancing servers participating in the load-balancing farm.</span></span><br/>               |
| [<span data-ttu-id="44f49-122">**делетесерверс**</span><span class="sxs-lookup"><span data-stu-id="44f49-122">**DeleteServers**</span></span>](deleteservers-win32-tsgatewayloadbalancer.md)                 | <span data-ttu-id="44f49-123">Удаляет серверы из свойства **Servers** .</span><span class="sxs-lookup"><span data-stu-id="44f49-123">Deletes servers from the **Servers** property.</span></span><br/>                                                        |
| [<span data-ttu-id="44f49-124">**ислоадбаланЦингсервер**</span><span class="sxs-lookup"><span data-stu-id="44f49-124">**IsLoadBalancingServer**</span></span>](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | <span data-ttu-id="44f49-125">Определяет, может ли сервер выполнять балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="44f49-125">Determines whether the server can perform load balancing.</span></span><br/>                                             |
| [<span data-ttu-id="44f49-126">**сетсерверс**</span><span class="sxs-lookup"><span data-stu-id="44f49-126">**SetServers**</span></span>](setservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="44f49-127">Задает свойство **Servers** с разделенным точкой с запятой списком серверов балансировки нагрузки шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="44f49-127">Sets the **Servers** property with the semicolon-separated list of RD Gateway load-balancing servers.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="44f49-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="44f49-128">Properties</span></span>

<span data-ttu-id="44f49-129">Класс **Win32 \_ тсгатевайлоадбаланцер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="44f49-129">The **Win32\_TSGatewayLoadBalancer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44f49-130">**Серверы**</span><span class="sxs-lookup"><span data-stu-id="44f49-130">**Servers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f49-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="44f49-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44f49-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44f49-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44f49-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44f49-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44f49-134">Разделенный точками с запятой список серверов балансировки нагрузки шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="44f49-134">Semicolon-separated list of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="44f49-135">Это свойство можно изменить с помощью методов [**сетсерверс**](setservers-win32-tsgatewayloadbalancer.md), [**аддсерверс**](addservers-win32-tsgatewayloadbalancer.md), [**делетесерверс**](deleteservers-win32-tsgatewayloadbalancer.md)и [**делетеаллсерверс**](deleteallservers-win32-tsgatewayloadbalancer.md) .</span><span class="sxs-lookup"><span data-stu-id="44f49-135">This property can be changed with the [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md), and [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44f49-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44f49-136">Remarks</span></span>

<span data-ttu-id="44f49-137">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="44f49-137">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="44f49-138">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="44f49-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="44f49-139">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="44f49-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="44f49-140">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="44f49-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="44f49-141">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="44f49-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="44f49-142">Требования</span><span class="sxs-lookup"><span data-stu-id="44f49-142">Requirements</span></span>



| <span data-ttu-id="44f49-143">Требование</span><span class="sxs-lookup"><span data-stu-id="44f49-143">Requirement</span></span> | <span data-ttu-id="44f49-144">Значение</span><span class="sxs-lookup"><span data-stu-id="44f49-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44f49-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44f49-145">Minimum supported client</span></span><br/> | <span data-ttu-id="44f49-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="44f49-146">None supported</span></span><br/>                                                                |
| <span data-ttu-id="44f49-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44f49-147">Minimum supported server</span></span><br/> | <span data-ttu-id="44f49-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44f49-148">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="44f49-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="44f49-149">Namespace</span></span><br/>                | <span data-ttu-id="44f49-150">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="44f49-150">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="44f49-151">MOF</span><span class="sxs-lookup"><span data-stu-id="44f49-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44f49-152"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44f49-152"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="44f49-153">DLL</span><span class="sxs-lookup"><span data-stu-id="44f49-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44f49-154"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44f49-154"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="44f49-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44f49-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f49-156">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="44f49-156">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="44f49-157">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="44f49-157">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="44f49-158">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="44f49-158">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="44f49-159">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="44f49-159">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="44f49-160">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="44f49-160">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="44f49-161">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="44f49-161">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

