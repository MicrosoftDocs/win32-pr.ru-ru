---
title: Класс Win32_TSGatewayServerSettings
description: Предоставляет методы и свойства для просмотра и настройки параметров сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayServerSettings, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492705"
---
# <a name="win32_tsgatewayserversettings-class"></a><span data-ttu-id="1850b-105">\_Класс Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="1850b-105">Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="1850b-106">Предоставляет методы и свойства для просмотра и настройки параметров сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="1850b-106">Provides methods and properties to view and configure Remote Desktop Gateway (RD Gateway) server settings.</span></span> <span data-ttu-id="1850b-107">Администратор может использовать этот класс для настройки набора протоколов, набора событий, которые будут записываться в журнал событий, и максимального числа подключений через шлюз удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-107">An administrator can use this class to configure a set of protocols, the set of events that will be written to the event log, and the maximum number of connections through RD Gateway.</span></span>

## <a name="syntax"></a><span data-ttu-id="1850b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1850b-108">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a><span data-ttu-id="1850b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1850b-109">Members</span></span>

<span data-ttu-id="1850b-110">Класс **Win32 \_ тсгатевайсерверсеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1850b-110">The **Win32\_TSGatewayServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="1850b-111">Методы</span><span class="sxs-lookup"><span data-stu-id="1850b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1850b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1850b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1850b-113">Методы</span><span class="sxs-lookup"><span data-stu-id="1850b-113">Methods</span></span>

<span data-ttu-id="1850b-114">Класс **Win32 \_ тсгатевайсерверсеттингс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1850b-114">The **Win32\_TSGatewayServerSettings** class has these methods.</span></span>



