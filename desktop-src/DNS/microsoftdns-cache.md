---
title: Класс MicrosoftDNS_Cache
description: '\_Класс кэша микрософтднс описывает существующий кэш на DNS-сервере.'
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- DNS класса MicrosoftDNS_Cache
- DNS-MicrosoftDNS_Cache класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071634"
---
# <a name="microsoftdns_cache-class"></a><span data-ttu-id="1fb78-105">\_Класс кэша микрософтднс</span><span class="sxs-lookup"><span data-stu-id="1fb78-105">MicrosoftDNS\_Cache class</span></span>

<span data-ttu-id="1fb78-106">Класс **\_ кэша микрософтднс** описывает существующий кэш на DNS-сервере.</span><span class="sxs-lookup"><span data-stu-id="1fb78-106">The **MicrosoftDNS\_Cache** class describes a cache existing on a DNS Server.</span></span> <span data-ttu-id="1fb78-107">Этот класс упрощает визуализацию включения DNS-объектов, а не представляет реальный объект.</span><span class="sxs-lookup"><span data-stu-id="1fb78-107">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span> <span data-ttu-id="1fb78-108">Класс **\_ кэша микрософтднс** — это контейнер для записей ресурсов, кэшированных DNS-сервером.</span><span class="sxs-lookup"><span data-stu-id="1fb78-108">The **MicrosoftDNS\_Cache** class is a container for the resource records cached by the DNS Server.</span></span> <span data-ttu-id="1fb78-109">Не путайте это с файлом кэша, содержащим корневые ссылки.</span><span class="sxs-lookup"><span data-stu-id="1fb78-109">Do not confuse this with a Cache file that contains root hints.</span></span>

<span data-ttu-id="1fb78-110">Каждый экземпляр **\_ кэша микрософтднс** класса должен быть назначен ровно одному DNS-серверу.</span><span class="sxs-lookup"><span data-stu-id="1fb78-110">Every instance of the class **MicrosoftDNS\_Cache** must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="1fb78-111">Он может быть связан с несколькими экземплярами классов [**микрософтднс \_ domain**](microsoftdns-domain.md) или [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="1fb78-111">It may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="1fb78-112">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="1fb78-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb78-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fb78-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="1fb78-114">Члены</span><span class="sxs-lookup"><span data-stu-id="1fb78-114">Members</span></span>

<span data-ttu-id="1fb78-115">Класс **\_ кэша микрософтднс** содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1fb78-115">The **MicrosoftDNS\_Cache** class has these types of members:</span></span>

-   [<span data-ttu-id="1fb78-116">Методы</span><span class="sxs-lookup"><span data-stu-id="1fb78-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1fb78-117">Методы</span><span class="sxs-lookup"><span data-stu-id="1fb78-117">Methods</span></span>

<span data-ttu-id="1fb78-118">Класс **\_ кэша микрософтднс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1fb78-118">The **MicrosoftDNS\_Cache** class has these methods.</span></span>



| <span data-ttu-id="1fb78-119">Метод</span><span class="sxs-lookup"><span data-stu-id="1fb78-119">Method</span></span>                   | <span data-ttu-id="1fb78-120">Описание</span><span class="sxs-lookup"><span data-stu-id="1fb78-120">Description</span></span>                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb78-121">**ClearCache**</span><span class="sxs-lookup"><span data-stu-id="1fb78-121">**ClearCache**</span></span>           | <span data-ttu-id="1fb78-122">Очищает кэш DNS-сервера записей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fb78-122">Clears the DNS Server cache of resource records.</span></span> <br/> <span data-ttu-id="1fb78-123">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="1fb78-123">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="1fb78-124">**жетдистингуишеднаме**</span><span class="sxs-lookup"><span data-stu-id="1fb78-124">**GetDistinguishedName**</span></span> | <span data-ttu-id="1fb78-125">Извлекает различающееся имя зоны.</span><span class="sxs-lookup"><span data-stu-id="1fb78-125">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="1fb78-126">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="1fb78-126">Qualifiers: Implemented</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="1fb78-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1fb78-127">Requirements</span></span>



| <span data-ttu-id="1fb78-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1fb78-128">Requirement</span></span> | <span data-ttu-id="1fb78-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1fb78-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb78-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fb78-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb78-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1fb78-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1fb78-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fb78-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb78-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1fb78-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1fb78-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1fb78-134">Namespace</span></span><br/>                | <span data-ttu-id="1fb78-135">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="1fb78-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="1fb78-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1fb78-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fb78-137"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fb78-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb78-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fb78-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb78-139">**\_Домен микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="1fb78-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="1fb78-140">**Метод ClearCache \_ класса кэша микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="1fb78-140">**ClearCache Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-clearcache.md)
</dt> <dt>

[<span data-ttu-id="1fb78-141">**Метод Жетдистингуишеднаме \_ класса кэша микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="1fb78-141">**GetDistinguishedName Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





