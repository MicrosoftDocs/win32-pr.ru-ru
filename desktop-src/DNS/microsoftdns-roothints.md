---
title: Класс MicrosoftDNS_RootHints
description: Класс Микрософтднс \_ русинтс описывает русинтс, хранимые в файле кэша на DNS-сервере. Этот класс упрощает визуализацию включения DNS-объектов, а не представляет реальный объект.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- DNS класса MicrosoftDNS_RootHints
- DNS-MicrosoftDNS_RootHints класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136218"
---
# <a name="microsoftdns_roothints-class"></a><span data-ttu-id="ac978-106">\_Класс микрософтднс русинтс</span><span class="sxs-lookup"><span data-stu-id="ac978-106">MicrosoftDNS\_RootHints class</span></span>

<span data-ttu-id="ac978-107">Класс **микрософтднс \_ Русинтс** описывает русинтс, хранимые в файле кэша на DNS-сервере.</span><span class="sxs-lookup"><span data-stu-id="ac978-107">The **MicrosoftDNS\_RootHints** class describes the RootHints stored in a Cache file on a DNS Server.</span></span> <span data-ttu-id="ac978-108">Этот класс упрощает визуализацию включения DNS-объектов, а не представляет реальный объект.</span><span class="sxs-lookup"><span data-stu-id="ac978-108">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span>

<span data-ttu-id="ac978-109">**Микрософтднс \_ Русинтс** — это контейнер для записей ресурсов, хранимых DNS-сервером в файле кэша.</span><span class="sxs-lookup"><span data-stu-id="ac978-109">**MicrosoftDNS\_RootHints** is a container for the resource records stored by the DNS Server in a Cache file.</span></span> <span data-ttu-id="ac978-110">Каждый экземпляр класса **микрософтднс \_ русинтс** должен быть назначен ровно одному DNS-серверу.</span><span class="sxs-lookup"><span data-stu-id="ac978-110">Every instance of the **MicrosoftDNS\_RootHints** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="ac978-111">Он может быть связан с несколькими экземплярами класса [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="ac978-111">It may be associated with multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

<span data-ttu-id="ac978-112">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="ac978-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac978-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac978-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="ac978-114">Члены</span><span class="sxs-lookup"><span data-stu-id="ac978-114">Members</span></span>

<span data-ttu-id="ac978-115">Класс **микрософтднс \_ русинтс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ac978-115">The **MicrosoftDNS\_RootHints** class has these types of members:</span></span>

-   [<span data-ttu-id="ac978-116">Методы</span><span class="sxs-lookup"><span data-stu-id="ac978-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ac978-117">Методы</span><span class="sxs-lookup"><span data-stu-id="ac978-117">Methods</span></span>

<span data-ttu-id="ac978-118">Класс **микрософтднс \_ русинтс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ac978-118">The **MicrosoftDNS\_RootHints** class has these methods.</span></span>



| <span data-ttu-id="ac978-119">Метод</span><span class="sxs-lookup"><span data-stu-id="ac978-119">Method</span></span>                        | <span data-ttu-id="ac978-120">Описание</span><span class="sxs-lookup"><span data-stu-id="ac978-120">Description</span></span>                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac978-121">**жетдистингуишеднаме**</span><span class="sxs-lookup"><span data-stu-id="ac978-121">**GetDistinguishedName**</span></span>      | <span data-ttu-id="ac978-122">Извлекает различающееся имя зоны.</span><span class="sxs-lookup"><span data-stu-id="ac978-122">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="ac978-123">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="ac978-123">Qualifiers: Implemented</span></span><br/>   |
| <span data-ttu-id="ac978-124">**вритебаккрусинтдатафиле**</span><span class="sxs-lookup"><span data-stu-id="ac978-124">**WriteBackRootHintDatafile**</span></span> | <span data-ttu-id="ac978-125">Записывает Русинтс обратно в файл кэша DNS.</span><span class="sxs-lookup"><span data-stu-id="ac978-125">Writes the RootHints back to the DNS Cache file.</span></span> <br/> <span data-ttu-id="ac978-126">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="ac978-126">Qualifiers: Implemented</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ac978-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ac978-127">Requirements</span></span>



| <span data-ttu-id="ac978-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ac978-128">Requirement</span></span> | <span data-ttu-id="ac978-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ac978-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac978-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac978-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ac978-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac978-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ac978-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac978-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ac978-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac978-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ac978-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac978-134">Namespace</span></span><br/>                | <span data-ttu-id="ac978-135">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="ac978-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ac978-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ac978-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac978-137"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac978-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac978-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac978-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac978-139">**\_Домен микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="ac978-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="ac978-140">**Метод Вритебаккрусинтдатафиле \_ класса Русинтс микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="ac978-140">**WriteBackRootHintDatafile Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[<span data-ttu-id="ac978-141">**Метод Жетдистингуишеднаме \_ класса Русинтс микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="ac978-141">**GetDistinguishedName Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