| <span data-ttu-id="1850b-115">Метод</span><span class="sxs-lookup"><span data-stu-id="1850b-115">Method</span></span>                                                                                                                                             | <span data-ttu-id="1850b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1850b-116">Description</span></span>                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1850b-117">**Configure**</span><span class="sxs-lookup"><span data-stu-id="1850b-117">**Configure**</span></span>](configure-win32-tsgatewayserversettings.md)                                                                                       | <span data-ttu-id="1850b-118">Настраивает параметры IIS и RPC, необходимые для службы шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-118">Configures the IIS and RPC settings required by the RD Gateway service.</span></span><br/> <span data-ttu-id="1850b-119">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-119">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                               |
| [<span data-ttu-id="1850b-120">**енаблецентралкап**</span><span class="sxs-lookup"><span data-stu-id="1850b-120">**EnableCentralCAP**</span></span>](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="1850b-121">Включает или отключает свойство **централкапенаблед** , которое определяет, используются ли центральные серверы политики авторизации удаленный рабочий стол подключений (RD CAP) для управления политиками авторизации подключений для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="1850b-121">Enables or disables the **CentralCAPEnabled** property, which controls whether central Remote Desktop connection authorization policy (RD CAP) servers are used for controlling connection authorization policies for this server.</span></span><br/>                    |
| [<span data-ttu-id="1850b-122">**енаблеложевент**</span><span class="sxs-lookup"><span data-stu-id="1850b-122">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="1850b-123">Включает или отключает ведение журнала для указанного типа событий.</span><span class="sxs-lookup"><span data-stu-id="1850b-123">Enables or disables logging of the specified event type.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="1850b-124">**енаблеонликонсенткапаблеклиентс**</span><span class="sxs-lookup"><span data-stu-id="1850b-124">**EnableOnlyConsentCapableClients**</span></span>](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | <span data-ttu-id="1850b-125">Задает свойство **онликонсенткапаблеклиентс** .</span><span class="sxs-lookup"><span data-stu-id="1850b-125">Sets the **OnlyConsentCapableClients** property.</span></span><br/> <span data-ttu-id="1850b-126">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-126">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="1850b-127">**енаблерекуестсох**</span><span class="sxs-lookup"><span data-stu-id="1850b-127">**EnableRequestSOH**</span></span>](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | <span data-ttu-id="1850b-128">Этот метод не поддерживается начиная с Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="1850b-128">This method is not supported starting with Windows Server 2016.</span></span><br/> <span data-ttu-id="1850b-129">**Windows server 2012 R2, Windows server 2012, Windows server 2008 R2 и Windows server 2008:** Включает или отключает запросы состояния работоспособности (SoH).</span><span class="sxs-lookup"><span data-stu-id="1850b-129">**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:** Enables or disables requests for a Statement of Health (SoH).</span></span><br/> <br/> |
| [<span data-ttu-id="1850b-130">**енаблетранспорт**</span><span class="sxs-lookup"><span data-stu-id="1850b-130">**EnableTransport**</span></span>](enabletransport-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="1850b-131">Включает или отключает указанный транспорт.</span><span class="sxs-lookup"><span data-stu-id="1850b-131">Enables or disables the specified transport.</span></span><br/> <span data-ttu-id="1850b-132">**Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до выхода Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="1850b-132">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="1850b-133">**енумаусентикатионплугинс**</span><span class="sxs-lookup"><span data-stu-id="1850b-133">**EnumAuthenticationPlugins**</span></span>](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | <span data-ttu-id="1850b-134">Перечисляет все зарегистрированные подключаемые модули проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1850b-134">Enumerates all registered authentication plug-ins.</span></span><br/> <span data-ttu-id="1850b-135">**Windows Server 2008:** Этот метод недоступен.</span><span class="sxs-lookup"><span data-stu-id="1850b-135">**Windows Server 2008:** This method is not available.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="1850b-136">**енумаусоризатионплугинс**</span><span class="sxs-lookup"><span data-stu-id="1850b-136">**EnumAuthorizationPlugins**</span></span>](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="1850b-137">Перечисляет все зарегистрированные подключаемые модули авторизации.</span><span class="sxs-lookup"><span data-stu-id="1850b-137">Enumerates all registered authorization plug-ins.</span></span><br/> <span data-ttu-id="1850b-138">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="1850b-139">**жетипандпорт**</span><span class="sxs-lookup"><span data-stu-id="1850b-139">**GetIPAndPort**</span></span>](getipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="1850b-140">Получает IP-адрес прослушивания и номер порта для указанного транспорта.</span><span class="sxs-lookup"><span data-stu-id="1850b-140">Obtains the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="1850b-141">**Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до выхода Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="1850b-141">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                 |
| [<span data-ttu-id="1850b-142">**жетложевентнаме**</span><span class="sxs-lookup"><span data-stu-id="1850b-142">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="1850b-143">Возвращает имя события журнала для указанного индекса событий журнала.</span><span class="sxs-lookup"><span data-stu-id="1850b-143">Returns the log event name for the specified log event index.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="1850b-144">**жетпротоколнаме**</span><span class="sxs-lookup"><span data-stu-id="1850b-144">**GetProtocolName**</span></span>](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="1850b-145">Возвращает имя протокола для указанного индекса протокола.</span><span class="sxs-lookup"><span data-stu-id="1850b-145">Returns the protocol name for the specified protocol index.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="1850b-146">**исложевентенаблед**</span><span class="sxs-lookup"><span data-stu-id="1850b-146">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="1850b-147">Указывает, включен ли указанный тип журнала событий.</span><span class="sxs-lookup"><span data-stu-id="1850b-147">Indicates whether the specified event log type is enabled.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="1850b-148">**истранспортенаблед**</span><span class="sxs-lookup"><span data-stu-id="1850b-148">**IsTransportEnabled**</span></span>](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="1850b-149">Определяет, включен ли указанный транспорт.</span><span class="sxs-lookup"><span data-stu-id="1850b-149">Determines whether the specified transport is enabled.</span></span><br/> <span data-ttu-id="1850b-150">**Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до выхода Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="1850b-150">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                        |
| [<span data-ttu-id="1850b-151">**куерицертконтекст**</span><span class="sxs-lookup"><span data-stu-id="1850b-151">**QueryCertContext**</span></span>](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | <span data-ttu-id="1850b-152">Указывает, установлен ли указанный сертификат.</span><span class="sxs-lookup"><span data-stu-id="1850b-152">Indicates whether the specified certificate is installed.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="1850b-153">**рециклерпкаппликатионпулс**</span><span class="sxs-lookup"><span data-stu-id="1850b-153">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | <span data-ttu-id="1850b-154">Повторное использование пулов приложений RPC в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="1850b-154">Recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="1850b-155">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-155">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="1850b-156">**рефрешцертконтекст**</span><span class="sxs-lookup"><span data-stu-id="1850b-156">**RefreshCertContext**</span></span>](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | <span data-ttu-id="1850b-157">Обновляет сертификат, используемый сервером шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-157">Refreshes the certificate that is used by the RD Gateway server.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="1850b-158">**сетаусентикатионплугин**</span><span class="sxs-lookup"><span data-stu-id="1850b-158">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | <span data-ttu-id="1850b-159">Задает текущий подключаемый модуль проверки подлинности для сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-159">Sets the current authentication plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="1850b-160">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-160">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="1850b-161">**сетаусентикатионплугинандрециклерпкаппликатионпулс**</span><span class="sxs-lookup"><span data-stu-id="1850b-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span></span>](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | <span data-ttu-id="1850b-162">Задает текущий подключаемый модуль проверки подлинности для сервера шлюза удаленных рабочих столов и выполняет повторный запуск пулов приложений RPC в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="1850b-162">Sets the current authentication plug-in for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="1850b-163">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-163">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                      |
| [<span data-ttu-id="1850b-164">**сетаусоризатионплугин**</span><span class="sxs-lookup"><span data-stu-id="1850b-164">**SetAuthorizationPlugin**</span></span>](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | <span data-ttu-id="1850b-165">Задает текущий подключаемый модуль авторизации для сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-165">Sets the current authorization plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="1850b-166">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-166">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                     |
| [<span data-ttu-id="1850b-167">**сетцертификате**</span><span class="sxs-lookup"><span data-stu-id="1850b-167">**SetCertificate**</span></span>](setcertificate-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="1850b-168">Задает хэш сертификата для привязки HTTPS через порт 443 в IIS.</span><span class="sxs-lookup"><span data-stu-id="1850b-168">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span><br/> <span data-ttu-id="1850b-169">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                       |
| [<span data-ttu-id="1850b-170">**сетцертификатеакл**</span><span class="sxs-lookup"><span data-stu-id="1850b-170">**SetCertificateACL**</span></span>](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="1850b-171">Задает списки управления доступом (ACL) сертификатов для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="1850b-171">Sets the certificate access control lists (ACLs) for this server.</span></span><br/>                                                                                                                                                                                     |
| [<span data-ttu-id="1850b-172">**сетдефаултплугинсандрециклерпкаппликатионпулс**</span><span class="sxs-lookup"><span data-stu-id="1850b-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span></span>](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | <span data-ttu-id="1850b-173">Задает текущие подключаемые модули проверки подлинности и авторизации для сервера шлюза удаленных рабочих столов и выполняет повторный запуск пулов приложений RPC в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="1850b-173">Sets the current authentication and authorization plug-ins for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="1850b-174">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-174">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                   |
| [<span data-ttu-id="1850b-175">**сетенфорцечаннелбиндинг**</span><span class="sxs-lookup"><span data-stu-id="1850b-175">**SetEnforceChannelBinding**</span></span>](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="1850b-176">Задает свойство **енфорцечаннелбиндинг** .</span><span class="sxs-lookup"><span data-stu-id="1850b-176">Sets the **EnforceChannelBinding** property.</span></span><br/> <span data-ttu-id="1850b-177">**Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до выхода Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="1850b-177">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="1850b-178">**сетипандпорт**</span><span class="sxs-lookup"><span data-stu-id="1850b-178">**SetIPAndPort**</span></span>](setipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="1850b-179">Задает IP-адрес прослушивания и номер порта для указанного транспорта.</span><span class="sxs-lookup"><span data-stu-id="1850b-179">Sets the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="1850b-180">**Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до выхода Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="1850b-180">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                    |
| [<span data-ttu-id="1850b-181">**сетмаксконнектионс**</span><span class="sxs-lookup"><span data-stu-id="1850b-181">**SetMaxConnections**</span></span>](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="1850b-182">Задает максимальное число разрешенных подключений через шлюз удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-182">Sets the maximum number of allowed connections through RD Gateway.</span></span> <span data-ttu-id="1850b-183">Этот метод изменяет свойства **MaxConnections** и **унлимитедконнектионс** .</span><span class="sxs-lookup"><span data-stu-id="1850b-183">This method changes the **MaxConnections** and **UnlimitedConnections** properties.</span></span><br/>                                                                                                |
| [<span data-ttu-id="1850b-184">**сетсслбридгинг**</span><span class="sxs-lookup"><span data-stu-id="1850b-184">**SetSslBridging**</span></span>](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="1850b-185">Задает тип моста SSL, который будет использоваться сервером шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-185">Sets the type of SSL bridging to be used by the RD Gateway server.</span></span><br/> <span data-ttu-id="1850b-186">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-186">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="1850b-187">**тсгремовеадминмсг**</span><span class="sxs-lookup"><span data-stu-id="1850b-187">**TSGRemoveAdminMsg**</span></span>](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="1850b-188">Удаляет административное сообщение для сервера шлюза.</span><span class="sxs-lookup"><span data-stu-id="1850b-188">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="1850b-189">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-189">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="1850b-190">**тсгремовеконсентмсг**</span><span class="sxs-lookup"><span data-stu-id="1850b-190">**TSGRemoveConsentMsg**</span></span>](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | <span data-ttu-id="1850b-191">Удаляет административное сообщение для сервера шлюза.</span><span class="sxs-lookup"><span data-stu-id="1850b-191">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="1850b-192">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-192">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="1850b-193">**тсгстореадминмсг**</span><span class="sxs-lookup"><span data-stu-id="1850b-193">**TSGStoreAdminMsg**</span></span>](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="1850b-194">Обновляет административное сообщение для сервера шлюза.</span><span class="sxs-lookup"><span data-stu-id="1850b-194">Updates the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="1850b-195">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-195">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="1850b-196">**тсгстореконсентмсг**</span><span class="sxs-lookup"><span data-stu-id="1850b-196">**TSGStoreConsentMsg**</span></span>](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="1850b-197">Обновляет сообщение согласия для сервера шлюза.</span><span class="sxs-lookup"><span data-stu-id="1850b-197">Updates the consent message for the gateway server.</span></span><br/> <span data-ttu-id="1850b-198">**Windows Server 2008:** Этот метод недоступен до выхода Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-198">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="1850b-199">Свойства</span><span class="sxs-lookup"><span data-stu-id="1850b-199">Properties</span></span>

<span data-ttu-id="1850b-200">Класс **Win32 \_ тсгатевайсерверсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1850b-200">The **Win32\_TSGatewayServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1850b-201">**админмессажеендтиме**</span><span class="sxs-lookup"><span data-stu-id="1850b-201">**adminMessageEndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-204">Время окончания административного сообщения.</span><span class="sxs-lookup"><span data-stu-id="1850b-204">The administrative message end time.</span></span>

<span data-ttu-id="1850b-205">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-205">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-206">**админмессажестарттиме**</span><span class="sxs-lookup"><span data-stu-id="1850b-206">**adminMessageStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-209">Время начала административного сообщения.</span><span class="sxs-lookup"><span data-stu-id="1850b-209">The administrative message start time.</span></span>

<span data-ttu-id="1850b-210">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-210">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-211">**админмессажетекст**</span><span class="sxs-lookup"><span data-stu-id="1850b-211">**adminMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-212">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-214">Текст административного сообщения.</span><span class="sxs-lookup"><span data-stu-id="1850b-214">The administrative message text.</span></span>

<span data-ttu-id="1850b-215">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-215">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-216">**аусентикатионплугинклсид**</span><span class="sxs-lookup"><span data-stu-id="1850b-216">**AuthenticationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-219">Идентификатор CLSID текущего подключаемого модуля проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1850b-219">The CLSID of the current authentication plug-in.</span></span>

<span data-ttu-id="1850b-220">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-220">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-221">**аусентикатионплугиндескриптион**</span><span class="sxs-lookup"><span data-stu-id="1850b-221">**AuthenticationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-224">Описание текущего подключаемого модуля проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1850b-224">The description of the current authentication plug-in.</span></span>

<span data-ttu-id="1850b-225">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-225">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-226">**аусентикатионплугиннаме**</span><span class="sxs-lookup"><span data-stu-id="1850b-226">**AuthenticationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-229">Имя текущего подключаемого модуля проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1850b-229">The name of the current authentication plug-in.</span></span>

<span data-ttu-id="1850b-230">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-230">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-231">**аусоризатионплугинклсид**</span><span class="sxs-lookup"><span data-stu-id="1850b-231">**AuthorizationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-234">Идентификатор CLSID текущего подключаемого модуля авторизации.</span><span class="sxs-lookup"><span data-stu-id="1850b-234">The CLSID of the current authorization plug-in.</span></span>

<span data-ttu-id="1850b-235">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-235">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-236">**аусоризатионплугиндескриптион**</span><span class="sxs-lookup"><span data-stu-id="1850b-236">**AuthorizationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-239">Описание текущего подключаемого модуля авторизации.</span><span class="sxs-lookup"><span data-stu-id="1850b-239">The description of the current authorization plug-in.</span></span>

<span data-ttu-id="1850b-240">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-240">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-241">**аусоризатионплугиннаме**</span><span class="sxs-lookup"><span data-stu-id="1850b-241">**AuthorizationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-244">Имя текущего подключаемого модуля авторизации.</span><span class="sxs-lookup"><span data-stu-id="1850b-244">The name of the current authorization plug-in.</span></span>

<span data-ttu-id="1850b-245">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-245">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-246">**централкапенаблед**</span><span class="sxs-lookup"><span data-stu-id="1850b-246">**CentralCAPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-247">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1850b-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-249">Указывает, используются ли центральные серверы ограниченного использования удаленных рабочих столов для управления этим сервером.</span><span class="sxs-lookup"><span data-stu-id="1850b-249">Specifies whether central RD CAP servers are used for controlling this server.</span></span> <span data-ttu-id="1850b-250">Это свойство можно изменить, вызвав метод [**енаблецентралкап**](enablecentralcap-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="1850b-250">This property can be changed by calling the [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-251">**CertHash**</span><span class="sxs-lookup"><span data-stu-id="1850b-251">**CertHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-252">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1850b-252">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1850b-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-254">Указывает хэш сертификата для привязки HTTPS через порт 443 в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="1850b-254">Specifies the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

<span data-ttu-id="1850b-255">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-255">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-256">**консентмессажетекст**</span><span class="sxs-lookup"><span data-stu-id="1850b-256">**consentMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-259">Текст сообщения согласия.</span><span class="sxs-lookup"><span data-stu-id="1850b-259">The consent message text.</span></span>

<span data-ttu-id="1850b-260">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-260">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-261">**енфорцечаннелбиндинг**</span><span class="sxs-lookup"><span data-stu-id="1850b-261">**EnforceChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-262">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1850b-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-264">Указывает, применяется ли привязка канала для транспорта HTTP.</span><span class="sxs-lookup"><span data-stu-id="1850b-264">Indicates if channel binding is enforced for the HTTP transport.</span></span> <span data-ttu-id="1850b-265">Это значение свойства можно изменить с помощью метода [**сетенфорцечаннелбиндинг**](setenforcechannelbinding-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="1850b-265">This property value can be changed by using the [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) method.</span></span>

<span data-ttu-id="1850b-266">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно до Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="1850b-266">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available before Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-267">**Флажка IsConfigured**</span><span class="sxs-lookup"><span data-stu-id="1850b-267">**IsConfigured**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-268">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1850b-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-270">Указывает, настроены ли параметры IIS и RPC, необходимые для службы шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-270">Specifies if IIS and RPC settings required by the RD Gateway service are configured.</span></span>

<span data-ttu-id="1850b-271">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-271">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-272">**MaxConnections**</span><span class="sxs-lookup"><span data-stu-id="1850b-272">**MaxConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-273">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1850b-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1850b-275">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1850b-275">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1850b-276">Возвращает максимальное число подключений, разрешенных через шлюз удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-276">Returns the maximum number of connections that are allowed through RD Gateway.</span></span> <span data-ttu-id="1850b-277">Это свойство можно задать с помощью метода [**сетмаксконнектионс**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="1850b-277">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-278">**максимумалловедконнектионсбиску**</span><span class="sxs-lookup"><span data-stu-id="1850b-278">**MaximumAllowedConnectionsBySku**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-279">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1850b-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-281">Максимальное число подключений, разрешенное модулем хранения запасов (SKU).</span><span class="sxs-lookup"><span data-stu-id="1850b-281">Maximum number of connections that the stock-keeping unit (SKU) allows.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-282">**максложевентс**</span><span class="sxs-lookup"><span data-stu-id="1850b-282">**MaxLogEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-283">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1850b-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-285">Возвращает максимальное число событий журнала.</span><span class="sxs-lookup"><span data-stu-id="1850b-285">Returns the maximum number of log events.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-286">**макспротоколс**</span><span class="sxs-lookup"><span data-stu-id="1850b-286">**MaxProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-287">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1850b-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-289">Число протоколов, поддерживаемых шлюзом удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-289">Number of protocols supported by RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-290">**онликонсенткапаблеклиентс**</span><span class="sxs-lookup"><span data-stu-id="1850b-290">**OnlyConsentCapableClients**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-291">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1850b-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-293">Указывает, разрешено ли подключение к шлюзу удаленных рабочих столов только клиентам, которым могут быть предоставлены сообщения согласия.</span><span class="sxs-lookup"><span data-stu-id="1850b-293">Specifies if only clients capable of consent messages are allowed to connect to the RD Gateway.</span></span>

<span data-ttu-id="1850b-294">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-294">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="1850b-295">отличные</span><span class="sxs-lookup"><span data-stu-id="1850b-295">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="1850b-296">Подключаться могут только клиенты, поддерживающие сообщения согласия.</span><span class="sxs-lookup"><span data-stu-id="1850b-296">Only consent message capable clients can connect.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-297">нуль</span><span class="sxs-lookup"><span data-stu-id="1850b-297">zero</span></span>
</dt> <dd>

<span data-ttu-id="1850b-298">Клиенты, не поддерживающие сообщение согласия, могут также подключаться.</span><span class="sxs-lookup"><span data-stu-id="1850b-298">Clients that are not consent message capable can also connect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1850b-299">**рекуестсох**</span><span class="sxs-lookup"><span data-stu-id="1850b-299">**RequestSOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-300">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1850b-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-302">Это свойство не поддерживается начиная с Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="1850b-302">This property is not supported starting with Windows Server 2016.</span></span>

<span data-ttu-id="1850b-303">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 и Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="1850b-303">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="1850b-304">Указывает, должен ли сервер запросить состояние работоспособности (SoH) от клиента.</span><span class="sxs-lookup"><span data-stu-id="1850b-304">Specifies whether the server must request a Statement of Health (SoH) from the client.</span></span> <span data-ttu-id="1850b-305">Это свойство можно изменить с помощью метода [**енаблерекуестсох**](win32-tsgatewayserversettings-enablerequestsoh.md) .</span><span class="sxs-lookup"><span data-stu-id="1850b-305">This property can be changed by using the [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-306">**SkuName**</span><span class="sxs-lookup"><span data-stu-id="1850b-306">**SkuName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1850b-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-309">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="1850b-309">Name of the SKU.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-310">**сслбридгинг**</span><span class="sxs-lookup"><span data-stu-id="1850b-310">**SslBridging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-311">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1850b-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-313">Указывает тип моста SSL, который будет использоваться сервером шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-313">Specifies which type of SSL bridging to be used by the RD Gateway server.</span></span> <span data-ttu-id="1850b-314">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1850b-314">This can be one of the following values.</span></span>

<span data-ttu-id="1850b-315">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1850b-315">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="1850b-316">0</span><span class="sxs-lookup"><span data-stu-id="1850b-316">0</span></span>
</dt> <dd>

<span data-ttu-id="1850b-317">Мост SSL отсутствует.</span><span class="sxs-lookup"><span data-stu-id="1850b-317">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-318">1</span><span class="sxs-lookup"><span data-stu-id="1850b-318">1</span></span>
</dt> <dd>

<span data-ttu-id="1850b-319">Мост HTTPS для HTTP.</span><span class="sxs-lookup"><span data-stu-id="1850b-319">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="1850b-320">2</span><span class="sxs-lookup"><span data-stu-id="1850b-320">2</span></span>
</dt> <dd>

<span data-ttu-id="1850b-321">Мост HTTPS для HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1850b-321">HTTPS to HTTPS bridging.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1850b-322">**унлимитедконнектионс**</span><span class="sxs-lookup"><span data-stu-id="1850b-322">**UnlimitedConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1850b-323">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1850b-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1850b-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1850b-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1850b-325">Указывает, разрешено ли неограниченное число подключений через шлюз удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1850b-325">Indicates whether an unlimited number of connections are allowed through RD Gateway.</span></span> <span data-ttu-id="1850b-326">Это свойство можно задать с помощью метода [**сетмаксконнектионс**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="1850b-326">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1850b-327">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1850b-327">Remarks</span></span>

<span data-ttu-id="1850b-328">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="1850b-328">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="1850b-329">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="1850b-329">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1850b-330">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="1850b-330">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1850b-331">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="1850b-331">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1850b-332">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1850b-332">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1850b-333">Требования</span><span class="sxs-lookup"><span data-stu-id="1850b-333">Requirements</span></span>



| <span data-ttu-id="1850b-334">Требование</span><span class="sxs-lookup"><span data-stu-id="1850b-334">Requirement</span></span> | <span data-ttu-id="1850b-335">Значение</span><span class="sxs-lookup"><span data-stu-id="1850b-335">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1850b-336">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1850b-336">Minimum supported client</span></span><br/> | <span data-ttu-id="1850b-337">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1850b-337">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1850b-338">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1850b-338">Minimum supported server</span></span><br/> | <span data-ttu-id="1850b-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1850b-339">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1850b-340">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1850b-340">Namespace</span></span><br/>                | <span data-ttu-id="1850b-341">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="1850b-341">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1850b-342">MOF</span><span class="sxs-lookup"><span data-stu-id="1850b-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1850b-343"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-343"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1850b-344">DLL</span><span class="sxs-lookup"><span data-stu-id="1850b-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1850b-345"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1850b-345"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1850b-346">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1850b-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1850b-347">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="1850b-347">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="1850b-348">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="1850b-348">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="1850b-349">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="1850b-349">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="1850b-350">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="1850b-350">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="1850b-351">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="1850b-351">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="1850b-352">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="1850b-352">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

