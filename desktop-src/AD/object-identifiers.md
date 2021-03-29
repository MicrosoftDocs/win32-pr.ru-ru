---
title: Идентификаторы объектов (AD DS)
description: Идентификаторы объектов (OID) — это уникальные числовые значения, выдаваемые различными центрами сертификации для уникальной идентификации элементов данных, синтаксисов и других частей распределенных приложений.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- идентификаторы объектов Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2019
ms.locfileid: "105654259"
---
# <a name="object-identifiers-ad-ds"></a><span data-ttu-id="422f7-104">Идентификаторы объектов (AD DS)</span><span class="sxs-lookup"><span data-stu-id="422f7-104">Object Identifiers (AD DS)</span></span>

<span data-ttu-id="422f7-105">Идентификаторы объектов (OID) — это уникальные числовые значения, выдаваемые различными центрами сертификации для уникальной идентификации элементов данных, синтаксисов и других частей распределенных приложений.</span><span class="sxs-lookup"><span data-stu-id="422f7-105">Object Identifiers (OIDs) are unique numeric values issued by various issuing authorities to uniquely identify data elements, syntaxes, and other parts of distributed applications.</span></span> <span data-ttu-id="422f7-106">OID находятся в приложениях OSI, каталогах X. 500, SNMP и других приложениях, где важна уникальность.</span><span class="sxs-lookup"><span data-stu-id="422f7-106">OIDs are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="422f7-107">OID основаны на древовидной структуре, в которой старший центр сертификации (например, ISO) выделяет ветвь дерева для подавтора, который, в свою очередь, может выделять подветви.</span><span class="sxs-lookup"><span data-stu-id="422f7-107">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a subauthority, who in turn can allocate subbranches.</span></span>

<span data-ttu-id="422f7-108">Протокол LDAP (RFC 2251) требует, чтобы служба каталогов определяла классы объектов, атрибуты и синтаксисы OID.</span><span class="sxs-lookup"><span data-stu-id="422f7-108">The LDAP protocol (RFC 2251) requires a directory service to identify object classes, attributes, and syntaxes with OIDs.</span></span> <span data-ttu-id="422f7-109">Это часть устаревшей версии LDAP X. 500.</span><span class="sxs-lookup"><span data-stu-id="422f7-109">This is part of the LDAP X.500 legacy.</span></span>

<span data-ttu-id="422f7-110">OID в домен Active Directory Services включают в себя некоторые, выданные по ISO для классов и атрибутов X. 500, а также некоторые, выпущенные корпорацией Майкрософт и другими центрами сертификации.</span><span class="sxs-lookup"><span data-stu-id="422f7-110">OIDs in Active Directory Domain Services include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft and other issuing authorities.</span></span> <span data-ttu-id="422f7-111">Нотация OID — это точечная строка чисел, например "1.2.840.113556.1.5.9", которая описывается в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="422f7-111">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.9", which is described in the following table.</span></span>



| <span data-ttu-id="422f7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="422f7-112">Value</span></span>  | <span data-ttu-id="422f7-113">Значение</span><span class="sxs-lookup"><span data-stu-id="422f7-113">Meaning</span></span>          | <span data-ttu-id="422f7-114">Описание</span><span class="sxs-lookup"><span data-stu-id="422f7-114">Description</span></span>                                              |
|--------|------------------|----------------------------------------------------------|
| <span data-ttu-id="422f7-115">1</span><span class="sxs-lookup"><span data-stu-id="422f7-115">1</span></span>      | <span data-ttu-id="422f7-116">ISO</span><span class="sxs-lookup"><span data-stu-id="422f7-116">ISO</span></span>              | <span data-ttu-id="422f7-117">Определяет корневой центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="422f7-117">Identifies the root authority.</span></span>                           |
| <span data-ttu-id="422f7-118">2</span><span class="sxs-lookup"><span data-stu-id="422f7-118">2</span></span>      | <span data-ttu-id="422f7-119">ANSI</span><span class="sxs-lookup"><span data-stu-id="422f7-119">ANSI</span></span>             | <span data-ttu-id="422f7-120">Обозначение группы, назначенное по ISO.</span><span class="sxs-lookup"><span data-stu-id="422f7-120">Group designation assigned by ISO.</span></span>                       |
| <span data-ttu-id="422f7-121">840</span><span class="sxs-lookup"><span data-stu-id="422f7-121">840</span></span>    | <span data-ttu-id="422f7-122">США</span><span class="sxs-lookup"><span data-stu-id="422f7-122">USA</span></span>              | <span data-ttu-id="422f7-123">Обозначение страны или региона, назначенное группой.</span><span class="sxs-lookup"><span data-stu-id="422f7-123">Country/region designation assigned by the group.</span></span>        |
| <span data-ttu-id="422f7-124">113556</span><span class="sxs-lookup"><span data-stu-id="422f7-124">113556</span></span> | <span data-ttu-id="422f7-125">Microsoft</span><span class="sxs-lookup"><span data-stu-id="422f7-125">Microsoft</span></span>        | <span data-ttu-id="422f7-126">Обозначение Организации, назначенное страной или регионом.</span><span class="sxs-lookup"><span data-stu-id="422f7-126">Organization designation assigned by the country/region.</span></span> |
| <span data-ttu-id="422f7-127">1</span><span class="sxs-lookup"><span data-stu-id="422f7-127">1</span></span>      | <span data-ttu-id="422f7-128">Active Directory</span><span class="sxs-lookup"><span data-stu-id="422f7-128">Active Directory</span></span> | <span data-ttu-id="422f7-129">Назначено Организацией.</span><span class="sxs-lookup"><span data-stu-id="422f7-129">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="422f7-130">5</span><span class="sxs-lookup"><span data-stu-id="422f7-130">5</span></span>      | <span data-ttu-id="422f7-131">Классы</span><span class="sxs-lookup"><span data-stu-id="422f7-131">Classes</span></span>          | <span data-ttu-id="422f7-132">Назначено Организацией.</span><span class="sxs-lookup"><span data-stu-id="422f7-132">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="422f7-133">9</span><span class="sxs-lookup"><span data-stu-id="422f7-133">9</span></span>      | <span data-ttu-id="422f7-134">класс **пользователя**</span><span class="sxs-lookup"><span data-stu-id="422f7-134">**user** class</span></span>   | <span data-ttu-id="422f7-135">Назначено Организацией.</span><span class="sxs-lookup"><span data-stu-id="422f7-135">Assigned by the organization.</span></span>                            |



 

<span data-ttu-id="422f7-136">Дополнительные сведения и описание двух процедур, используемых для получения допустимых идентификаторов OID для использования при расширении схемы Active Directory, см. в разделе [Получение идентификатора объекта](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="422f7-136">For more information, and a discussion of two procedures used to obtain valid OIDs for use in extending the Active Directory schema, see [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>

 

 




