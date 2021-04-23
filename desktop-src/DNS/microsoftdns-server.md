---
title: Класс MicrosoftDNS_Server
description: '\_Класс сервера микрософтднс описывает DNS-сервер. Каждый экземпляр этого класса может быть связан с одним экземпляром кэша Микрософтднс \_ , одним экземпляром микрософтднс \_ русинтс и несколькими экземплярами \_ зоны микрософтднс.'
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- DNS класса MicrosoftDNS_Server
- DNS-MicrosoftDNS_Server класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988264"
---
# <a name="microsoftdns_server-class"></a><span data-ttu-id="aaf05-106">\_Класс сервера микрософтднс</span><span class="sxs-lookup"><span data-stu-id="aaf05-106">MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="aaf05-107">Класс **\_ сервера микрософтднс** описывает DNS-сервер.</span><span class="sxs-lookup"><span data-stu-id="aaf05-107">The **MicrosoftDNS\_Server** class describes a DNS Server.</span></span> <span data-ttu-id="aaf05-108">Каждый экземпляр этого класса может быть связан с одним экземпляром [**\_ кэша микрософтднс**](microsoftdns-cache.md), одним экземпляром [**микрософтднс \_ русинтс**](microsoftdns-roothints.md)и несколькими экземплярами [**\_ зоны микрософтднс**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="aaf05-108">Every instance of this class may be associated with one instance of [**MicrosoftDNS\_Cache**](microsoftdns-cache.md), one instance of [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md), and multiple instances of [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

<span data-ttu-id="aaf05-109">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="aaf05-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf05-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aaf05-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a><span data-ttu-id="aaf05-111">Члены</span><span class="sxs-lookup"><span data-stu-id="aaf05-111">Members</span></span>

<span data-ttu-id="aaf05-112">Класс **\_ сервера микрософтднс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="aaf05-112">The **MicrosoftDNS\_Server** class has these types of members:</span></span>

