---
title: Класс MicrosoftDNS_ServerDomainContainment
description: Каждый экземпляр \_ класса WMI ассоциации сервера микрософтднс может содержать несколько экземпляров \_ класса домена микрософтднс.
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- DNS класса MicrosoftDNS_ServerDomainContainment
- DNS-MicrosoftDNS_ServerDomainContainment класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801349"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a><span data-ttu-id="66ec0-105">\_Класс микрософтднс сервердомаинконтаинмент</span><span class="sxs-lookup"><span data-stu-id="66ec0-105">MicrosoftDNS\_ServerDomainContainment class</span></span>

<span data-ttu-id="66ec0-106">Каждый экземпляр класса WMI [**ассоциации \_ сервера микрософтднс**](microsoftdns-server.md) может содержать несколько экземпляров класса [**\_ домена микрософтднс**](microsoftdns-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="66ec0-106">Every instance of the [**MicrosoftDNS\_Server**](microsoftdns-server.md) association WMI class may contain multiple instances of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class.</span></span> <span data-ttu-id="66ec0-107">Каждый экземпляр класса **\_ домена микрософтднс** принадлежит одному экземпляру класса **\_ сервера микрософтднс** и определен как ненадежный для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="66ec0-107">Every instance of the **MicrosoftDNS\_Domain** class belongs to a single instance of the **MicrosoftDNS\_Server** class, and is defined to be weak to that server.</span></span>

<span data-ttu-id="66ec0-108">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="66ec0-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ec0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66ec0-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="66ec0-110">Члены</span><span class="sxs-lookup"><span data-stu-id="66ec0-110">Members</span></span>

<span data-ttu-id="66ec0-111">Класс **микрософтднс \_ сервердомаинконтаинмент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="66ec0-111">The **MicrosoftDNS\_ServerDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="66ec0-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="66ec0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66ec0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="66ec0-113">Properties</span></span>

<span data-ttu-id="66ec0-114">Класс **микрософтднс \_ сервердомаинконтаинмент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="66ec0-114">The **MicrosoftDNS\_ServerDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66ec0-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="66ec0-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ec0-116">Тип данных: **микрософтднс \_ Server**</span><span class="sxs-lookup"><span data-stu-id="66ec0-116">Data type: **MicrosoftDNS\_Server**</span></span>
</dt> <dt>

<span data-ttu-id="66ec0-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66ec0-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66ec0-118">Квалификаторы: ключ, переопределение ("GroupComponent"), min (1), Max (1)</span><span class="sxs-lookup"><span data-stu-id="66ec0-118">Qualifiers: Key, Override ("GroupComponent"), Min (1), Max (1)</span></span>

<span data-ttu-id="66ec0-119">Описание: DNS-сервер.</span><span class="sxs-lookup"><span data-stu-id="66ec0-119">Description: The DNS Server.</span></span>

<span data-ttu-id="66ec0-120">Наследуется от **\_ компонента CIM**.</span><span class="sxs-lookup"><span data-stu-id="66ec0-120">Inherited from **CIM\_Component**.</span></span>

</dd> <dt>

<span data-ttu-id="66ec0-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="66ec0-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ec0-122">Тип данных: **\_ домен микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="66ec0-122">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="66ec0-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66ec0-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66ec0-124">Квалификаторы: ключ, переопределение ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="66ec0-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="66ec0-125">Описание: домен, зона, кэш или Русинтс, управляемые DNS-сервером.</span><span class="sxs-lookup"><span data-stu-id="66ec0-125">Description: A Domain, Zone, Cache, or RootHints managed by the DNS Server.</span></span>

<span data-ttu-id="66ec0-126">Наследуется от **\_ компонента CIM**.</span><span class="sxs-lookup"><span data-stu-id="66ec0-126">Inherited from **CIM\_Component**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66ec0-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66ec0-127">Remarks</span></span>

<span data-ttu-id="66ec0-128">Класс **микрософтднс \_ сервердомаинконтаинмент** является производным от класса **\_ компонента CIM** .</span><span class="sxs-lookup"><span data-stu-id="66ec0-128">The **MicrosoftDNS\_ServerDomainContainment** class is derived from the **CIM\_Component** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ec0-129">Требования</span><span class="sxs-lookup"><span data-stu-id="66ec0-129">Requirements</span></span>



| <span data-ttu-id="66ec0-130">Требование</span><span class="sxs-lookup"><span data-stu-id="66ec0-130">Requirement</span></span> | <span data-ttu-id="66ec0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="66ec0-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66ec0-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66ec0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="66ec0-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="66ec0-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="66ec0-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66ec0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="66ec0-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66ec0-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="66ec0-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="66ec0-136">Namespace</span></span><br/>                | <span data-ttu-id="66ec0-137">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="66ec0-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="66ec0-138">MOF</span><span class="sxs-lookup"><span data-stu-id="66ec0-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66ec0-139"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66ec0-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ec0-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66ec0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ec0-141">**Микрософтднс \_ домаиндомаинконтаинмент**</span><span class="sxs-lookup"><span data-stu-id="66ec0-141">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="66ec0-142">**Микрософтднс \_ домаинресаурцерекордконтаинмент**</span><span class="sxs-lookup"><span data-stu-id="66ec0-142">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="66ec0-143">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="66ec0-143">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





