---
title: Класс MicrosoftDNS_Zone
description: '\_Класс зоны микрософтднс описывает зону DNS. Каждый экземпляр \_ класса зоны микрософтднс должен быть назначен ровно одному DNS-серверу. Зоны могут быть связаны с несколькими экземплярами \_ классов микрософтднс Domain или микрософтднс \_ ресаурцерекорд.'
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- DNS класса MicrosoftDNS_Zone
- DNS-MicrosoftDNS_Zone класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072122"
---
# <a name="microsoftdns_zone-class"></a><span data-ttu-id="9335b-107">\_Класс зоны микрософтднс</span><span class="sxs-lookup"><span data-stu-id="9335b-107">MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="9335b-108">Эта статья содержит ссылки на термин slave (ведомый). Корпорация Майкрософт больше не использует его.</span><span class="sxs-lookup"><span data-stu-id="9335b-108">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="9335b-109">Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.</span><span class="sxs-lookup"><span data-stu-id="9335b-109">When the term is removed from the software, we’ll remove it from this article.</span></span>

> [!NOTE]
> <span data-ttu-id="9335b-110">Эта статья содержит ссылки на термин «главный сервер», термин, который корпорация Майкрософт больше не использует.</span><span class="sxs-lookup"><span data-stu-id="9335b-110">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="9335b-111">Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.</span><span class="sxs-lookup"><span data-stu-id="9335b-111">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="9335b-112">Класс **\_ зоны Микрософтднс** описывает зону DNS.</span><span class="sxs-lookup"><span data-stu-id="9335b-112">The **MicrosoftDNS\_Zone** class describes a DNS Zone.</span></span> <span data-ttu-id="9335b-113">Каждый экземпляр класса **\_ зоны микрософтднс** должен быть назначен ровно одному DNS-серверу.</span><span class="sxs-lookup"><span data-stu-id="9335b-113">Every instance of the **MicrosoftDNS\_Zone** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="9335b-114">Зоны могут быть связаны с несколькими экземплярами классов [**микрософтднс \_ domain**](microsoftdns-domain.md) или [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="9335b-114">Zones may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="9335b-115">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9335b-115">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9335b-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9335b-116">Syntax</span></span>

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a><span data-ttu-id="9335b-117">Члены</span><span class="sxs-lookup"><span data-stu-id="9335b-117">Members</span></span>

<span data-ttu-id="9335b-118">Класс **микрософтднс \_ Zone** содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9335b-118">The **MicrosoftDNS\_Zone** class has these types of members:</span></span>

-   [<span data-ttu-id="9335b-119">Методы</span><span class="sxs-lookup"><span data-stu-id="9335b-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="9335b-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="9335b-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9335b-121">Методы</span><span class="sxs-lookup"><span data-stu-id="9335b-121">Methods</span></span>

<span data-ttu-id="9335b-122">Класс **микрософтднс \_ Zone** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9335b-122">The **MicrosoftDNS\_Zone** class has these methods.</span></span>



| <span data-ttu-id="9335b-123">Метод</span><span class="sxs-lookup"><span data-stu-id="9335b-123">Method</span></span>                   | <span data-ttu-id="9335b-124">Описание</span><span class="sxs-lookup"><span data-stu-id="9335b-124">Description</span></span>                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9335b-125">**ажеаллрекордс**</span><span class="sxs-lookup"><span data-stu-id="9335b-125">**AgeAllRecords**</span></span>        | <span data-ttu-id="9335b-126">Включает устаревание для некоторых или всех записей, отличных от NS и не являющихся записями SOA.</span><span class="sxs-lookup"><span data-stu-id="9335b-126">Enables aging for some or all non-NS and non-SOA records.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="9335b-127">**чанжезонетипе**</span><span class="sxs-lookup"><span data-stu-id="9335b-127">**ChangeZoneType**</span></span>       | <span data-ttu-id="9335b-128">Изменяет типы зон.</span><span class="sxs-lookup"><span data-stu-id="9335b-128">Changes zone types.</span></span> <br/> <span data-ttu-id="9335b-129">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="9335b-129">Qualifiers: Implemented</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="9335b-130">**креатезоне**</span><span class="sxs-lookup"><span data-stu-id="9335b-130">**CreateZone**</span></span>           | <span data-ttu-id="9335b-131">Создает новую зону.</span><span class="sxs-lookup"><span data-stu-id="9335b-131">Creates a new zone.</span></span> <br/> <span data-ttu-id="9335b-132">Квалификаторы: нет.</span><span class="sxs-lookup"><span data-stu-id="9335b-132">Qualifiers: None.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="9335b-133">**форцерефреш**</span><span class="sxs-lookup"><span data-stu-id="9335b-133">**ForceRefresh**</span></span>         | <span data-ttu-id="9335b-134">Принудительное обновление базы данных-получателя с главного сервера DNS.</span><span class="sxs-lookup"><span data-stu-id="9335b-134">Forces an update of the secondary from the Master DNS Server.</span></span> <br/> <span data-ttu-id="9335b-135">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="9335b-135">Qualifiers: Implemented</span></span><br/>                                                                                               |
| <span data-ttu-id="9335b-136">**жетдистингуишеднаме**</span><span class="sxs-lookup"><span data-stu-id="9335b-136">**GetDistinguishedName**</span></span> | <span data-ttu-id="9335b-137">Получает различающееся имя DS для зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-137">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="9335b-138">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="9335b-138">Qualifiers: Implemented</span></span><br/>                                                                                                                 |
| <span data-ttu-id="9335b-139">**паусезоне**</span><span class="sxs-lookup"><span data-stu-id="9335b-139">**PauseZone**</span></span>            | <span data-ttu-id="9335b-140">Приостанавливает работу зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-140">Pauses the Zone.</span></span> <br/> <span data-ttu-id="9335b-141">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="9335b-141">Qualifiers: Implemented</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="9335b-142">**релоадзоне**</span><span class="sxs-lookup"><span data-stu-id="9335b-142">**ReloadZone**</span></span>           | <span data-ttu-id="9335b-143">Перезагружает зону.</span><span class="sxs-lookup"><span data-stu-id="9335b-143">Reloads the Zone.</span></span> <br/> <span data-ttu-id="9335b-144">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="9335b-144">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="9335b-145">**ресетсекондариес**</span><span class="sxs-lookup"><span data-stu-id="9335b-145">**ResetSecondaries**</span></span>     | <span data-ttu-id="9335b-146">Сбрасывает массив вторичных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="9335b-146">Resets the secondary ip address array.</span></span> <br/> <span data-ttu-id="9335b-147">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="9335b-147">Qualifiers: Implemented</span></span><br/>                                                                                                                      |
| <span data-ttu-id="9335b-148">**ресумезоне**</span><span class="sxs-lookup"><span data-stu-id="9335b-148">**ResumeZone**</span></span>           | <span data-ttu-id="9335b-149">Возобновляет зону.</span><span class="sxs-lookup"><span data-stu-id="9335b-149">Resumes the Zone.</span></span> <br/> <span data-ttu-id="9335b-150">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="9335b-150">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="9335b-151">**упдатефромдс**</span><span class="sxs-lookup"><span data-stu-id="9335b-151">**UpdateFromDS**</span></span>         | <span data-ttu-id="9335b-152">Принудительное обновление зоны из службы каталогов (DS).</span><span class="sxs-lookup"><span data-stu-id="9335b-152">Forces an update of the Zone from the Directory Service (DS).</span></span> <span data-ttu-id="9335b-153">Чтобы этот метод был допустимым, ZoneType должен быть равен 0. зона должна храниться в DS.</span><span class="sxs-lookup"><span data-stu-id="9335b-153">For this method to be valid, the ZoneType must be 0 the Zone must indeed be stored in the DS.</span></span> <br/> <span data-ttu-id="9335b-154">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="9335b-154">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="9335b-155">**вритебаккзоне**</span><span class="sxs-lookup"><span data-stu-id="9335b-155">**WriteBackZone**</span></span>        | <span data-ttu-id="9335b-156">Сохраняет данные зоны в файл зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-156">Saves Zone data to its zone file.</span></span> <br/> <span data-ttu-id="9335b-157">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="9335b-157">Qualifiers: Implemented, static</span></span><br/>                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="9335b-158">Свойства</span><span class="sxs-lookup"><span data-stu-id="9335b-158">Properties</span></span>

<span data-ttu-id="9335b-159">Класс **микрософтднс \_ Zone** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9335b-159">The **MicrosoftDNS\_Zone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9335b-160">**Время существования**</span><span class="sxs-lookup"><span data-stu-id="9335b-160">**Aging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-161">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-163">Задает режим устаревания и очистки зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-163">Specifies the aging and scavenging behavior of the zone.</span></span> <span data-ttu-id="9335b-164">Ноль означает, что очистка отключена.</span><span class="sxs-lookup"><span data-stu-id="9335b-164">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="9335b-165">Если очистка отключена, метки времени записей в зоне не обновляются, а записи не подвергаются очистке.</span><span class="sxs-lookup"><span data-stu-id="9335b-165">When scavenging is disabled, the timestamps of records in the zone are not refreshed, and the records are not subjected to scavenging.</span></span> <span data-ttu-id="9335b-166">Если задано значение One, записи подвергаются очистке, а их метки времени обновляются, когда сервер получает запрос на динамическое обновление записей.</span><span class="sxs-lookup"><span data-stu-id="9335b-166">When set to one, records are subjected to scavenging and their timestamps are refreshed when the server receives the dynamic update request for the records.</span></span> <span data-ttu-id="9335b-167">Для зон, интегрированных с Active Directory, это значение устанавливается в свойство *дефаултагингстате* DNS-сервера, на котором создана зона.</span><span class="sxs-lookup"><span data-stu-id="9335b-167">For Active Directory-integrated zones, this value is set to the *DefaultAgingState* property of the DNS Server where the zone is created.</span></span> <span data-ttu-id="9335b-168">Для стандартных основных зон значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9335b-168">For standard primary zones, the default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-169">**алловупдате**</span><span class="sxs-lookup"><span data-stu-id="9335b-169">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-172">Указывает, принимает ли зона динамические запросы на обновление.</span><span class="sxs-lookup"><span data-stu-id="9335b-172">Indicates whether the Zone accepts dynamic update requests.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-173">**Автоматически создано**</span><span class="sxs-lookup"><span data-stu-id="9335b-173">**AutoCreated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-174">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-176">Указывает, создается ли зона с помощью автосоздания.</span><span class="sxs-lookup"><span data-stu-id="9335b-176">Indicates whether the Zone is autocreated.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-177">**аваилфорскавенжетиме**</span><span class="sxs-lookup"><span data-stu-id="9335b-177">**AvailForScavengeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-178">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-180">Указывает время, когда сервер может выполнить очистку зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-180">Specifies the time when the server may attempt scavenging the zone.</span></span> <span data-ttu-id="9335b-181">Даже если зона настроена для включения очистки DNS-сервера, она не будет пытаться очистить эту зону до этого момента.</span><span class="sxs-lookup"><span data-stu-id="9335b-181">Even if the zone is configured to enable scavenging the DNS server will not attempt scavenging this zone until after this moment.</span></span> <span data-ttu-id="9335b-182">Это значение устанавливается равным текущему времени плюс интервал обновления зоны при каждой загрузке зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-182">This value is set to the current time plus the Refresh Interval of the zone whenever the zone is loaded.</span></span> <span data-ttu-id="9335b-183">Этот параметр хранится локально и не реплицируется в другие копии зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-183">This parameter is stored locally, and is not replicated to other copies of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-184">**DataFile**</span><span class="sxs-lookup"><span data-stu-id="9335b-184">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9335b-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-187">Указывает имя файла зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-187">Indicates the name of the zone file.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-188">**дисаблевинсрекордрепликатион**</span><span class="sxs-lookup"><span data-stu-id="9335b-188">**DisableWINSRecordReplication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-189">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-191">Указывает, реплицируется ли запись WINS.</span><span class="sxs-lookup"><span data-stu-id="9335b-191">Indicates whether the WINS record is replicated.</span></span> <span data-ttu-id="9335b-192">Если задано значение TRUE, репликация записей WINS отключена.</span><span class="sxs-lookup"><span data-stu-id="9335b-192">If set to TRUE, WINS record replication is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-193">**дсинтегратед**</span><span class="sxs-lookup"><span data-stu-id="9335b-193">**DsIntegrated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-194">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-196">Указывает, является ли зона интегрированной в службу каталогов DS.</span><span class="sxs-lookup"><span data-stu-id="9335b-196">Specifies whether the zone is DS integrated.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-197">**форвардерславе**</span><span class="sxs-lookup"><span data-stu-id="9335b-197">**ForwarderSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-198">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-200">Указывает, использует ли DNS рекурсию при разрешении имен для указанной зоны прямого использования.</span><span class="sxs-lookup"><span data-stu-id="9335b-200">Indicates whether the DNS uses recursion when resolving the names for the specified forward zone.</span></span> <span data-ttu-id="9335b-201">Применимо только к зонам условного перенаправления.</span><span class="sxs-lookup"><span data-stu-id="9335b-201">Applicable to Conditional Forwarding zones only.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-202">**форвардертимеаут**</span><span class="sxs-lookup"><span data-stu-id="9335b-202">**ForwarderTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-203">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-205">Указывает время (в секундах), в течение которого DNS-сервер пересылает запрос на имя в зоне прямого подключения, прежде чем пытаться разрешить сам запрос.</span><span class="sxs-lookup"><span data-stu-id="9335b-205">Indicates the time, in seconds, a DNS server forwarding a query for the name under the forward zone waits for resolution from the forwarder before attempting to resolve the query itself.</span></span> <span data-ttu-id="9335b-206">Этот параметр применим только к прямым зонам.</span><span class="sxs-lookup"><span data-stu-id="9335b-206">This parameter is applicable to the Forward zones only.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-207">**ластсукцессфулсоачекк**</span><span class="sxs-lookup"><span data-stu-id="9335b-207">**LastSuccessfulSoaCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-208">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-210">Количество секунд с начала 1 января 1970 GMT, так как серийный номер SOA для зоны был последний раз проверен.</span><span class="sxs-lookup"><span data-stu-id="9335b-210">Number of seconds since the beginning of January 1, 1970 GMT, since the SOA serial number for the zone was last checked.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-211">**ластсукцессфулксфр**</span><span class="sxs-lookup"><span data-stu-id="9335b-211">**LastSuccessfulXfr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-212">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-214">Число секунд с начала 1 января 1970 GMT, так как зона была последний раз передана с главного сервера.</span><span class="sxs-lookup"><span data-stu-id="9335b-214">Number of seconds since the beginning of January 1, 1970 GMT, since the zone was last transferred from a master server.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-215">**локалмастерсерверс**</span><span class="sxs-lookup"><span data-stu-id="9335b-215">**LocalMasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-216">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9335b-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9335b-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-218">Локальные IP-адреса главных DNS-серверов для этой зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-218">Local IP addresses of the master DNS servers for this zone.</span></span> <span data-ttu-id="9335b-219">Если этот параметр задан, эти шаблоны перемастерсерверсся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9335b-219">If set, these masters over-ride the MasterServers found in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-220">**мастерсерверс**</span><span class="sxs-lookup"><span data-stu-id="9335b-220">**MasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-221">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9335b-221">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9335b-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-223">IP-адреса главных DNS-серверов для этой зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-223">IP addresses of the master DNS servers for this zone.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-224">**норефрешинтервал**</span><span class="sxs-lookup"><span data-stu-id="9335b-224">**NoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-225">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-227">Указывает интервал времени между последним обновлением метки времени записи и наиболее ранним моментом, когда можно обновить отметку времени.</span><span class="sxs-lookup"><span data-stu-id="9335b-227">Specifies the time interval between the last update of a record's timestamp and the earliest moment when the timestamp can be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-228">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="9335b-228">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-229">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-231">Указывает, уведомляет ли Главная зона о всех изменениях в базе данных RR.</span><span class="sxs-lookup"><span data-stu-id="9335b-231">Indicates whether the master Zone notifies secondaries of any changes in its RRs database.</span></span> <span data-ttu-id="9335b-232">Задайте значение 1, чтобы уведомить получателей.</span><span class="sxs-lookup"><span data-stu-id="9335b-232">Set to 1 to notify secondaries.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-233">**нотифисерверс**</span><span class="sxs-lookup"><span data-stu-id="9335b-233">**NotifyServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-234">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9335b-234">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9335b-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-236">Массив строк, перечисление IP-адреса DNS-серверов для уведомления об изменениях в этой зоне.</span><span class="sxs-lookup"><span data-stu-id="9335b-236">Array of strings enumerating IP addresses of DNS servers to be notified of changes in this zone.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-237">**Приостановлено**</span><span class="sxs-lookup"><span data-stu-id="9335b-237">**Paused**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-238">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-238">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-240">Указывает, приостановлена ли зона.</span><span class="sxs-lookup"><span data-stu-id="9335b-240">Indicates whether the Zone is paused.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-241">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="9335b-241">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-242">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-244">Указывает интервал обновления, в течение которого должны обновляться записи с ненулевой отметкой времени, чтобы остаться в зоне.</span><span class="sxs-lookup"><span data-stu-id="9335b-244">Specifies the refresh interval, during which the records with nonzero timestamp are expected to be refreshed to remain in the zone.</span></span> <span data-ttu-id="9335b-245">Записи, которые не обновлялись по истечении интервала обновления, могут быть удалены при следующей очистке, выполненной сервером.</span><span class="sxs-lookup"><span data-stu-id="9335b-245">Records that have not been refreshed by expiration of the Refresh interval could be removed by the next scavenging performed by a server.</span></span> <span data-ttu-id="9335b-246">Это значение никогда не должно быть меньше наибольшего периода обновления записей, зарегистрированных в зоне.</span><span class="sxs-lookup"><span data-stu-id="9335b-246">This value should never be less than the longest refresh period of the records registered in the zone.</span></span> <span data-ttu-id="9335b-247">Слишком малые значения могут привести к удалению допустимых записей DNS.</span><span class="sxs-lookup"><span data-stu-id="9335b-247">Values that are too small may lead to removal of valid DNS records.</span></span> <span data-ttu-id="9335b-248">слишком большие значения устаревают в течение срока жизни устаревших записей.</span><span class="sxs-lookup"><span data-stu-id="9335b-248">values that are too large prolong the lifetime of stale records.</span></span> <span data-ttu-id="9335b-249">Это значение устанавливается в свойство *DefaultRefreshInterval* DNS-сервера, на котором создана зона.</span><span class="sxs-lookup"><span data-stu-id="9335b-249">This value is set to the *DefaultRefreshInterval* property of the DNS server where the zone is created.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-250">**Отмена**</span><span class="sxs-lookup"><span data-stu-id="9335b-250">**Reverse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-251">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-253">Указывает, является ли зона обратным (истина) или прямой (FALSE).</span><span class="sxs-lookup"><span data-stu-id="9335b-253">Indicates whether the Zone is reverse (TRUE) or forward (FALSE).</span></span>

</dd> <dt>

<span data-ttu-id="9335b-254">**скавенжесерверс**</span><span class="sxs-lookup"><span data-stu-id="9335b-254">**ScavengeServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-255">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9335b-255">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9335b-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-257">Массив строк, перечисляющий список IP-адресов DNS-серверов, которым разрешено выполнять очистку устаревших записей этой зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-257">Array of strings that enumerates the list of IP addresses of DNS servers that are allowed to perform scavenging of stale records of this zone.</span></span> <span data-ttu-id="9335b-258">Если этот список не указан, любой основной DNS-сервер, полномочный для зоны, может очистить зону при соблюдении других необходимых условий.</span><span class="sxs-lookup"><span data-stu-id="9335b-258">If the list is not specified, any primary DNS server authoritative for the zone is allowed to scavenge the zone when other prerequisites are met.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-259">**секондарисерверс**</span><span class="sxs-lookup"><span data-stu-id="9335b-259">**SecondaryServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-260">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9335b-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9335b-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-262">Массив строк, перечисление IP-адресов DNS-серверов, которым разрешено получение этой зоны через репликацию зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-262">Array of strings enumerating IP addresses of DNS servers allowed to receive this zone through zone replication.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-263">**секуресекондариес**</span><span class="sxs-lookup"><span data-stu-id="9335b-263">**SecureSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-264">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-266">Указывает, разрешена ли зонная Отправка только определенным вторичным репликам.</span><span class="sxs-lookup"><span data-stu-id="9335b-266">Indicates whether zone transfer is allowed to designated secondaries only.</span></span> <span data-ttu-id="9335b-267">Назначенные вторичные реплики являются DNS-серверами, IP-адреса которых указаны в Секондариесипаддрессесаррай.</span><span class="sxs-lookup"><span data-stu-id="9335b-267">Designated secondaries are DNS Servers whose IP addresses are listed in SecondariesIPAddressesArray.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-268">**Завершение работы**</span><span class="sxs-lookup"><span data-stu-id="9335b-268">**Shutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-269">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-271">Указывает, истек ли срок действия копии зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-271">Indicates whether the copy of the Zone is expired.</span></span> <span data-ttu-id="9335b-272">Если задано значение TRUE, срок действия зоны истек или завершение работы.</span><span class="sxs-lookup"><span data-stu-id="9335b-272">If TRUE, the Zone is expired, or shut down.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-273">**усенбстат**</span><span class="sxs-lookup"><span data-stu-id="9335b-273">**UseNBStat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-274">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-276">Это логическое значение указывает, использует ли зона обратный просмотр NBStat.</span><span class="sxs-lookup"><span data-stu-id="9335b-276">This Boolean indicates whether the Zone uses NBStat reverse lookup.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-277">**усевинс**</span><span class="sxs-lookup"><span data-stu-id="9335b-277">**UseWins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-278">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9335b-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-280">Указывает, использует ли зона поиск WINS.</span><span class="sxs-lookup"><span data-stu-id="9335b-280">Indicates whether the Zone uses WINS look up.</span></span>

</dd> <dt>

<span data-ttu-id="9335b-281">**ZoneType**</span><span class="sxs-lookup"><span data-stu-id="9335b-281">**ZoneType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9335b-282">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9335b-282">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9335b-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9335b-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9335b-284">Указывает тип зоны.</span><span class="sxs-lookup"><span data-stu-id="9335b-284">Indicates the type of the Zone.</span></span> <span data-ttu-id="9335b-285">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="9335b-285">Valid values are:</span></span>

-   <span data-ttu-id="9335b-286">Интегрированная служба каталогов</span><span class="sxs-lookup"><span data-stu-id="9335b-286">DS integrated</span></span>
-   <span data-ttu-id="9335b-287">Первичная</span><span class="sxs-lookup"><span data-stu-id="9335b-287">Primary</span></span>
-   <span data-ttu-id="9335b-288">Вторичная</span><span class="sxs-lookup"><span data-stu-id="9335b-288">Secondary</span></span>

<span data-ttu-id="9335b-289">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="9335b-289">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="9335b-290">Дополнительные значения:</span><span class="sxs-lookup"><span data-stu-id="9335b-290">Additional values:</span></span>

-   <span data-ttu-id="9335b-291">Кэш</span><span class="sxs-lookup"><span data-stu-id="9335b-291">Cache</span></span>
-   <span data-ttu-id="9335b-292">Ловушек</span><span class="sxs-lookup"><span data-stu-id="9335b-292">Stub</span></span>
-   <span data-ttu-id="9335b-293">Сервер пересылки</span><span class="sxs-lookup"><span data-stu-id="9335b-293">Forwarder</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9335b-294">Требования</span><span class="sxs-lookup"><span data-stu-id="9335b-294">Requirements</span></span>



| <span data-ttu-id="9335b-295">Требование</span><span class="sxs-lookup"><span data-stu-id="9335b-295">Requirement</span></span> | <span data-ttu-id="9335b-296">Значение</span><span class="sxs-lookup"><span data-stu-id="9335b-296">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9335b-297">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9335b-297">Minimum supported client</span></span><br/> | <span data-ttu-id="9335b-298">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9335b-298">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9335b-299">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9335b-299">Minimum supported server</span></span><br/> | <span data-ttu-id="9335b-300">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9335b-300">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9335b-301">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9335b-301">Namespace</span></span><br/>                | <span data-ttu-id="9335b-302">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="9335b-302">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9335b-303">MOF</span><span class="sxs-lookup"><span data-stu-id="9335b-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9335b-304"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9335b-304"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9335b-305">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9335b-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9335b-306">**\_Домен микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-306">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="9335b-307">**Метод Ажеаллрекордс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-307">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="9335b-308">**Метод Чанжезонетипе \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-308">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="9335b-309">**Метод Креатезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-309">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="9335b-310">**Метод Форцерефреш \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-310">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="9335b-311">**Метод Жетдистингуишеднаме \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-311">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="9335b-312">**Метод Паусезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-312">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="9335b-313">**Метод Релоадзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-313">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="9335b-314">**Метод Ресетсекондариес \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-314">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="9335b-315">**Метод Ресумезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-315">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="9335b-316">**Метод Упдатефромдс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-316">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="9335b-317">**Метод Вритебаккзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9335b-317">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