-   [<span data-ttu-id="aaf05-113">Методы</span><span class="sxs-lookup"><span data-stu-id="aaf05-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="aaf05-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="aaf05-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aaf05-115">Методы</span><span class="sxs-lookup"><span data-stu-id="aaf05-115">Methods</span></span>

<span data-ttu-id="aaf05-116">Класс **\_ сервера микрософтднс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-116">The **MicrosoftDNS\_Server** class has these methods.</span></span>



| <span data-ttu-id="aaf05-117">Метод</span><span class="sxs-lookup"><span data-stu-id="aaf05-117">Method</span></span>                   | <span data-ttu-id="aaf05-118">Описание</span><span class="sxs-lookup"><span data-stu-id="aaf05-118">Description</span></span>                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| <span data-ttu-id="aaf05-119">**жетдистингуишеднаме**</span><span class="sxs-lookup"><span data-stu-id="aaf05-119">**GetDistinguishedName**</span></span> | <span data-ttu-id="aaf05-120">Извлекает различающееся имя DNS для зоны.</span><span class="sxs-lookup"><span data-stu-id="aaf05-120">Retrieves DNS distinguished name for the zone.</span></span><br/>                        |
| <span data-ttu-id="aaf05-121">**стартскавенгинг**</span><span class="sxs-lookup"><span data-stu-id="aaf05-121">**StartScavenging**</span></span>      | <span data-ttu-id="aaf05-122">Запускает очистку устаревших записей в зонах, подлежащим очистке.</span><span class="sxs-lookup"><span data-stu-id="aaf05-122">Starts scavenging stale records in the zones subjected to scavenging.</span></span><br/> |
| <span data-ttu-id="aaf05-123">**StartService**</span><span class="sxs-lookup"><span data-stu-id="aaf05-123">**StartService**</span></span>         | <span data-ttu-id="aaf05-124">Запускает DNS-сервер.</span><span class="sxs-lookup"><span data-stu-id="aaf05-124">Starts the DNS Server.</span></span><br/>                                                |
| <span data-ttu-id="aaf05-125">**StopService**</span><span class="sxs-lookup"><span data-stu-id="aaf05-125">**StopService**</span></span>          | <span data-ttu-id="aaf05-126">Останавливает DNS-сервер.</span><span class="sxs-lookup"><span data-stu-id="aaf05-126">Stops the DNS Server.</span></span><br/>                                                 |



 

### <a name="properties"></a><span data-ttu-id="aaf05-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="aaf05-127">Properties</span></span>

<span data-ttu-id="aaf05-128">Класс **\_ сервера микрософтднс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="aaf05-128">The **MicrosoftDNS\_Server** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aaf05-129">**аддрессансверлимит**</span><span class="sxs-lookup"><span data-stu-id="aaf05-129">**AddressAnswerLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-132">Максимальное число записей узлов, возвращаемых в ответ на запрос адреса.</span><span class="sxs-lookup"><span data-stu-id="aaf05-132">Maximum number of host records returned in response to an address request.</span></span> <span data-ttu-id="aaf05-133">Допустимы значения от 5 до 28.</span><span class="sxs-lookup"><span data-stu-id="aaf05-133">Values between 5 and 28 are valid.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-134">**алловупдате**</span><span class="sxs-lookup"><span data-stu-id="aaf05-134">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-137">Указывает, принимает ли DNS-сервер запросы на динамическое обновление.</span><span class="sxs-lookup"><span data-stu-id="aaf05-137">Specifies whether the DNS Server accepts dynamic update requests.</span></span> <span data-ttu-id="aaf05-138">Допустимые значения представлены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="aaf05-138">Valid values are as shown in the following table.</span></span>



| <span data-ttu-id="aaf05-139">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-139">Value</span></span>                                                                                                | <span data-ttu-id="aaf05-140">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-140">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="aaf05-141"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-141"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="aaf05-142">Без ограничений.</span><span class="sxs-lookup"><span data-stu-id="aaf05-142">No Restrictions.</span></span><br/>                                                                           |
| <span id="1"></span><dl> <span data-ttu-id="aaf05-143"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-143"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="aaf05-144">Не допускает динамическое обновление записей SOA.</span><span class="sxs-lookup"><span data-stu-id="aaf05-144">Does not allow dynamic updates of SOA records.</span></span><br/>                                             |
| <span id="2"></span><dl> <span data-ttu-id="aaf05-145"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-145"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="aaf05-146">Не допускает динамическое обновление записей NS в корне зоны.</span><span class="sxs-lookup"><span data-stu-id="aaf05-146">Does not allow dynamic updates of NS records at the zone root.</span></span><br/>                             |
| <span id="4"></span><dl> <span data-ttu-id="aaf05-147"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-147"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="aaf05-148">Не допускает динамическое обновление записей NS, которые не находятся в корне зоны (записи делегирования NS).</span><span class="sxs-lookup"><span data-stu-id="aaf05-148">Does not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span><br/> |



 

<span data-ttu-id="aaf05-149">Вычислите эти значения, чтобы определить значение параметра.</span><span class="sxs-lookup"><span data-stu-id="aaf05-149">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-150">**аутокачеупдате**</span><span class="sxs-lookup"><span data-stu-id="aaf05-150">**AutoCacheUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-151">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-153">Указывает, пытается ли DNS-сервер обновить свои записи кэша с помощью данных из корневых серверов.</span><span class="sxs-lookup"><span data-stu-id="aaf05-153">Indicates whether the DNS Server attempts to update its cache entries using data from root servers.</span></span> <span data-ttu-id="aaf05-154">Когда DNS-сервер загружается, ему нужен список записей NS для корневого сервера, а также записи для серверов, которые исторически называли файлом кэша.</span><span class="sxs-lookup"><span data-stu-id="aaf05-154">When a DNS Server boots, it needs a list of root server 'hints' NS and A records for the servers historically called the cache file.</span></span> <span data-ttu-id="aaf05-155">DNS-серверы Майкрософт имеют функцию, которая позволяет им попытаться записать новый файл кэша на основе ответов от корневых серверов.</span><span class="sxs-lookup"><span data-stu-id="aaf05-155">Microsoft DNS Servers have a feature that enables them to attempt to write back a new cache file based on the responses from root servers.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-156">**аутоконфигфилезонес**</span><span class="sxs-lookup"><span data-stu-id="aaf05-156">**AutoConfigFileZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-159">Указывает, какие стандартные основные зоны, полномочные для имени DNS-сервера, должны обновляться при изменении сервера имен.</span><span class="sxs-lookup"><span data-stu-id="aaf05-159">Indicates which standard primary zones that are authoritative for the name of the DNS Server must be updated when the name server changes.</span></span> <span data-ttu-id="aaf05-160">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="aaf05-160">Valid values are as follows:</span></span>



| <span data-ttu-id="aaf05-161">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-161">Value</span></span>                                                                                                | <span data-ttu-id="aaf05-162">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-162">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="aaf05-163"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-163"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="aaf05-164">Нет.</span><span class="sxs-lookup"><span data-stu-id="aaf05-164">None.</span></span><br/>                                           |
| <span id="1"></span><dl> <span data-ttu-id="aaf05-165"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-165"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="aaf05-166">Только серверы, допускающие динамические обновления.</span><span class="sxs-lookup"><span data-stu-id="aaf05-166">Only servers that allow dynamic updates.</span></span><br/>        |
| <span id="2"></span><dl> <span data-ttu-id="aaf05-167"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-167"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="aaf05-168">Только серверы, которые не разрешают динамические обновления.</span><span class="sxs-lookup"><span data-stu-id="aaf05-168">Only servers that do not allow dynamic updates.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="aaf05-169"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-169"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="aaf05-170">Все серверы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-170">All servers.</span></span><br/>                                    |



 

<span data-ttu-id="aaf05-171">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="aaf05-171">The default value is 1.</span></span>

<span data-ttu-id="aaf05-172">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="aaf05-172">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="aaf05-173">Число 3 представляет все серверы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-173">The number 3 represents All servers.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-174">**биндсекондариес**</span><span class="sxs-lookup"><span data-stu-id="aaf05-174">**BindSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-175">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-176">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-176">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-177">Определяет формат сообщения AXFR при отправке на серверы-получатели DNS сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="aaf05-177">Determines the AXFR message format when sending to non-Microsoft DNS Server secondaries.</span></span> <span data-ttu-id="aaf05-178">Если задано значение TRUE, DNS-сервер отправляет передачу данных в несжатом формате из получателей сторонних DNS-серверов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="aaf05-178">When set to TRUE, the DNS Server sends transfers to non-Microsoft DNS Server secondaries in the uncompressed format.</span></span> <span data-ttu-id="aaf05-179">Если значение равно "FALSE", все передачи отправляются в быстром формате.</span><span class="sxs-lookup"><span data-stu-id="aaf05-179">When FALSE, all transfers are sent in the fast format.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-180">**бутмесод**</span><span class="sxs-lookup"><span data-stu-id="aaf05-180">**BootMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-181">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-182">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-183">Метод инициализации для DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="aaf05-183">Initialization method for the DNS Server.</span></span> <span data-ttu-id="aaf05-184">В следующей таблице представлены допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="aaf05-184">Valid values are shown in the following table.</span></span>



| <span data-ttu-id="aaf05-185">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-185">Value</span></span>                                                                                                | <span data-ttu-id="aaf05-186">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-186">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="aaf05-187"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-187"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="aaf05-188">Неинициализированный.</span><span class="sxs-lookup"><span data-stu-id="aaf05-188">Uninitialized.</span></span><br/>                    |
| <span id="1"></span><dl> <span data-ttu-id="aaf05-189"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-189"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="aaf05-190">Загрузка из файла.</span><span class="sxs-lookup"><span data-stu-id="aaf05-190">Boot from file.</span></span><br/>                   |
| <span id="2"></span><dl> <span data-ttu-id="aaf05-191"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-191"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="aaf05-192">Загрузка из реестра.</span><span class="sxs-lookup"><span data-stu-id="aaf05-192">Boot from registry.</span></span><br/>               |
| <span id="3"></span><dl> <span data-ttu-id="aaf05-193"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-193"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="aaf05-194">Загрузка из каталога и реестра.</span><span class="sxs-lookup"><span data-stu-id="aaf05-194">Boot from directory and registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aaf05-195">**дефаултагингстате**</span><span class="sxs-lookup"><span data-stu-id="aaf05-195">**DefaultAgingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-196">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-197">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-198">Значение **скавенгингинтервал** по умолчанию, заданное для всех зон, интегрированных с Active Directory, созданных на этом DNS-сервере.</span><span class="sxs-lookup"><span data-stu-id="aaf05-198">Default **ScavengingInterval** value set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="aaf05-199">Значение по умолчанию равно нулю, что означает, что очистка отключена.</span><span class="sxs-lookup"><span data-stu-id="aaf05-199">The default value is zero, indicating scavenging is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-200">**дефаултнорефрешинтервал**</span><span class="sxs-lookup"><span data-stu-id="aaf05-200">**DefaultNoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-201">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-202">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-203">Интервал без обновления в часах, заданный для всех зон, интегрированных с Active Directory, созданных на этом DNS-сервере.</span><span class="sxs-lookup"><span data-stu-id="aaf05-203">No-refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="aaf05-204">Значение по умолчанию — 168 часов (семь дней).</span><span class="sxs-lookup"><span data-stu-id="aaf05-204">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-205">**DefaultRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="aaf05-205">**DefaultRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-206">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-207">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-207">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-208">Интервал обновления в часах, заданный для всех Active Directoryных зон, созданных на этом DNS-сервере.</span><span class="sxs-lookup"><span data-stu-id="aaf05-208">Refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="aaf05-209">Значение по умолчанию — 168 часов (семь дней).</span><span class="sxs-lookup"><span data-stu-id="aaf05-209">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-210">**дисаблеаутореверсезонес**</span><span class="sxs-lookup"><span data-stu-id="aaf05-210">**DisableAutoReverseZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-211">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-212">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-213">Указывает, будет ли DNS-сервер автоматически создавать стандартные зоны обратных просмотров.</span><span class="sxs-lookup"><span data-stu-id="aaf05-213">Indicates whether the DNS Server automatically creates standard reverse look up zones.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-214">**дисжоинтнетс**</span><span class="sxs-lookup"><span data-stu-id="aaf05-214">**DisjointNets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-215">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-216">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-217">Указывает, можно ли переопределить привязку портов по умолчанию для сокета, используемого для отправки запросов на удаленные DNS-серверы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-217">Indicates whether the default port binding for a socket used to send queries to remote DNS Servers can be overridden.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-218">**дсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="aaf05-218">**DsAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-219">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-221">Указывает, имеется ли доступная DS на DNS-сервере.</span><span class="sxs-lookup"><span data-stu-id="aaf05-221">Indicates whether there is an available DS on the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-222">**дсполлингинтервал**</span><span class="sxs-lookup"><span data-stu-id="aaf05-222">**DsPollingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-223">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-224">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-224">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-225">Интервал в секундах для опроса зон, интегрированных с DS.</span><span class="sxs-lookup"><span data-stu-id="aaf05-225">Interval, in seconds, to poll the DS-integrated zones.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-226">**дстомбстонеинтервал**</span><span class="sxs-lookup"><span data-stu-id="aaf05-226">**DsTombstoneInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-227">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-228">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-229">Время существования захороненных записей в интегрированных зонах службы каталогов, выраженное в секундах.</span><span class="sxs-lookup"><span data-stu-id="aaf05-229">Lifetime of tombstoned records in Directory Service integrated zones, expressed in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-230">**еднскачетимеаут**</span><span class="sxs-lookup"><span data-stu-id="aaf05-230">**EDnsCacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-231">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-231">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-233">Время существования в секундах кэшированной информации, описывающей версию EDNS, поддерживаемую другими DNS-серверами.</span><span class="sxs-lookup"><span data-stu-id="aaf05-233">Lifetime, in seconds, of the cached information describing the EDNS version supported by other DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-234">**енабледиректорипартитионс**</span><span class="sxs-lookup"><span data-stu-id="aaf05-234">**EnableDirectoryPartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-235">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-236">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-237">Указывает, включена ли поддержка разделов каталога приложений на DNS-сервере.</span><span class="sxs-lookup"><span data-stu-id="aaf05-237">Specifies whether support for application directory partitions is enabled on the DNS Server.</span></span>

<span data-ttu-id="aaf05-238">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="aaf05-238">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="aaf05-239">Этот метод называется Енабледиректорипартитионсуппорт.</span><span class="sxs-lookup"><span data-stu-id="aaf05-239">This method is named EnableDirectoryPartitionSupport.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-240">**енабледнссек**</span><span class="sxs-lookup"><span data-stu-id="aaf05-240">**EnableDnsSec**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-241">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-242">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-243">Указывает, содержит ли DNS-сервер записи ресурсов DNSSEC, KEY, SIG и NXT в ответе, в соответствии со следующей таблицей:</span><span class="sxs-lookup"><span data-stu-id="aaf05-243">Specifies whether the DNS Server includes DNSSEC-specific RRs, KEY, SIG, and NXT in a response, per the following table:</span></span>



| <span data-ttu-id="aaf05-244">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-244">Value</span></span>                                                                                                | <span data-ttu-id="aaf05-245">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-245">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="aaf05-246"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-246"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="aaf05-247">Записи DNSSEC не включаются в ответ, если запрос не запрашивал набор записей ресурсов типа DNSSEC.</span><span class="sxs-lookup"><span data-stu-id="aaf05-247">No DNSSEC records are included in the response unless the query requested a resource record set of the DNSSEC record type.</span></span><br/>          |
| <span id="1"></span><dl> <span data-ttu-id="aaf05-248"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-248"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="aaf05-249">Записи DNSSEC включаются в ответ в соответствии с RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="aaf05-249">DNSSEC records are included in the response according to RFC 2535.</span></span><br/>                                                                  |
| <span id="2"></span><dl> <span data-ttu-id="aaf05-250"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-250"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="aaf05-251">Записи DNSSEC включаются в ответ, только если исходный запрос клиента содержал запись ресурса OPT согласно RFC 2671.</span><span class="sxs-lookup"><span data-stu-id="aaf05-251">DNSSEC records are included in a response only if the original client query contained the OPT resource record according to RFC 2671</span></span><br/> |



 

<span data-ttu-id="aaf05-252">Если запрос запрашивает набор записей ресурсов типа DNSSEC, DNS-сервер всегда отвечает на такие записи, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="aaf05-252">If a query requests a resource record set of the DNSSEC type, the DNS Server always responds with such records, if available.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-253">**енаблиднспробес**</span><span class="sxs-lookup"><span data-stu-id="aaf05-253">**EnableEDnsProbes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-254">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-254">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-255">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-255">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-256">Указывает поведение DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="aaf05-256">Specifies the behavior of the DNS Server.</span></span> <span data-ttu-id="aaf05-257">Если значение равно TRUE, DNS-сервер всегда отвечает на записи ресурсов OPT в соответствии с RFC 2671, если только удаленный сервер не указал, что он не поддерживает EDNS в предыдущей среде Exchange.</span><span class="sxs-lookup"><span data-stu-id="aaf05-257">When TRUE, the DNS Server always responds with OPT resource records according to RFC 2671, unless the remote server has indicated it does not support EDNS in a prior exchange.</span></span> <span data-ttu-id="aaf05-258">Если задано значение FALSE, то DNS-сервер отвечает на запросы с параметром только в том случае, если в исходном запросе отправляются разрешения.</span><span class="sxs-lookup"><span data-stu-id="aaf05-258">If FALSE, the DNS Server responds to queries with OPTs only if OPTs are sent in the original query.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-259">**EventLogLevel**</span><span class="sxs-lookup"><span data-stu-id="aaf05-259">**EventLogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-260">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-260">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-261">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-261">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-262">Указывает, какие события DNS-сервер регистрирует в Просмотр событий системном журнале.</span><span class="sxs-lookup"><span data-stu-id="aaf05-262">Indicates which events the DNS Server records in the Event Viewer system log.</span></span> <span data-ttu-id="aaf05-263">Используются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="aaf05-263">The following values are used.</span></span>



| <span data-ttu-id="aaf05-264">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-264">Value</span></span>                                                                                                | <span data-ttu-id="aaf05-265">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-265">Meaning</span></span>                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="aaf05-266"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-266"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="aaf05-267">Нет.</span><span class="sxs-lookup"><span data-stu-id="aaf05-267">None.</span></span><br/>                         |
| <span id="1"></span><dl> <span data-ttu-id="aaf05-268"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-268"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="aaf05-269">Регистрировать только ошибки.</span><span class="sxs-lookup"><span data-stu-id="aaf05-269">Log only errors.</span></span><br/>              |
| <span id="2"></span><dl> <span data-ttu-id="aaf05-270"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-270"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="aaf05-271">Регистрировать только предупреждения и ошибки.</span><span class="sxs-lookup"><span data-stu-id="aaf05-271">Log only warnings and errors.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="aaf05-272"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-272"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="aaf05-273">Регистрация всех событий.</span><span class="sxs-lookup"><span data-stu-id="aaf05-273">Log all events.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="aaf05-274">**форвардделегатионс**</span><span class="sxs-lookup"><span data-stu-id="aaf05-274">**ForwardDelegations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-275">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-276">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-276">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-277">Указывает, перенаправляются ли запросы к делегированным вложенным зонам.</span><span class="sxs-lookup"><span data-stu-id="aaf05-277">Specifies whether queries to delegated sub-zones are forwarded.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-278">**Серверы пересылки**</span><span class="sxs-lookup"><span data-stu-id="aaf05-278">**Forwarders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-279">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="aaf05-279">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-280">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-280">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-281">Перечисляет список IP-адресов серверов пересылки, на которые DNS-сервер перенаправляет запросы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-281">Enumerates the list of IP addresses of Forwarders to which the DNS Server forwards queries.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-282">**форвардингтимеаут**</span><span class="sxs-lookup"><span data-stu-id="aaf05-282">**ForwardingTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-283">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-284">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-284">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-285">Время (в секундах), в течение которого DNS-сервер пересылает запрос, ждет разрешения от сервера [*пересылки*](f-gly.md) , прежде чем пытаться разрешить сам запрос.</span><span class="sxs-lookup"><span data-stu-id="aaf05-285">Time, in seconds, a DNS Server forwarding a query will wait for resolution from the [*forwarder*](f-gly.md) before attempting to resolve the query itself.</span></span>

<span data-ttu-id="aaf05-286">Это значение не имеет смысла, если сервер пересылки не настроен на использование рекурсии.</span><span class="sxs-lookup"><span data-stu-id="aaf05-286">This value is meaningless if the forwarding server is not set to use recursion.</span></span> <span data-ttu-id="aaf05-287">Чтобы определить это, проверьте логическое свойство Slave.</span><span class="sxs-lookup"><span data-stu-id="aaf05-287">To determine this, check the IsSlave Boolean property.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-288">**Slave**</span><span class="sxs-lookup"><span data-stu-id="aaf05-288">**IsSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-289">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-290">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-291">**Значение true** , если DNS-сервер не использует рекурсию при сбое разрешения имен через серверы пересылки.</span><span class="sxs-lookup"><span data-stu-id="aaf05-291">**TRUE** if the DNS server does not use recursion when name-resolution through forwarders fails.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-292">**листенаддрессес**</span><span class="sxs-lookup"><span data-stu-id="aaf05-292">**ListenAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-293">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="aaf05-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-294">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-294">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-295">Перечисляет список IP-адресов, на которые DNS-сервер может принимать запросы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-295">Enumerates the list of IP addresses on which the DNS Server can receive queries.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-296">**локалнетприорити**</span><span class="sxs-lookup"><span data-stu-id="aaf05-296">**LocalNetPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-297">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-298">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-298">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-299">Указывает, назначает ли DNS-сервер приоритет локальному сетевому адресу при возврате записей.</span><span class="sxs-lookup"><span data-stu-id="aaf05-299">Indicates whether the DNS Server gives priority to the local net address when returning A records.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-300">**логфилемакссизе**</span><span class="sxs-lookup"><span data-stu-id="aaf05-300">**LogFileMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-301">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-302">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-302">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-303">Размер журнала отладки DNS-сервера в байтах.</span><span class="sxs-lookup"><span data-stu-id="aaf05-303">Size of the DNS Server debug log, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-304">**LogFilePath**</span><span class="sxs-lookup"><span data-stu-id="aaf05-304">**LogFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-305">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aaf05-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-306">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-306">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-307">Имя файла и путь к журналу отладки DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="aaf05-307">File name and path for the DNS Server debug log.</span></span> <span data-ttu-id="aaf05-308">Значение по умолчанию —% system32% DNS \\ \\ DNS. log.</span><span class="sxs-lookup"><span data-stu-id="aaf05-308">Default is %system32%\\dns\\dns.log.</span></span> <span data-ttu-id="aaf05-309">Относительные пути задаются относительно% systemroot% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="aaf05-309">Relative paths are relative to %Systemroot%\\System32.</span></span> <span data-ttu-id="aaf05-310">Можно использовать абсолютные пути, но пути UNC не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="aaf05-310">Absolute paths may be used, but UNC paths are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-311">**логипфилтерлист**</span><span class="sxs-lookup"><span data-stu-id="aaf05-311">**LogIPFilterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-312">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="aaf05-312">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-313">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-313">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-314">Список IP-адресов, используемых для фильтрации событий DNS, записываемых в журнал отладки.</span><span class="sxs-lookup"><span data-stu-id="aaf05-314">List of IP addresses used to filter DNS events written to the debug log.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-315">**LogLevel**</span><span class="sxs-lookup"><span data-stu-id="aaf05-315">**LogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-316">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-317">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-317">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-318">Указывает, какие политики активируются в системном журнале Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="aaf05-318">Indicates which policies are activated in the Event Viewer system log.</span></span>

<span data-ttu-id="aaf05-319">Необходимо задать определенные значения на основе следующего алгоритма: каждой политике (для активации в системном журнале Просмотр событий) присваивается определенное значение.</span><span class="sxs-lookup"><span data-stu-id="aaf05-319">Should be set to specific values based on the following algorithm: Every policy (to be activated in the Event Viewer system log) is assigned a specific value.</span></span>



| <span data-ttu-id="aaf05-320">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-320">Value</span></span>                                                                                                                  | <span data-ttu-id="aaf05-321">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-321">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="aaf05-322"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-322"><dt>**1**</dt></span></span> </dl>                   | <span data-ttu-id="aaf05-323">Выбор.</span><span class="sxs-lookup"><span data-stu-id="aaf05-323">Query.</span></span><br/>                                   |
| <span id="16"></span><dl> <span data-ttu-id="aaf05-324"><dt>**глубин**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-324"><dt>**16**</dt></span></span> </dl>                 | <span data-ttu-id="aaf05-325">Явлении.</span><span class="sxs-lookup"><span data-stu-id="aaf05-325">Notify.</span></span><br/>                                  |
| <span id="32"></span><dl> <span data-ttu-id="aaf05-326"><dt>**32**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-326"><dt>**32**</dt></span></span> </dl>                 | <span data-ttu-id="aaf05-327">Обновление.</span><span class="sxs-lookup"><span data-stu-id="aaf05-327">Update.</span></span><br/>                                  |
| <span id="254"></span><dl> <span data-ttu-id="aaf05-328"><dt>**254**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-328"><dt>**254**</dt></span></span> </dl>               | <span data-ttu-id="aaf05-329">Транзакции, не являющиеся запросами.</span><span class="sxs-lookup"><span data-stu-id="aaf05-329">Nonquery transactions.</span></span><br/>                   |
| <span id="256"></span><dl> <span data-ttu-id="aaf05-330"><dt>**256**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-330"><dt>**256**</dt></span></span> </dl>               | <span data-ttu-id="aaf05-331">Вопросы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-331">Questions.</span></span><br/>                               |
| <span id="512"></span><dl> <span data-ttu-id="aaf05-332"><dt>**512**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-332"><dt>**512**</dt></span></span> </dl>               | <span data-ttu-id="aaf05-333">Вас.</span><span class="sxs-lookup"><span data-stu-id="aaf05-333">Answers.</span></span><br/>                                 |
| <span id="4096"></span><dl> <span data-ttu-id="aaf05-334"><dt>**4096**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-334"><dt>**4096**</dt></span></span> </dl>             | <span data-ttu-id="aaf05-335">Отправить.</span><span class="sxs-lookup"><span data-stu-id="aaf05-335">Send.</span></span><br/>                                    |
| <span id="8192"></span><dl> <span data-ttu-id="aaf05-336"><dt>**8192**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-336"><dt>**8192**</dt></span></span> </dl>             | <span data-ttu-id="aaf05-337">Получать.</span><span class="sxs-lookup"><span data-stu-id="aaf05-337">Receive.</span></span><br/>                                 |
| <span id="16384"></span><dl> <span data-ttu-id="aaf05-338"><dt>**16384**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-338"><dt>**16384**</dt></span></span> </dl>           | <span data-ttu-id="aaf05-339">Протокола.</span><span class="sxs-lookup"><span data-stu-id="aaf05-339">UDP.</span></span><br/>                                     |
| <span id="32768"></span><dl> <span data-ttu-id="aaf05-340"><dt>**32768**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-340"><dt>**32768**</dt></span></span> </dl>           | <span data-ttu-id="aaf05-341">Протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="aaf05-341">TCP.</span></span><br/>                                     |
| <span id="65535"></span><dl> <span data-ttu-id="aaf05-342"><dt>**65535**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-342"><dt>**65535**</dt></span></span> </dl>           | <span data-ttu-id="aaf05-343">Все пакеты.</span><span class="sxs-lookup"><span data-stu-id="aaf05-343">All packets.</span></span><br/>                             |
| <span id="65536"></span><dl> <span data-ttu-id="aaf05-344"><dt>**65536**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-344"><dt>**65536**</dt></span></span> </dl>           | <span data-ttu-id="aaf05-345">Транзакция записи в службу каталогов NT.</span><span class="sxs-lookup"><span data-stu-id="aaf05-345">NT Directory Service write transaction.</span></span><br/>  |
| <span id="131072"></span><dl> <span data-ttu-id="aaf05-346"><dt>**131072**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-346"><dt>**131072**</dt></span></span> </dl>         | <span data-ttu-id="aaf05-347">Транзакция обновления службы каталогов NT.</span><span class="sxs-lookup"><span data-stu-id="aaf05-347">NT Directory Service update transaction.</span></span><br/> |
| <span id="16777216"></span><dl> <span data-ttu-id="aaf05-348"><dt>**16777216**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-348"><dt>**16777216**</dt></span></span> </dl>     | <span data-ttu-id="aaf05-349">Полные пакеты.</span><span class="sxs-lookup"><span data-stu-id="aaf05-349">Full packets.</span></span><br/>                            |
| <span id="2147483648"></span><dl> <span data-ttu-id="aaf05-350"><dt>**2147483648**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-350"><dt>**2147483648**</dt></span></span> </dl> | <span data-ttu-id="aaf05-351">Запись с помощью.</span><span class="sxs-lookup"><span data-stu-id="aaf05-351">Write through.</span></span><br/>                           |



 

<span data-ttu-id="aaf05-352">В этом свойстве указывается сумма значений, соответствующих всем активируемым политикам.</span><span class="sxs-lookup"><span data-stu-id="aaf05-352">The sum of the values corresponding to all the policies to be activated is indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-353">**лусевилдкардинг**</span><span class="sxs-lookup"><span data-stu-id="aaf05-353">**LooseWildcarding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-354">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-355">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-355">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-356">Указывает, выполняет ли DNS-сервер нестрогие подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="aaf05-356">Indicates whether the DNS Server performs loose wildcarding.</span></span> <span data-ttu-id="aaf05-357">Если значение не определено или равно нулю, сервер соответствует поведению подстановочных знаков, указанному в DNS RFC.</span><span class="sxs-lookup"><span data-stu-id="aaf05-357">If undefined or zero, the server follows the wildcarding behavior specified in the DNS RFC.</span></span> <span data-ttu-id="aaf05-358">В этом случае администратору рекомендуется включить MX-записи для всех узлов, не способных получать почту.</span><span class="sxs-lookup"><span data-stu-id="aaf05-358">In this case, an administrator is advised to include MX records for all hosts incapable of receiving mail.</span></span> <span data-ttu-id="aaf05-359">Если значение не равно нулю, сервер ищет ближайший узел с подстановочными знаками; в этом случае администратор должен разместить MX-записи в корне зоны и в узле с подстановочными знаками (" \* ") непосредственно под корнем зоны.</span><span class="sxs-lookup"><span data-stu-id="aaf05-359">If nonzero, the server seeks the closest wildcard node; in this case, an administrator should put MX records at the zone root and in a wildcard node ('\*') directly below the zone root.</span></span> <span data-ttu-id="aaf05-360">Кроме того, администраторы должны размещать ссылки на собственные записи MX на узлах, получающих собственную почту.</span><span class="sxs-lookup"><span data-stu-id="aaf05-360">Also, administrators should put self-referencing MX records on hosts that receive their own mail.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-361">**макскачеттл**</span><span class="sxs-lookup"><span data-stu-id="aaf05-361">**MaxCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-362">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-363">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-363">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-364">Максимальное время (в секундах), в течение которого запись рекурсивного имени запроса может остаться в кэше DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="aaf05-364">Maximum time, in seconds, the record of a recursive name query may remain in the DNS Server cache.</span></span> <span data-ttu-id="aaf05-365">DNS-сервер удаляет записи из кэша по истечении значения этой записи, даже если значение поля TTL в записи больше.</span><span class="sxs-lookup"><span data-stu-id="aaf05-365">The DNS Server deletes records from the cache when the value of this entry expires, even if the value of the TTL field in the record is greater.</span></span>

<span data-ttu-id="aaf05-366">Значение этого свойства по умолчанию — 86 400 секунд (1 день).</span><span class="sxs-lookup"><span data-stu-id="aaf05-366">The default value of this property is 86,400 seconds (1 day).</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-367">**макснегативекачеттл**</span><span class="sxs-lookup"><span data-stu-id="aaf05-367">**MaxNegativeCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-368">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-369">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-369">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-370">Максимальное время в секундах, в течение которого Ошибка имени в результате рекурсивного запроса может остаться в кэше DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="aaf05-370">Maximum time, in seconds, a name error result from a recursive query may remain in the DNS Server cache.</span></span> <span data-ttu-id="aaf05-371">DNS удаляет записи из кэша по истечении этого времени, даже если поле TTL больше.</span><span class="sxs-lookup"><span data-stu-id="aaf05-371">DNS deletes records from the cache when this timer expires, even if the TTL field is greater.</span></span> <span data-ttu-id="aaf05-372">Значение по умолчанию — 86 400 (один день).</span><span class="sxs-lookup"><span data-stu-id="aaf05-372">Default value is 86,400 (one day).</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="aaf05-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aaf05-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aaf05-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-376">Полное доменное имя (FQDN) или IP-адрес DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="aaf05-376">Fully qualified domain name (FQDN) or IP address of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-377">**намечеккфлаг**</span><span class="sxs-lookup"><span data-stu-id="aaf05-377">**NameCheckFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-378">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-379">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-379">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-380">Указывает набор подходящих символов, которые будут использоваться в DNS-именах.</span><span class="sxs-lookup"><span data-stu-id="aaf05-380">Indicates the set of eligible characters to be used in DNS names.</span></span> <span data-ttu-id="aaf05-381">Используются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="aaf05-381">The following values are used.</span></span>



| <span data-ttu-id="aaf05-382">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-382">Value</span></span>                                                                                                | <span data-ttu-id="aaf05-383">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-383">Meaning</span></span>                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="aaf05-384"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-384"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="aaf05-385">Кодировка RFC (ANSI)</span><span class="sxs-lookup"><span data-stu-id="aaf05-385">Strict RFC (ANSI)</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="aaf05-386"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-386"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="aaf05-387">Не RFC (ANSI)</span><span class="sxs-lookup"><span data-stu-id="aaf05-387">Non RFC (ANSI)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="aaf05-388"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-388"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="aaf05-389">Многобайтовая кодировка (UTF8)</span><span class="sxs-lookup"><span data-stu-id="aaf05-389">Multibyte (UTF8)</span></span><br/>  |



 

<span data-ttu-id="aaf05-390">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="aaf05-390">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="aaf05-391">Значение «2» означает «Any».</span><span class="sxs-lookup"><span data-stu-id="aaf05-391">A value of "2" indicates "Any."</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-392">**норекурсион**</span><span class="sxs-lookup"><span data-stu-id="aaf05-392">**NoRecursion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-393">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-393">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-394">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-394">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-395">Указывает, выполняет ли DNS-сервер рекурсивный поиск.</span><span class="sxs-lookup"><span data-stu-id="aaf05-395">Indicates whether the DNS Server performs recursive look ups.</span></span> <span data-ttu-id="aaf05-396">Значение TRUE указывает, что рекурсивный поиск не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aaf05-396">TRUE indicates recursive look ups are not performed.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-397">**рекурсионретри**</span><span class="sxs-lookup"><span data-stu-id="aaf05-397">**RecursionRetry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-398">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-399">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-399">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-400">Прошло секунд перед повторным выполнением рекурсивного поиска.</span><span class="sxs-lookup"><span data-stu-id="aaf05-400">Elapsed seconds before retrying a recursive look up.</span></span> <span data-ttu-id="aaf05-401">Если свойство не определено или равно нулю, повторные попытки выполняются через три секунды.</span><span class="sxs-lookup"><span data-stu-id="aaf05-401">If the property is undefined or zero, retries are made after three seconds.</span></span> <span data-ttu-id="aaf05-402">Пользователям не рекомендуется изменять это свойство.</span><span class="sxs-lookup"><span data-stu-id="aaf05-402">Users are discouraged from altering this property.</span></span> <span data-ttu-id="aaf05-403">Существуют определенные ситуации, когда необходимо изменить свойство. одним из примеров является то, что DNS-сервер обращается к удаленным серверам через медленное подключение, и DNS-сервер повторяет попытку получения ответа от удаленного DNS.</span><span class="sxs-lookup"><span data-stu-id="aaf05-403">There are certain situations when the property should be changed; one example is when the DNS Server contacts remote servers over a slow link, and the DNS Server is retrying before receiving response from the remote DNS.</span></span> <span data-ttu-id="aaf05-404">В этом случае повышение времени ожидания будет немного дольше, чем наблюдаемое время отклика с удаленного DNS.</span><span class="sxs-lookup"><span data-stu-id="aaf05-404">In this case, raising the time out to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-405">**рекурсионтимеаут**</span><span class="sxs-lookup"><span data-stu-id="aaf05-405">**RecursionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-406">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-406">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-407">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-407">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-408">Прошло секунд до того, как DNS-сервер предоставит рекурсивный запрос.</span><span class="sxs-lookup"><span data-stu-id="aaf05-408">Elapsed seconds before the DNS Server gives up recursive query.</span></span> <span data-ttu-id="aaf05-409">Если свойство не определено или равно нулю, DNS-сервер додается через 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="aaf05-409">If the property is undefined or zero, the DNS Server gives up after 15 seconds.</span></span> <span data-ttu-id="aaf05-410">Как правило, время ожидания в 15 секунд достаточно для того, чтобы любой необработанный ответ можно было вернуть на DNS-сервер.</span><span class="sxs-lookup"><span data-stu-id="aaf05-410">In general, the 15-second time out is sufficient to allow any outstanding response to get back to the DNS Server.</span></span>

<span data-ttu-id="aaf05-411">Пользователям не рекомендуется изменять это свойство.</span><span class="sxs-lookup"><span data-stu-id="aaf05-411">Users are discouraged from altering this property.</span></span> <span data-ttu-id="aaf05-412">Один из сценариев, в котором необходимо изменить свойство, — когда DNS-сервер обращается к удаленным серверам по медленному каналу, а DNS-сервер отклоняет запросы (с \_ ошибкой сервера) перед получением ответов.</span><span class="sxs-lookup"><span data-stu-id="aaf05-412">One scenario where the property should be changed is when the DNS Server contacts remote servers over a slow link, and the DNS Server is observed rejecting queries (with SERVER\_FAILURE) before responses are received.</span></span>

<span data-ttu-id="aaf05-413">Кроме того, при повторном выполнении запросов клиентские разрешения также требуют тщательного изучения, чтобы определить, связаны ли удаленные ответы с запросом, для которого истекло время ожидания. В этом случае увеличение значения времени ожидания будет немного дольше, чем наблюдаемое время отклика с удаленного DNS.</span><span class="sxs-lookup"><span data-stu-id="aaf05-413">Client resolvers also retry queries, so careful investigation is required to determine whether remote responses are actually associated with the query that timed out. In this case, raising the time out value to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-414">**Циклический перебор**</span><span class="sxs-lookup"><span data-stu-id="aaf05-414">**RoundRobin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-415">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-416">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-416">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-417">Указывает, является ли DNS-сервер циклическим Робинс несколько записей A.</span><span class="sxs-lookup"><span data-stu-id="aaf05-417">Indicates whether the DNS Server round robins multiple A records.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-418">**Установлена**</span><span class="sxs-lookup"><span data-stu-id="aaf05-418">**RpcProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-419">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-419">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-420">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-420">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-421">Протокол RPC или протоколы, по которым выполняется администрирование RPC.</span><span class="sxs-lookup"><span data-stu-id="aaf05-421">RPC protocol or protocols over which administrative RPC runs.</span></span> <span data-ttu-id="aaf05-422">Для назначения определенного значения используется следующий алгоритм:</span><span class="sxs-lookup"><span data-stu-id="aaf05-422">The following algorithm is used to assign a specific value:</span></span>



| <span data-ttu-id="aaf05-423">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-423">Value</span></span>                                                                                                | <span data-ttu-id="aaf05-424">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-424">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="aaf05-425"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-425"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="aaf05-426">Нет</span><span class="sxs-lookup"><span data-stu-id="aaf05-426">None</span></span><br/>        |
| <span id="1"></span><dl> <span data-ttu-id="aaf05-427"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-427"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="aaf05-428">TCP</span><span class="sxs-lookup"><span data-stu-id="aaf05-428">TCP</span></span><br/>         |
| <span id="2"></span><dl> <span data-ttu-id="aaf05-429"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-429"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="aaf05-430">Именованные каналы</span><span class="sxs-lookup"><span data-stu-id="aaf05-430">Named Pipes</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="aaf05-431"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-431"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="aaf05-432">ВЫЗОВА</span><span class="sxs-lookup"><span data-stu-id="aaf05-432">LPC</span></span><br/>         |



 

<span data-ttu-id="aaf05-433">Сумма значений указывает используемые протоколы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-433">The sum of the values indicates the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-434">**скавенгингинтервал**</span><span class="sxs-lookup"><span data-stu-id="aaf05-434">**ScavengingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-435">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-435">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-436">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-436">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-437">Интервал (в часах) между двумя последовательными операциями очистки, выполняемыми DNS-сервером.</span><span class="sxs-lookup"><span data-stu-id="aaf05-437">Interval, in hours, between two consecutive scavenging operations performed by the DNS Server.</span></span> <span data-ttu-id="aaf05-438">Ноль означает, что очистка отключена.</span><span class="sxs-lookup"><span data-stu-id="aaf05-438">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="aaf05-439">Значение по умолчанию — 168 часов (семь дней).</span><span class="sxs-lookup"><span data-stu-id="aaf05-439">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-440">**секуререспонсес**</span><span class="sxs-lookup"><span data-stu-id="aaf05-440">**SecureResponses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-441">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-441">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-442">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-442">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-443">Указывает, сохраняет ли DNS-сервер монопольные записи имен в одном поддереве с сервером, на котором они были предоставлены.</span><span class="sxs-lookup"><span data-stu-id="aaf05-443">Indicates whether the DNS Server exclusively saves records of names in the same subtree as the server that provided them.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-444">**сендпорт**</span><span class="sxs-lookup"><span data-stu-id="aaf05-444">**SendPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-445">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-446">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-446">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-447">Порт, на котором DNS-сервер отправляет запросы UDP на другие серверы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-447">Port on which the DNS Server sends UDP queries to other servers.</span></span> <span data-ttu-id="aaf05-448">По умолчанию DNS-сервер отправляет запросы к сокету, привязанному к DNS-порту.</span><span class="sxs-lookup"><span data-stu-id="aaf05-448">By default, the DNS Server sends queries on a socket bound to the DNS port.</span></span>

<span data-ttu-id="aaf05-449">В некоторых ситуациях это не лучшая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="aaf05-449">Under certain situations, this is not the best configuration.</span></span> <span data-ttu-id="aaf05-450">Один из очевидных случаев заключается в том, что администратор блокирует порт DNS с брандмауэром, чтобы предотвратить доступ к DNS-серверу извне, но по-прежнему хочет, чтобы сервер мог связаться с DNS-серверами в Интернете, чтобы обеспечить разрешение имен для внутренних клиентов.</span><span class="sxs-lookup"><span data-stu-id="aaf05-450">One obvious case is when an administrator blocks the DNS port with a firewall to prevent outside access to the DNS Server, but still wants the server to be able to contact Internet DNS Servers to provide name resolution for internal clients.</span></span> <span data-ttu-id="aaf05-451">Другой случай — когда DNS-сервер поддерживает несвязанные раскрытия (свойство **дисжоинтнетс** , установленное в значение true, определяет этот сценарий).</span><span class="sxs-lookup"><span data-stu-id="aaf05-451">Another case is when the DNS Server is supporting disjoint nets (the property **DisjointNets** set to TRUE identifies this scenario).</span></span> <span data-ttu-id="aaf05-452">В этих случаях при присвоении свойству **сендоннонднспорт** ненулевого значения сервер DNS привязывается к произвольному порту для отправки на удаленные DNS-серверы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-452">In these cases, setting the **SendOnNonDnsPort** property to a nonzero value directs the DNS Server to bind to an arbitrary port for sending to remote DNS Servers.</span></span>

<span data-ttu-id="aaf05-453">Если значение **сендоннонднспорт** больше 1024, DNS-сервер явно привязывается к заданному значению порта.</span><span class="sxs-lookup"><span data-stu-id="aaf05-453">If the **SendOnNonDnsPort** value is greater than 1024, the DNS Server binds explicitly to the port value given.</span></span> <span data-ttu-id="aaf05-454">Этот параметр конфигурации полезен, если администратору необходимо исправить порт запроса DNS для целей брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="aaf05-454">This configuration option is useful when an administrator needs to fix the DNS query port for firewall purposes.</span></span>

<span data-ttu-id="aaf05-455">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="aaf05-455">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="aaf05-456">Установка ненулевого значения для свойства Сендпорт приводит к тому, что DNS-сервер привязывается к произвольному порту для отправки на удаленные DNS-серверы.</span><span class="sxs-lookup"><span data-stu-id="aaf05-456">Setting the SendPort property to a non-zero value causes the DNS server to bind to an arbitrary port for sending to remote DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-457">**сервераддрессес**</span><span class="sxs-lookup"><span data-stu-id="aaf05-457">**ServerAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-458">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="aaf05-458">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-459">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aaf05-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-460">Перечисляет список IP-адресов для DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="aaf05-460">Enumerates the list of IP addresses for the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-461">**стриктфилепарсинг**</span><span class="sxs-lookup"><span data-stu-id="aaf05-461">**StrictFileParsing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-462">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-462">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-463">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-463">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-464">Указывает, будет ли DNS-сервер анализировать [*файлы зоны*](z-gly.md) строго.</span><span class="sxs-lookup"><span data-stu-id="aaf05-464">Indicates whether the DNS Server parses [*zone files*](z-gly.md) strictly.</span></span> <span data-ttu-id="aaf05-465">Если значение не определено или равно нулю, сервер будет записывать и игнорировать неверные данные в файле зоны и продолжать загрузку.</span><span class="sxs-lookup"><span data-stu-id="aaf05-465">If undefined or zero, the server will log and ignore bad data in the zone file and continue to load.</span></span> <span data-ttu-id="aaf05-466">Если значение не равно нулю, сервер регистрирует ошибки в файле зоны и завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="aaf05-466">If nonzero, the server will log and fail on zone file errors.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-467">**UpdateOptions**</span><span class="sxs-lookup"><span data-stu-id="aaf05-467">**UpdateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-468">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aaf05-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-470">Позволяет ограничивать тип записей, которые могут динамически обновляться на сервере, в дополнение к параметрам **алловупдате** объектов Server и Zone.</span><span class="sxs-lookup"><span data-stu-id="aaf05-470">Restricts the type of records that can be dynamically updated on the server, used in addition to the **AllowUpdate** settings on Server and Zone objects.</span></span>

<span data-ttu-id="aaf05-471">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="aaf05-471">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="aaf05-472">0 — нет ограничений.</span><span class="sxs-lookup"><span data-stu-id="aaf05-472">0: No restrictions.</span></span>

<span data-ttu-id="aaf05-473">1: не разрешать динамическое обновление записей SOA.</span><span class="sxs-lookup"><span data-stu-id="aaf05-473">1: Do not allow dynamic updates of SOA records.</span></span>

<span data-ttu-id="aaf05-474">2: не разрешать динамическое обновление записей NS в корне зоны.</span><span class="sxs-lookup"><span data-stu-id="aaf05-474">2: Do not allow dynamic updates of NS records at the zone root.</span></span>

<span data-ttu-id="aaf05-475">4: не разрешать динамическое обновление записей NS, не расположенных в корне зоны (записи делегирования NS).</span><span class="sxs-lookup"><span data-stu-id="aaf05-475">4: Do not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span>

<span data-ttu-id="aaf05-476">Вычислите эти значения, чтобы определить значение параметра.</span><span class="sxs-lookup"><span data-stu-id="aaf05-476">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-477">**Version**</span><span class="sxs-lookup"><span data-stu-id="aaf05-477">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-478">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-479">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aaf05-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-480">Версия DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="aaf05-480">Version of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-481">**вритеаусоритинс**</span><span class="sxs-lookup"><span data-stu-id="aaf05-481">**WriteAuthorityNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-482">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aaf05-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-483">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-483">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-484">Указывает, будет ли DNS-сервер записывать записи NS и SOA в раздел Authority при успешном отклике.</span><span class="sxs-lookup"><span data-stu-id="aaf05-484">Specifies whether the DNS Server writes NS and SOA records to the authority section on successful response.</span></span>

</dd> <dt>

<span data-ttu-id="aaf05-485">**ксфрконнекттимеаут**</span><span class="sxs-lookup"><span data-stu-id="aaf05-485">**XfrConnectTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf05-486">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aaf05-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf05-487">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aaf05-487">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aaf05-488">Время (в секундах), в течение которого DNS-сервер ожидает успешного подключения TCP к удаленному серверу при попытке зонной попытки.</span><span class="sxs-lookup"><span data-stu-id="aaf05-488">Time, in seconds, the DNS Server waits for a successful TCP connection to a remote server when attempting a zone transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aaf05-489">Требования</span><span class="sxs-lookup"><span data-stu-id="aaf05-489">Requirements</span></span>



| <span data-ttu-id="aaf05-490">Требование</span><span class="sxs-lookup"><span data-stu-id="aaf05-490">Requirement</span></span> | <span data-ttu-id="aaf05-491">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf05-491">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf05-492">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aaf05-492">Minimum supported client</span></span><br/> | <span data-ttu-id="aaf05-493">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="aaf05-493">None supported</span></span><br/>                                                              |
| <span data-ttu-id="aaf05-494">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aaf05-494">Minimum supported server</span></span><br/> | <span data-ttu-id="aaf05-495">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aaf05-495">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aaf05-496">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aaf05-496">Namespace</span></span><br/>                | <span data-ttu-id="aaf05-497">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="aaf05-497">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="aaf05-498">MOF</span><span class="sxs-lookup"><span data-stu-id="aaf05-498">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aaf05-499"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aaf05-499"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaf05-500">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aaf05-500">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf05-501">**Метод StartService \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="aaf05-501">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="aaf05-502">**Метод работы \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="aaf05-502">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="aaf05-503">**Метод Стартскавенгинг \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="aaf05-503">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="aaf05-504">**Метод Жетдистингуишеднаме \_ класса микрософтднс Server**</span><span class="sxs-lookup"><span data-stu-id="aaf05-504">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





