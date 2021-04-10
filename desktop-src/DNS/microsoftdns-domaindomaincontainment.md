---
title: Класс MicrosoftDNS_DomainDomainContainment
description: Класс Микрософтднс \_ домаиндомаинконтаинмент используется для включения домена. Домены DNS могут содержать другие домены DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- DNS класса MicrosoftDNS_DomainDomainContainment
- DNS-MicrosoftDNS_DomainDomainContainment класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071869"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a><span data-ttu-id="5a546-105">\_Класс микрософтднс домаиндомаинконтаинмент</span><span class="sxs-lookup"><span data-stu-id="5a546-105">MicrosoftDNS\_DomainDomainContainment class</span></span>

<span data-ttu-id="5a546-106">Класс **микрософтднс \_ домаиндомаинконтаинмент** используется для включения домена. Домены DNS могут содержать другие домены DNS.</span><span class="sxs-lookup"><span data-stu-id="5a546-106">The **MicrosoftDNS\_DomainDomainContainment** class is used for domain containment; DNS domains may contain other DNS domains.</span></span> <span data-ttu-id="5a546-107">Каждый экземпляр класса [**\_ домена микрософтднс**](microsoftdns-domain.md) может содержать несколько других экземпляров **\_ домена микрософтднс**.</span><span class="sxs-lookup"><span data-stu-id="5a546-107">Every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class may contain multiple other instances of **MicrosoftDNS\_Domain**.</span></span> <span data-ttu-id="5a546-108">Экземпляр объекта **\_ домена микрософтднс** напрямую содержится в не более чем в одном **\_ домене микрософтднс** более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5a546-108">An instance of a **MicrosoftDNS\_Domain** object is directly contained in no more than one higher level **MicrosoftDNS\_Domain**.</span></span>

<span data-ttu-id="5a546-109">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="5a546-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a546-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a546-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="5a546-111">Члены</span><span class="sxs-lookup"><span data-stu-id="5a546-111">Members</span></span>

<span data-ttu-id="5a546-112">Класс **микрософтднс \_ домаиндомаинконтаинмент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5a546-112">The **MicrosoftDNS\_DomainDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="5a546-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a546-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a546-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a546-114">Properties</span></span>

<span data-ttu-id="5a546-115">Класс **микрософтднс \_ домаиндомаинконтаинмент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5a546-115">The **MicrosoftDNS\_DomainDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a546-116">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="5a546-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a546-117">Тип данных: **\_ домен микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="5a546-117">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="5a546-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a546-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a546-119">Квалификаторы: Key, Max (1), reoverride ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="5a546-119">Qualifiers: Key, Max(1), Override("GroupComponent")</span></span>

<span data-ttu-id="5a546-120">Описание: домен более высокого уровня, зона, кэш или Русинтс.</span><span class="sxs-lookup"><span data-stu-id="5a546-120">Description: A higher level Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="5a546-121">Наследуется от \_ компонента CIM</span><span class="sxs-lookup"><span data-stu-id="5a546-121">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="5a546-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5a546-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a546-123">Тип данных: **\_ домен микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="5a546-123">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="5a546-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a546-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a546-125">Квалификаторы: ключ, переопределение ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="5a546-125">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="5a546-126">Описание: домен, содержащийся в домене более высокого уровня, в зоне, кэше или Русинтс.</span><span class="sxs-lookup"><span data-stu-id="5a546-126">Description: The Domain contained by a higher level Domain, Zone, Cache or RootHints.</span></span>

<span data-ttu-id="5a546-127">Наследуется от \_ компонента CIM.</span><span class="sxs-lookup"><span data-stu-id="5a546-127">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a546-128">Требования</span><span class="sxs-lookup"><span data-stu-id="5a546-128">Requirements</span></span>



| <span data-ttu-id="5a546-129">Требование</span><span class="sxs-lookup"><span data-stu-id="5a546-129">Requirement</span></span> | <span data-ttu-id="5a546-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5a546-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a546-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a546-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5a546-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5a546-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5a546-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a546-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5a546-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a546-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5a546-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5a546-135">Namespace</span></span><br/>                | <span data-ttu-id="5a546-136">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="5a546-136">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5a546-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5a546-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a546-138"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a546-138"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a546-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a546-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a546-140">**Микрософтднс \_ домаинресаурцерекордконтаинмент**</span><span class="sxs-lookup"><span data-stu-id="5a546-140">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="5a546-141">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="5a546-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="5a546-142">**Микрософтднс \_ сервердомаинконтаинмент**</span><span class="sxs-lookup"><span data-stu-id="5a546-142">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





