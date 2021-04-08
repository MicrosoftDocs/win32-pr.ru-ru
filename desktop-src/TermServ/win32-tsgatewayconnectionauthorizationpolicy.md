---
title: Класс Win32_TSGatewayConnectionAuthorizationPolicy
description: Описание политики авторизации подключений удаленный рабочий стол (RD \ 160; CAP). RD \ 160; С помощью политик можно определить, разрешено ли пользователю подключаться к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayConnectionAuthorizationPolicy, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891813"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="47859-106">\_Класс Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="47859-106">Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="47859-107">Описание политики авторизации подключений удаленный рабочий стол (RD CAP).</span><span class="sxs-lookup"><span data-stu-id="47859-107">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="47859-108">RD CAP используется, чтобы определить, разрешено ли пользователю подключаться к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="47859-108">RD CAPs are used to determine whether a user is allowed to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="47859-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47859-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a><span data-ttu-id="47859-110">Члены</span><span class="sxs-lookup"><span data-stu-id="47859-110">Members</span></span>

<span data-ttu-id="47859-111">Класс **Win32 \_ тсгатевайконнектионаусоризатионполици** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="47859-111">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="47859-112">Методы</span><span class="sxs-lookup"><span data-stu-id="47859-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="47859-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="47859-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="47859-114">Методы</span><span class="sxs-lookup"><span data-stu-id="47859-114">Methods</span></span>

