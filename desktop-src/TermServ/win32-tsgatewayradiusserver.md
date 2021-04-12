---
title: Класс Win32_TSGatewayRADIUSServer
description: Описывает сервер протокол RADIUS (RADIUS) с набором политик авторизации подключений службы удаленных рабочих столов (RD \ 160; CAP).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayRADIUSServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayRADIUSServer, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490278"
---
# <a name="win32_tsgatewayradiusserver-class"></a><span data-ttu-id="50007-105">\_Класс Win32 тсгатевайрадиуссервер</span><span class="sxs-lookup"><span data-stu-id="50007-105">Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="50007-106">Описывает сервер протокол RADIUS (RADIUS) с набором политик авторизации подключений (RD CAP) службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="50007-106">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

<span data-ttu-id="50007-107">RADIUS — это стандартный промышленный протокол, используемый для передачи данных проверки подлинности, авторизации и конфигурации между компьютером сервера и сервером проверки подлинности, который называется сервером RADIUS, с базой данных, в которой хранятся сведения о пользователях.</span><span class="sxs-lookup"><span data-stu-id="50007-107">RADIUS is an industry-standard protocol that is used to transmit authentication, authorization, and configuration information between a server computer and an authenticating server, called a RADIUS server, with a database that stores user information.</span></span> <span data-ttu-id="50007-108">Дополнительные сведения см. в разделе [протокол RADIUS](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="50007-108">For more information, see [RADIUS Protocol](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span></span>

## <a name="syntax"></a><span data-ttu-id="50007-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50007-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a><span data-ttu-id="50007-110">Члены</span><span class="sxs-lookup"><span data-stu-id="50007-110">Members</span></span>

<span data-ttu-id="50007-111">Класс **Win32 \_ тсгатевайрадиуссервер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="50007-111">The **Win32\_TSGatewayRADIUSServer** class has these types of members:</span></span>

-   [<span data-ttu-id="50007-112">Методы</span><span class="sxs-lookup"><span data-stu-id="50007-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="50007-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="50007-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="50007-114">Методы</span><span class="sxs-lookup"><span data-stu-id="50007-114">Methods</span></span>

<span data-ttu-id="50007-115">Класс **Win32 \_ тсгатевайрадиуссервер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="50007-115">The **Win32\_TSGatewayRADIUSServer** class has these methods.</span></span>



| <span data-ttu-id="50007-116">Метод</span><span class="sxs-lookup"><span data-stu-id="50007-116">Method</span></span>                                                                 | <span data-ttu-id="50007-117">Описание</span><span class="sxs-lookup"><span data-stu-id="50007-117">Description</span></span>                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="50007-118">**Включить**</span><span class="sxs-lookup"><span data-stu-id="50007-118">**Add**</span></span>](win32-tsgatewayradiusserver-add.md)                         | <span data-ttu-id="50007-119">Добавляет новый сервер RADIUS.</span><span class="sxs-lookup"><span data-stu-id="50007-119">Adds a new RADIUS server.</span></span><br/>                                         |
| [<span data-ttu-id="50007-120">**Вниз**</span><span class="sxs-lookup"><span data-stu-id="50007-120">**MoveDown**</span></span>](movedown-win32-tsgatewayradiusserver.md)               | <span data-ttu-id="50007-121">Перемещает этот сервер RADIUS на одну точку вниз в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="50007-121">Moves this RADIUS server one position down in the priority order.</span></span><br/> |
| [<span data-ttu-id="50007-122">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="50007-122">**MoveUp**</span></span>](moveup-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="50007-123">Перемещает этот сервер RADIUS на одну точку вверх в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="50007-123">Moves this RADIUS server one position up in the priority order.</span></span><br/>   |
| [<span data-ttu-id="50007-124">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="50007-124">**Remove**</span></span>](win32-tsgatewayradiusserver-remove.md)                   | <span data-ttu-id="50007-125">Удаляет текущий сервер RADIUS.</span><span class="sxs-lookup"><span data-stu-id="50007-125">Removes the current RADIUS server.</span></span><br/>                                |
| [<span data-ttu-id="50007-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="50007-126">**SetName**</span></span>](setname-win32-tsgatewayradiusserver.md)                 | <span data-ttu-id="50007-127">Задает свойство **Name** для этого сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="50007-127">Sets the **Name** property for this RADIUS server.</span></span><br/>                |
| [<span data-ttu-id="50007-128">**сетшаредсекрет**</span><span class="sxs-lookup"><span data-stu-id="50007-128">**SetSharedSecret**</span></span>](setsharedsecret-win32-tsgatewayradiusserver.md) | <span data-ttu-id="50007-129">Задает свойство **SharedSecret** для этого сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="50007-129">Sets the **SharedSecret** property for this RADIUS server.</span></span><br/>        |
| [<span data-ttu-id="50007-130">**Обновляют**</span><span class="sxs-lookup"><span data-stu-id="50007-130">**Update**</span></span>](update-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="50007-131">Обновляет текущий сервер RADIUS.</span><span class="sxs-lookup"><span data-stu-id="50007-131">Updates the current RADIUS server.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="50007-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="50007-132">Properties</span></span>

<span data-ttu-id="50007-133">Класс **Win32 \_ тсгатевайрадиуссервер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="50007-133">The **Win32\_TSGatewayRADIUSServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50007-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="50007-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50007-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="50007-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50007-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50007-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50007-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="50007-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="50007-138">Имя сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="50007-138">Name of the RADIUS server.</span></span> <span data-ttu-id="50007-139">Это свойство можно изменить с помощью метода [**SetName**](setname-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="50007-139">This property can be changed with the [**SetName**](setname-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="50007-140">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="50007-140">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50007-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50007-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50007-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50007-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50007-143">Приоритет сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="50007-143">Priority of the RADIUS server.</span></span> <span data-ttu-id="50007-144">Сервер шлюза удаленных рабочих столов выполняет поиск политик авторизации подключений удаленных рабочих столов на серверах RADIUS в зависимости от приоритета.</span><span class="sxs-lookup"><span data-stu-id="50007-144">The RD Gateway server looks for RD CAPs on RADIUS servers based on the priority.</span></span> <span data-ttu-id="50007-145">Это свойство можно изменить с помощью методов [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**вниз**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)и [**Remove**](win32-tsgatewayradiusserver-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="50007-145">This property can be changed with the [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md), and [**Remove**](win32-tsgatewayradiusserver-remove.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="50007-146">**SharedSecret**</span><span class="sxs-lookup"><span data-stu-id="50007-146">**SharedSecret**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50007-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="50007-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50007-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="50007-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50007-149">Общий секрет для сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="50007-149">Shared secret for the RADIUS server.</span></span> <span data-ttu-id="50007-150">Это свойство можно изменить с помощью метода [**сетшаредсекрет**](setsharedsecret-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="50007-150">This property can be changed with the [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50007-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50007-151">Remarks</span></span>

<span data-ttu-id="50007-152">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="50007-152">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="50007-153">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="50007-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="50007-154">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="50007-154">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="50007-155">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="50007-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="50007-156">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="50007-156">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="50007-157">Требования</span><span class="sxs-lookup"><span data-stu-id="50007-157">Requirements</span></span>



| <span data-ttu-id="50007-158">Требование</span><span class="sxs-lookup"><span data-stu-id="50007-158">Requirement</span></span> | <span data-ttu-id="50007-159">Значение</span><span class="sxs-lookup"><span data-stu-id="50007-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50007-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50007-160">Minimum supported client</span></span><br/> | <span data-ttu-id="50007-161">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="50007-161">None supported</span></span><br/>                                                                |
| <span data-ttu-id="50007-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50007-162">Minimum supported server</span></span><br/> | <span data-ttu-id="50007-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50007-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="50007-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="50007-164">Namespace</span></span><br/>                | <span data-ttu-id="50007-165">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="50007-165">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="50007-166">MOF</span><span class="sxs-lookup"><span data-stu-id="50007-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50007-167"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50007-167"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="50007-168">DLL</span><span class="sxs-lookup"><span data-stu-id="50007-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50007-169"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50007-169"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="50007-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50007-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50007-171">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="50007-171">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="50007-172">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="50007-172">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="50007-173">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="50007-173">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="50007-174">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="50007-174">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="50007-175">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="50007-175">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="50007-176">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="50007-176">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

