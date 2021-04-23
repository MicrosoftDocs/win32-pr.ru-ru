---
title: Класс MicrosoftDNS_DomainResourceRecordContainment
description: Класс Микрософтднс \_ домаинресаурцерекордконтаинмент используется для включения записи RR; каждый экземпляр \_ домена микрософтднс может содержать несколько экземпляров \_ класса микрософтднс ресаурцерекорд.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- DNS класса MicrosoftDNS_DomainResourceRecordContainment
- DNS-MicrosoftDNS_DomainResourceRecordContainment класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490647"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a><span data-ttu-id="289ae-105">\_Класс микрософтднс домаинресаурцерекордконтаинмент</span><span class="sxs-lookup"><span data-stu-id="289ae-105">MicrosoftDNS\_DomainResourceRecordContainment class</span></span>

<span data-ttu-id="289ae-106">Класс **микрософтднс \_ домаинресаурцерекордконтаинмент** используется для включения записи RR; каждый экземпляр [**\_ домена микрософтднс**](microsoftdns-domain.md) может содержать несколько экземпляров класса [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="289ae-106">The **MicrosoftDNS\_DomainResourceRecordContainment** class is used for RR containment; every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) may contain multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span> <span data-ttu-id="289ae-107">Каждый экземпляр класса **микрософтднс \_ ресаурцерекорд** принадлежит одному экземпляру класса **\_ домена микрософтднс** и определен как слабый для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="289ae-107">Every instance of the **MicrosoftDNS\_ResourceRecord** class belongs to a single instance of the **MicrosoftDNS\_Domain** class, and is defined to be weak to that instance.</span></span>

<span data-ttu-id="289ae-108">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="289ae-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="289ae-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="289ae-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="289ae-110">Члены</span><span class="sxs-lookup"><span data-stu-id="289ae-110">Members</span></span>

<span data-ttu-id="289ae-111">Класс **микрософтднс \_ домаинресаурцерекордконтаинмент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="289ae-111">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="289ae-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="289ae-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="289ae-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="289ae-113">Properties</span></span>

<span data-ttu-id="289ae-114">Класс **микрософтднс \_ домаинресаурцерекордконтаинмент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="289ae-114">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="289ae-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="289ae-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289ae-116">Тип данных: **\_ домен микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="289ae-116">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="289ae-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289ae-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="289ae-118">Квалификаторы: ключ, переопределение ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="289ae-118">Qualifiers: Key, Override("GroupComponent")</span></span>

<span data-ttu-id="289ae-119">Описание: зона, кэш, Русинтс или домен, непосредственно содержащий запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="289ae-119">Description: The Zone, Cache, RootHints or Domain directly containing the Resource Record.</span></span>

<span data-ttu-id="289ae-120">Наследуется от \_ компонента CIM</span><span class="sxs-lookup"><span data-stu-id="289ae-120">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="289ae-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="289ae-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="289ae-122">Тип данных: **микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="289ae-122">Data type: **MicrosoftDNS\_ResourceRecord**</span></span>
</dt> <dt>

<span data-ttu-id="289ae-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="289ae-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="289ae-124">Квалификаторы: ключ, переопределение ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="289ae-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="289ae-125">Описание: запись ресурса, содержащаяся в домене, зоне, кэше или Русинтс.</span><span class="sxs-lookup"><span data-stu-id="289ae-125">Description: The resource record contained in a Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="289ae-126">Наследуется от \_ компонента CIM.</span><span class="sxs-lookup"><span data-stu-id="289ae-126">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="289ae-127">Требования</span><span class="sxs-lookup"><span data-stu-id="289ae-127">Requirements</span></span>



| <span data-ttu-id="289ae-128">Требование</span><span class="sxs-lookup"><span data-stu-id="289ae-128">Requirement</span></span> | <span data-ttu-id="289ae-129">Значение</span><span class="sxs-lookup"><span data-stu-id="289ae-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="289ae-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="289ae-130">Minimum supported client</span></span><br/> | <span data-ttu-id="289ae-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="289ae-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="289ae-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="289ae-132">Minimum supported server</span></span><br/> | <span data-ttu-id="289ae-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="289ae-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="289ae-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="289ae-134">Namespace</span></span><br/>                | <span data-ttu-id="289ae-135">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="289ae-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="289ae-136">MOF</span><span class="sxs-lookup"><span data-stu-id="289ae-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="289ae-137"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="289ae-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="289ae-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="289ae-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="289ae-139">**Микрософтднс \_ сервердомаинконтаинмент**</span><span class="sxs-lookup"><span data-stu-id="289ae-139">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="289ae-140">**Микрософтднс \_ домаиндомаинконтаинмент**</span><span class="sxs-lookup"><span data-stu-id="289ae-140">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="289ae-141">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="289ae-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





