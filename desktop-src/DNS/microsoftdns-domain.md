---
title: Класс MicrosoftDNS_Domain
description: '\_Доменный класс микрософтднс представляет домен в ИЕРАРХИИ DNS.'
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- DNS класса MicrosoftDNS_Domain
- DNS-MicrosoftDNS_Domain класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135918"
---
# <a name="microsoftdns_domain-class"></a><span data-ttu-id="8600f-105">\_Класс домена микрософтднс</span><span class="sxs-lookup"><span data-stu-id="8600f-105">MicrosoftDNS\_Domain class</span></span>

<span data-ttu-id="8600f-106">**\_ Доменный класс Микрософтднс** представляет домен в иерархии DNS.</span><span class="sxs-lookup"><span data-stu-id="8600f-106">The **MicrosoftDNS\_Domain** class represents a Domain in a DNS hierarchy.</span></span>

<span data-ttu-id="8600f-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="8600f-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8600f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8600f-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="8600f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="8600f-109">Members</span></span>

<span data-ttu-id="8600f-110">Класс **\_ домена микрософтднс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8600f-110">The **MicrosoftDNS\_Domain** class has these types of members:</span></span>

-   [<span data-ttu-id="8600f-111">Методы</span><span class="sxs-lookup"><span data-stu-id="8600f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8600f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="8600f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8600f-113">Методы</span><span class="sxs-lookup"><span data-stu-id="8600f-113">Methods</span></span>

<span data-ttu-id="8600f-114">Класс **\_ домена микрософтднс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8600f-114">The **MicrosoftDNS\_Domain** class has these methods.</span></span>



| <span data-ttu-id="8600f-115">Метод</span><span class="sxs-lookup"><span data-stu-id="8600f-115">Method</span></span>                   | <span data-ttu-id="8600f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8600f-116">Description</span></span>                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8600f-117">**жетдистингуишеднаме**</span><span class="sxs-lookup"><span data-stu-id="8600f-117">**GetDistinguishedName**</span></span> | <span data-ttu-id="8600f-118">Получает различающееся имя DS для зоны.</span><span class="sxs-lookup"><span data-stu-id="8600f-118">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="8600f-119">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="8600f-119">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8600f-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="8600f-120">Properties</span></span>

<span data-ttu-id="8600f-121">Класс **\_ домена микрософтднс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8600f-121">The **MicrosoftDNS\_Domain** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8600f-122">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="8600f-122">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8600f-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8600f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8600f-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8600f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8600f-125">Имя контейнера домена, который может быть зоной, кэшем или Русинтс.</span><span class="sxs-lookup"><span data-stu-id="8600f-125">Name of the container of the domain, which could be a Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="8600f-126">В случаях, когда контейнер является зоной (экземпляром класса [**микрософтднс \_ Zone**](microsoftdns-zone.md) ), это свойство содержит полное доменное имя зоны.</span><span class="sxs-lookup"><span data-stu-id="8600f-126">In cases where the Container is a Zone (an instance of the [**MicrosoftDNS\_Zone**](microsoftdns-zone.md) class), this property contains the FQDN of the Zone.</span></span>

<span data-ttu-id="8600f-127">Если контейнер является корневой зоной, \\ следует использовать строку. \\</span><span class="sxs-lookup"><span data-stu-id="8600f-127">When the Container is the root zone, the string \\.\\ should be used.</span></span>

<span data-ttu-id="8600f-128">В случаях, когда контейнер является кэшем DNS записей ресурсов (экземпляр класса [**\_ кэша микрософтднс**](microsoftdns-cache.md) ), для этого свойства задается строка \\ .. Кэш \\ .</span><span class="sxs-lookup"><span data-stu-id="8600f-128">In cases where the Container is the DNS cache of resource records (an instance of the [**MicrosoftDNS\_Cache**](microsoftdns-cache.md) class), this property is set to the string \\..Cache\\.</span></span>

<span data-ttu-id="8600f-129">Если контейнером является Русинтс (экземпляр класса [**микрософтднс \_ русинтс**](microsoftdns-roothints.md) ), этому свойству должно быть присвоено значение \\ . Русинтс \\ .</span><span class="sxs-lookup"><span data-stu-id="8600f-129">If the Container is RootHints (an instance of the [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md) class), this property should be set to \\..RootHints\\.</span></span>

</dd> <dt>

<span data-ttu-id="8600f-130">**днссервернаме**</span><span class="sxs-lookup"><span data-stu-id="8600f-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8600f-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8600f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8600f-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8600f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8600f-133">FQDN или IP-адрес DNS-сервера, содержащего домен.</span><span class="sxs-lookup"><span data-stu-id="8600f-133">FQDN or IP address of the DNS Server that contains the domain.</span></span>

</dd> <dt>

<span data-ttu-id="8600f-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="8600f-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8600f-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8600f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8600f-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8600f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8600f-137">Полное доменное имя домена.</span><span class="sxs-lookup"><span data-stu-id="8600f-137">FQDN of the domain.</span></span>

<span data-ttu-id="8600f-138">Для экземпляров кэша DNS или Русинтс строки \\ .. Кэш \\ и \\ .. Русинтс \\ следует использовать соответственно.</span><span class="sxs-lookup"><span data-stu-id="8600f-138">For instances of DNS Cache or RootHints, the strings \\..Cache\\ and \\..RootHints\\ should be used, respectively.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8600f-139">Требования</span><span class="sxs-lookup"><span data-stu-id="8600f-139">Requirements</span></span>



| <span data-ttu-id="8600f-140">Требование</span><span class="sxs-lookup"><span data-stu-id="8600f-140">Requirement</span></span> | <span data-ttu-id="8600f-141">Значение</span><span class="sxs-lookup"><span data-stu-id="8600f-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8600f-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8600f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8600f-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8600f-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8600f-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8600f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8600f-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8600f-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8600f-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8600f-146">Namespace</span></span><br/>                | <span data-ttu-id="8600f-147">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="8600f-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8600f-148">MOF</span><span class="sxs-lookup"><span data-stu-id="8600f-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8600f-149"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8600f-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8600f-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8600f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8600f-151">**Метод Жетдистингуишеднаме \_ класса домена микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="8600f-151">**GetDistinguishedName Method of the MicrosoftDNS\_Domain Class**</span></span>](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





