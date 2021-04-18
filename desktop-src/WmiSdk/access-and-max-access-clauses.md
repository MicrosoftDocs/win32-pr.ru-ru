---
description: Каждое определение объекта MIB содержит предложение доступа (в формате CLR) или MAX-ACCESS (SNMPv2C), которое определяет права доступа к объекту.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Предложения доступа и MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693330"
---
# <a name="access-and-max-access-clauses"></a><span data-ttu-id="70fbc-103">Предложения доступа и MAX-ACCESS</span><span class="sxs-lookup"><span data-stu-id="70fbc-103">ACCESS and MAX-ACCESS Clauses</span></span>

<span data-ttu-id="70fbc-104">Каждое определение объекта MIB содержит предложение доступа (в формате CLR) или MAX-ACCESS (SNMPv2C), которое определяет права доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="70fbc-104">Each MIB object definition contains either an ACCESS (SNMPv1) or MAX-ACCESS (SNMPv2C) clause that defines the access rights to the object.</span></span>

> [!Note]  
> <span data-ttu-id="70fbc-105">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="70fbc-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="70fbc-106">В следующей таблице приведено сопоставление предложения доступа в некотором списке.</span><span class="sxs-lookup"><span data-stu-id="70fbc-106">The following table lists the mapping of the SNMPv1 ACCESS clause.</span></span>



| <span data-ttu-id="70fbc-107">Предложение доступа MIB</span><span class="sxs-lookup"><span data-stu-id="70fbc-107">MIB ACCESS clause</span></span> | <span data-ttu-id="70fbc-108">Квалификатор CIM</span><span class="sxs-lookup"><span data-stu-id="70fbc-108">CIM qualifier</span></span>       |
|-------------------|---------------------|
| <span data-ttu-id="70fbc-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70fbc-109">read-only</span></span>         | <span data-ttu-id="70fbc-110">**Чтение**</span><span class="sxs-lookup"><span data-stu-id="70fbc-110">**Read**</span></span>            |
| <span data-ttu-id="70fbc-111">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="70fbc-111">read-write</span></span>        | <span data-ttu-id="70fbc-112">**Чтение**, **запись**</span><span class="sxs-lookup"><span data-stu-id="70fbc-112">**Read**, **Write**</span></span> |
| <span data-ttu-id="70fbc-113">только запись</span><span class="sxs-lookup"><span data-stu-id="70fbc-113">write-only</span></span>        | <span data-ttu-id="70fbc-114">**Запись**</span><span class="sxs-lookup"><span data-stu-id="70fbc-114">**Write**</span></span>           |
| <span data-ttu-id="70fbc-115">недоступно</span><span class="sxs-lookup"><span data-stu-id="70fbc-115">not-accessible</span></span>    | <span data-ttu-id="70fbc-116">**\_Недоступно**</span><span class="sxs-lookup"><span data-stu-id="70fbc-116">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="70fbc-117">В следующей таблице перечислены сопоставления предложения MAX-ACCESS SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="70fbc-117">The following table lists the mapping of the SNMPv2C MAX-ACCESS clause.</span></span>



| <span data-ttu-id="70fbc-118">MIB — предложение ACCESS</span><span class="sxs-lookup"><span data-stu-id="70fbc-118">MIB-ACCESS clause</span></span>     | <span data-ttu-id="70fbc-119">Квалификатор CIM</span><span class="sxs-lookup"><span data-stu-id="70fbc-119">CIM qualifier</span></span>       |
|-----------------------|---------------------|
| <span data-ttu-id="70fbc-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70fbc-120">read-only</span></span>             | <span data-ttu-id="70fbc-121">**Чтение**</span><span class="sxs-lookup"><span data-stu-id="70fbc-121">**Read**</span></span>            |
| <span data-ttu-id="70fbc-122">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="70fbc-122">read-write</span></span>            | <span data-ttu-id="70fbc-123">**Чтение**, **запись**</span><span class="sxs-lookup"><span data-stu-id="70fbc-123">**Read**, **Write**</span></span> |
| <span data-ttu-id="70fbc-124">для чтения и создания</span><span class="sxs-lookup"><span data-stu-id="70fbc-124">read-create</span></span>           | <span data-ttu-id="70fbc-125">**Чтение**</span><span class="sxs-lookup"><span data-stu-id="70fbc-125">**Read**</span></span>            |
| <span data-ttu-id="70fbc-126">доступный — для — уведомление</span><span class="sxs-lookup"><span data-stu-id="70fbc-126">accessible-for-notify</span></span> | <span data-ttu-id="70fbc-127">**\_Недоступно**</span><span class="sxs-lookup"><span data-stu-id="70fbc-127">**Not\_Accessible**</span></span> |
| <span data-ttu-id="70fbc-128">недоступно</span><span class="sxs-lookup"><span data-stu-id="70fbc-128">not-accessible</span></span>        | <span data-ttu-id="70fbc-129">**\_Недоступно**</span><span class="sxs-lookup"><span data-stu-id="70fbc-129">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="70fbc-130">Если объект MIB сопоставлен недоступному и не является свойством с ключом класса, сопоставление самого объекта MIB отсутствует.</span><span class="sxs-lookup"><span data-stu-id="70fbc-130">When a MIB object maps to not-accessible and is not a keyed property of the class, there is no mapping of the MIB object itself.</span></span>

 

 