<span data-ttu-id="47859-115">Класс **Win32 \_ тсгатевайконнектионаусоризатионполици** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="47859-115">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="47859-116">Метод</span><span class="sxs-lookup"><span data-stu-id="47859-116">Method</span></span>                                                                                                                | <span data-ttu-id="47859-117">Описание</span><span class="sxs-lookup"><span data-stu-id="47859-117">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47859-118">**аддкомпутерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="47859-118">**AddComputerGroupNames**</span></span>](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="47859-119">Добавляет указанные имена групп компьютеров в свойство **компутерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="47859-119">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span><br/>                                                                                      |
| [<span data-ttu-id="47859-120">**аддусерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="47859-120">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="47859-121">Добавляет указанные имена групп пользователей в свойство **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="47859-121">Adds the specified user group names to the **UserGroupNames** property.</span></span><br/>                                                                                              |
| [<span data-ttu-id="47859-122">**Создать**</span><span class="sxs-lookup"><span data-stu-id="47859-122">**Create**</span></span>](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="47859-123">Создает ограничение удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47859-123">Creates an RD CAP.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="47859-124">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="47859-124">**Delete**</span></span>](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="47859-125">Удаляет текущую политику авторизации подключений к удаленным рабочим столам.</span><span class="sxs-lookup"><span data-stu-id="47859-125">Deletes the current RD CAP.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="47859-126">**дисаблеклипбоард**</span><span class="sxs-lookup"><span data-stu-id="47859-126">**DisableClipboard**</span></span>](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | <span data-ttu-id="47859-127">Задает свойство **клипбоарддисаблед** .</span><span class="sxs-lookup"><span data-stu-id="47859-127">Sets the **ClipboardDisabled** property.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="47859-128">**дисабледискдривес**</span><span class="sxs-lookup"><span data-stu-id="47859-128">**DisableDiskDrives**</span></span>](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="47859-129">Задает свойство **дискдривесдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="47859-129">Sets the **DiskDrivesDisabled** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="47859-130">**дисаблеплугандплайдевицес**</span><span class="sxs-lookup"><span data-stu-id="47859-130">**DisablePlugAndPlayDevices**</span></span>](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | <span data-ttu-id="47859-131">Задает свойство **плугандплайдевицесдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="47859-131">Sets the **PlugAndPlayDevicesDisabled** property.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="47859-132">**дисаблепринтерс**</span><span class="sxs-lookup"><span data-stu-id="47859-132">**DisablePrinters**</span></span>](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | <span data-ttu-id="47859-133">Задает свойство **принтерсдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="47859-133">Sets the **PrintersDisabled** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="47859-134">**дисаблесериалпортс**</span><span class="sxs-lookup"><span data-stu-id="47859-134">**DisableSerialPorts**</span></span>](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="47859-135">Задает свойство **сериалпортсдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="47859-135">Sets the **SerialPortsDisabled** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="47859-136">**енаблеалловонлисдрсерверс**</span><span class="sxs-lookup"><span data-stu-id="47859-136">**EnableAllowOnlySDRServers**</span></span>](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | <span data-ttu-id="47859-137">Используется для переключения свойства **алловонлисдрсерверс**</span><span class="sxs-lookup"><span data-stu-id="47859-137">Used to toggle the **AllowOnlySDRServers** property</span></span><br/> <span data-ttu-id="47859-138">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="47859-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                  |
| [<span data-ttu-id="47859-139">**Вниз**</span><span class="sxs-lookup"><span data-stu-id="47859-139">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | <span data-ttu-id="47859-140">Перемещает текущую закрепление удаленных рабочих столов в списке вниз.</span><span class="sxs-lookup"><span data-stu-id="47859-140">Moves the current RD CAP one position down in the list.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="47859-141">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="47859-141">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="47859-142">Перемещает текущую закрепление удаленных рабочих столов в списке.</span><span class="sxs-lookup"><span data-stu-id="47859-142">Moves the current RD CAP one position up in the list.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="47859-143">**ремовекомпутерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="47859-143">**RemoveComputerGroupNames**</span></span>](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="47859-144">Удаляет указанные имена групп компьютеров из свойства **компутерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="47859-144">Removes the specified computer group names from the **ComputerGroupNames** property.</span></span><br/>                                                                                 |
| [<span data-ttu-id="47859-145">**ремовеусерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="47859-145">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | <span data-ttu-id="47859-146">Удаляет указанные имена групп пользователей из свойства **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="47859-146">Removes specified user group names from the **UserGroupNames** property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="47859-147">**сеткомпутерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="47859-147">**SetComputerGroupNames**</span></span>](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="47859-148">Задает свойство **компутерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="47859-148">Sets the **ComputerGroupNames** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="47859-149">**сеткукиеаусентикатионалловед**</span><span class="sxs-lookup"><span data-stu-id="47859-149">**SetCookieAuthenticationAllowed**</span></span>](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | <span data-ttu-id="47859-150">Задает свойство **кукиеаусентикатионалловед** .</span><span class="sxs-lookup"><span data-stu-id="47859-150">Sets the **CookieAuthenticationAllowed** property.</span></span><br/> <span data-ttu-id="47859-151">**Windows Server 2008:** Этот метод недоступен.</span><span class="sxs-lookup"><span data-stu-id="47859-151">**Windows Server 2008:** This method is not available.</span></span><br/>                                                 |
| [<span data-ttu-id="47859-152">**сетдевицередиректионтипе**</span><span class="sxs-lookup"><span data-stu-id="47859-152">**SetDeviceRedirectionType**</span></span>](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="47859-153">Задает свойство **девицередиректионтипе** .</span><span class="sxs-lookup"><span data-stu-id="47859-153">Sets the **DeviceRedirectionType** property.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="47859-154">**сетенаблед**</span><span class="sxs-lookup"><span data-stu-id="47859-154">**SetEnabled**</span></span>](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | <span data-ttu-id="47859-155">Включает или отключает текущую политику авторизации подключений к удаленным рабочим столам.</span><span class="sxs-lookup"><span data-stu-id="47859-155">Enables or disables the current RD CAP.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="47859-156">**сетидлетимеаут**</span><span class="sxs-lookup"><span data-stu-id="47859-156">**SetIdleTimeout**</span></span>](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | <span data-ttu-id="47859-157">Задает свойство **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="47859-157">Sets the **IdleTimeout** property.</span></span><br/> <span data-ttu-id="47859-158">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="47859-158">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                   |
| [<span data-ttu-id="47859-159">**SetName**</span><span class="sxs-lookup"><span data-stu-id="47859-159">**SetName**</span></span>](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | <span data-ttu-id="47859-160">Задает новое имя для этого ограничения удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47859-160">Sets a new name for this RD CAP.</span></span> <span data-ttu-id="47859-161">Этот метод гарантирует, что имена будут уникальными.</span><span class="sxs-lookup"><span data-stu-id="47859-161">This method ensures that names will be unique.</span></span><br/>                                                                                      |
| [<span data-ttu-id="47859-162">**сетпассвордалловед**</span><span class="sxs-lookup"><span data-stu-id="47859-162">**SetPasswordAllowed**</span></span>](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="47859-163">Задает свойство **пассвордалловед** .</span><span class="sxs-lookup"><span data-stu-id="47859-163">Sets the **PasswordAllowed** property.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="47859-164">**сетсекуреидалловед**</span><span class="sxs-lookup"><span data-stu-id="47859-164">**SetSecureIdAllowed**</span></span>](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="47859-165">Задает свойство **секуреидалловед** .</span><span class="sxs-lookup"><span data-stu-id="47859-165">Sets the **SecureIdAllowed** property.</span></span><br/> <span data-ttu-id="47859-166">**Windows Server 2008:** Этот метод зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="47859-166">**Windows Server 2008:** This method is reserved for future use.</span></span><br/>                                                   |
| [<span data-ttu-id="47859-167">**сетсессионтимеаут**</span><span class="sxs-lookup"><span data-stu-id="47859-167">**SetSessionTimeout**</span></span>](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="47859-168">Задает свойства **SessionTimeout** и **сессионтимеаутактион** .</span><span class="sxs-lookup"><span data-stu-id="47859-168">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span><br/> <span data-ttu-id="47859-169">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="47859-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/> |
| [<span data-ttu-id="47859-170">**сетсмарткардалловед**</span><span class="sxs-lookup"><span data-stu-id="47859-170">**SetSmartcardAllowed**</span></span>](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | <span data-ttu-id="47859-171">Задает свойство **смарткардалловед** .</span><span class="sxs-lookup"><span data-stu-id="47859-171">Sets the **SmartcardAllowed** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="47859-172">**сетусерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="47859-172">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="47859-173">Задает свойство **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="47859-173">Sets the **UserGroupNames** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="47859-174">**Обновляют**</span><span class="sxs-lookup"><span data-stu-id="47859-174">**Update**</span></span>](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="47859-175">Обновляет текущую политику авторизации подключений к удаленным рабочим столам.</span><span class="sxs-lookup"><span data-stu-id="47859-175">Updates the current RD CAP.</span></span><br/>                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="47859-176">Свойства</span><span class="sxs-lookup"><span data-stu-id="47859-176">Properties</span></span>

<span data-ttu-id="47859-177">Класс **Win32 \_ тсгатевайконнектионаусоризатионполици** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="47859-177">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47859-178">**алловонлисдрсерверс**</span><span class="sxs-lookup"><span data-stu-id="47859-178">**AllowOnlySDRServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-179">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-181">Указывает, разрешены ли подключения только для защиты RDS-серверов перенаправления устройств (SDR).</span><span class="sxs-lookup"><span data-stu-id="47859-181">Indicates whether connections allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="47859-182">Это свойство можно задать с помощью метода [**енаблеалловонлисдрсерверс**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .</span><span class="sxs-lookup"><span data-stu-id="47859-182">This property can be set using the [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) method.</span></span>

<span data-ttu-id="47859-183">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="47859-183">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="47859-184">**клипбоарддисаблед**</span><span class="sxs-lookup"><span data-stu-id="47859-184">**ClipboardDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-185">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-187">Указывает, будет ли отключено перенаправление буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="47859-187">Indicates if clipboard redirection will be disabled.</span></span> <span data-ttu-id="47859-188">Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="47859-188">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="47859-189">**компутерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="47859-189">**ComputerGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47859-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47859-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-192">Список имен групп компьютеров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="47859-192">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="47859-193">Это значение может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="47859-193">This value can be empty.</span></span> <span data-ttu-id="47859-194">Имена имеют формат *домена \\ компутерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="47859-194">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="47859-195">Если указано значение, то клиентский компьютер должен принадлежать к одной из этих групп компьютеров для доступа пользователя к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47859-195">If a value is specified, then the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="47859-196">**кукиеаусентикатионалловед**</span><span class="sxs-lookup"><span data-stu-id="47859-196">**CookieAuthenticationAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-197">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-199">Указывает, можно ли использовать проверку подлинности файлов cookie для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47859-199">Indicates if cookie authentication can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="47859-200">Это свойство можно задать с помощью метода [**сеткукиеаусентикатионалловед**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="47859-200">This property can be set by using the [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="47859-201">**Windows Server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="47859-201">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="47859-202">**девицередиректионтипе**</span><span class="sxs-lookup"><span data-stu-id="47859-202">**DeviceRedirectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-203">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47859-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47859-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-205">Указывает, какие устройства будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="47859-205">Specifies which devices will be redirected.</span></span>

<dt>

<span data-ttu-id="47859-206">0</span><span class="sxs-lookup"><span data-stu-id="47859-206">0</span></span>
</dt> <dd>

<span data-ttu-id="47859-207">Все устройства будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="47859-207">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="47859-208">1</span><span class="sxs-lookup"><span data-stu-id="47859-208">1</span></span>
</dt> <dd>

<span data-ttu-id="47859-209">Устройства не будут перенаправлены.</span><span class="sxs-lookup"><span data-stu-id="47859-209">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="47859-210">2</span><span class="sxs-lookup"><span data-stu-id="47859-210">2</span></span>
</dt> <dd>

<span data-ttu-id="47859-211">Указанные устройства не будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="47859-211">Specified devices will not be redirected.</span></span> <span data-ttu-id="47859-212">Свойства **дискдривесдисаблед**, **принтерсдисаблед**, **сериалпортсдисаблед**, **клипбоарддисаблед** и **плугандплайдевицесдисаблед** определяют, какие устройства не будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="47859-212">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47859-213">**дискдривесдисаблед**</span><span class="sxs-lookup"><span data-stu-id="47859-213">**DiskDrivesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-214">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-216">Указывает, будет ли перенаправление диска отключено.</span><span class="sxs-lookup"><span data-stu-id="47859-216">Indicates if disk drive redirection will be disabled.</span></span> <span data-ttu-id="47859-217">Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="47859-217">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="47859-218">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="47859-218">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-219">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-221">Указывает, будет ли использоваться эта политика авторизации подключений удаленных рабочих столов для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="47859-221">Indicates whether this RD CAP will be used to evaluate a user for authorization.</span></span>

</dd> <dt>

<span data-ttu-id="47859-222">**хаснапаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="47859-222">**HasNapAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-223">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-225">Указывает, использует ли политика авторизации подключений к удаленному рабочему столу атрибуты защиты доступа к сети (NAP).</span><span class="sxs-lookup"><span data-stu-id="47859-225">Indicates if the RD CAP uses Network Access Protection (NAP) attributes.</span></span>

</dd> <dt>

<span data-ttu-id="47859-226">**IdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="47859-226">**IdleTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-227">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47859-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47859-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-229">Значение времени ожидания простоя в минутах.</span><span class="sxs-lookup"><span data-stu-id="47859-229">The idle timeout value, in minutes.</span></span> <span data-ttu-id="47859-230">Значение 0 означает отсутствие времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="47859-230">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="47859-231">Это свойство можно задать с помощью метода [**сетидлетимеаут**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="47859-231">This property can be set by using the [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="47859-232">**Windows Server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="47859-232">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="47859-233">**Name**</span><span class="sxs-lookup"><span data-stu-id="47859-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47859-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47859-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47859-236">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47859-236">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47859-237">Имя политики авторизации подключений к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="47859-237">Name of the RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="47859-238">**Заказ**</span><span class="sxs-lookup"><span data-stu-id="47859-238">**Order**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-239">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47859-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47859-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-241">Порядок вычисления политики авторизации подключений к удаленным рабочим столам.</span><span class="sxs-lookup"><span data-stu-id="47859-241">Evaluation order of the RD CAP.</span></span> <span data-ttu-id="47859-242">Первое вычисление авторизации подключений к удаленному рабочему столу имеет значение "1".</span><span class="sxs-lookup"><span data-stu-id="47859-242">The first RD CAP evaluated has a value of "1".</span></span> <span data-ttu-id="47859-243">Свойство **Order** можно изменить при вызове методов [**CREATE**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)или [**вниз**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="47859-243">The **Order** property can be changed when the [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md), or [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="47859-244">**пассвордалловед**</span><span class="sxs-lookup"><span data-stu-id="47859-244">**PasswordAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-245">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-247">Указывает, можно ли использовать пароль для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47859-247">Indicates if a password can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="47859-248">Это свойство можно изменить с помощью метода [**сетпассвордалловед**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="47859-248">This property can be changed by using the [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="47859-249">**плугандплайдевицесдисаблед**</span><span class="sxs-lookup"><span data-stu-id="47859-249">**PlugAndPlayDevicesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-250">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-252">Указывает, будет ли отключено перенаправление устройств самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="47859-252">Indicates if redirection of Plug and Play devices will be disabled.</span></span> <span data-ttu-id="47859-253">Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="47859-253">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="47859-254">**принтерсдисаблед**</span><span class="sxs-lookup"><span data-stu-id="47859-254">**PrintersDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-255">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-257">Указывает, будет ли перенаправление принтера отключено.</span><span class="sxs-lookup"><span data-stu-id="47859-257">Indicates if printer redirection will be disabled.</span></span> <span data-ttu-id="47859-258">Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="47859-258">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="47859-259">**секуреидалловед**</span><span class="sxs-lookup"><span data-stu-id="47859-259">**SecureIdAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-260">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-260">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-262">Указывает, можно ли использовать безопасный идентификатор для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47859-262">Indicates if a secure identifier can be used to connect to the RD Gateway server.</span></span>

<span data-ttu-id="47859-263">**Windows Server 2008:** Это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="47859-263">**Windows Server 2008:** This property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="47859-264">**сериалпортсдисаблед**</span><span class="sxs-lookup"><span data-stu-id="47859-264">**SerialPortsDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-265">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-267">Указывает, будет ли перенаправление последовательного порта отключено.</span><span class="sxs-lookup"><span data-stu-id="47859-267">Indicates if serial port redirection will be disabled.</span></span> <span data-ttu-id="47859-268">Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="47859-268">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="47859-269">**SessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="47859-269">**SessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-270">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47859-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47859-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-272">Значение времени ожидания сеанса в минутах.</span><span class="sxs-lookup"><span data-stu-id="47859-272">The session timeout value, in minutes.</span></span> <span data-ttu-id="47859-273">Значение 0 означает отсутствие времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="47859-273">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="47859-274">Это свойство можно задать с помощью метода [**сетсессионтимеаут**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="47859-274">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="47859-275">**Windows Server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="47859-275">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="47859-276">**сессионтимеаутактион**</span><span class="sxs-lookup"><span data-stu-id="47859-276">**SessionTimeoutAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-277">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47859-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47859-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-279">Задает действие, выполняемое в случае истечения времени ожидания сеанса.</span><span class="sxs-lookup"><span data-stu-id="47859-279">Specifies the action to be taken in the case of a session timeout.</span></span> <span data-ttu-id="47859-280">Это свойство можно задать с помощью метода [**сетсессионтимеаут**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="47859-280">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="47859-281">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="47859-281">This can be one of the following values.</span></span>

<span data-ttu-id="47859-282">**Windows Server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="47859-282">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="47859-283">0</span><span class="sxs-lookup"><span data-stu-id="47859-283">0</span></span>
</dt> <dd>

<span data-ttu-id="47859-284">Отключите сеанс.</span><span class="sxs-lookup"><span data-stu-id="47859-284">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="47859-285">1</span><span class="sxs-lookup"><span data-stu-id="47859-285">1</span></span>
</dt> <dd>

<span data-ttu-id="47859-286">Попытка повторно авторизовать сеанс.</span><span class="sxs-lookup"><span data-stu-id="47859-286">Attempt to re-authorize the session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47859-287">**смарткардалловед**</span><span class="sxs-lookup"><span data-stu-id="47859-287">**SmartcardAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-288">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47859-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47859-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-290">Указывает, можно ли использовать смарт-карту для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47859-290">Indicates if a smart card can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="47859-291">Это свойство можно изменить с помощью метода [**сетсмарткардалловед**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="47859-291">This property can be changed by using the [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="47859-292">**усерграупнамес**</span><span class="sxs-lookup"><span data-stu-id="47859-292">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47859-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47859-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47859-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47859-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47859-295">Список имен групп пользователей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="47859-295">List of semicolon-separated user group names.</span></span> <span data-ttu-id="47859-296">Имена имеют формат *домена \\ усерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="47859-296">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="47859-297">Если пользователь принадлежит к любой из этих групп пользователей, ему будет разрешен доступ к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="47859-297">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47859-298">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47859-298">Remarks</span></span>

<span data-ttu-id="47859-299">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="47859-299">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="47859-300">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="47859-300">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="47859-301">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="47859-301">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="47859-302">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="47859-302">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="47859-303">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="47859-303">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="47859-304">Требования</span><span class="sxs-lookup"><span data-stu-id="47859-304">Requirements</span></span>



| <span data-ttu-id="47859-305">Требование</span><span class="sxs-lookup"><span data-stu-id="47859-305">Requirement</span></span> | <span data-ttu-id="47859-306">Значение</span><span class="sxs-lookup"><span data-stu-id="47859-306">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47859-307">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47859-307">Minimum supported client</span></span><br/> | <span data-ttu-id="47859-308">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="47859-308">None supported</span></span><br/>                                                                |
| <span data-ttu-id="47859-309">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47859-309">Minimum supported server</span></span><br/> | <span data-ttu-id="47859-310">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47859-310">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="47859-311">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="47859-311">Namespace</span></span><br/>                | <span data-ttu-id="47859-312">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="47859-312">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="47859-313">MOF</span><span class="sxs-lookup"><span data-stu-id="47859-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47859-314"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47859-314"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="47859-315">DLL</span><span class="sxs-lookup"><span data-stu-id="47859-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47859-316"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47859-316"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="47859-317">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47859-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47859-318">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="47859-318">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="47859-319">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="47859-319">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="47859-320">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="47859-320">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="47859-321">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="47859-321">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="47859-322">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="47859-322">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="47859-323">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="47859-323">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

