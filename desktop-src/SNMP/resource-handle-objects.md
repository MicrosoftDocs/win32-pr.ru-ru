---
title: Объекты «обработчик ресурсов»
description: Структура объекта ресурса ограничена реализацией Microsoft WinSNMP. Приложение WinSNMP может обращаться к объекту ресурса с помощью маркера.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778596"
---
# <a name="resource-handle-objects"></a><span data-ttu-id="579f6-104">Объекты «обработчик ресурсов»</span><span class="sxs-lookup"><span data-stu-id="579f6-104">Resource Handle Objects</span></span>

<span data-ttu-id="579f6-105">Структура объекта ресурса ограничена реализацией Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="579f6-105">The structure of a resource object is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="579f6-106">Приложение WinSNMP может обращаться к объекту ресурса с помощью маркера.</span><span class="sxs-lookup"><span data-stu-id="579f6-106">A WinSNMP application can access a resource object with a handle.</span></span>

<span data-ttu-id="579f6-107">Реализация может выделить один из следующих типов дескрипторов ресурсов для приложения WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="579f6-107">The implementation can allocate one of the following types of resource handles for a WinSNMP application.</span></span>

| <span data-ttu-id="579f6-108">Тип обработчика</span><span class="sxs-lookup"><span data-stu-id="579f6-108">Handle type</span></span>        | <span data-ttu-id="579f6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="579f6-109">Description</span></span>                       |
|--------------------|-----------------------------------|
| <span data-ttu-id="579f6-110">**\_сеанс хснмп**</span><span class="sxs-lookup"><span data-stu-id="579f6-110">**HSNMP\_SESSION**</span></span> | <span data-ttu-id="579f6-111">Обработчик для сеанса WinSNMP</span><span class="sxs-lookup"><span data-stu-id="579f6-111">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="579f6-112">**\_сущность хснмп**</span><span class="sxs-lookup"><span data-stu-id="579f6-112">**HSNMP\_ENTITY**</span></span>  | <span data-ttu-id="579f6-113">Обработчик для объекта SNMP</span><span class="sxs-lookup"><span data-stu-id="579f6-113">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="579f6-114">**\_контекст хснмп**</span><span class="sxs-lookup"><span data-stu-id="579f6-114">**HSNMP\_CONTEXT**</span></span> | <span data-ttu-id="579f6-115">Обработку контекста WinSNMP</span><span class="sxs-lookup"><span data-stu-id="579f6-115">Handle to a WinSNMP context</span></span>       |
| <span data-ttu-id="579f6-116">**ХСНМП \_ PDU**</span><span class="sxs-lookup"><span data-stu-id="579f6-116">**HSNMP\_PDU**</span></span>     | <span data-ttu-id="579f6-117">Обработчик для единицы данных протокола</span><span class="sxs-lookup"><span data-stu-id="579f6-117">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="579f6-118">**ХСНМП \_ вбл**</span><span class="sxs-lookup"><span data-stu-id="579f6-118">**HSNMP\_VBL**</span></span>     | <span data-ttu-id="579f6-119">Handle в список привязок переменных</span><span class="sxs-lookup"><span data-stu-id="579f6-119">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="579f6-120">WinSNMP-приложение может запрашивать, что реализация создает или удаляет дескрипторы ресурсов, но реализация выполняет операцию.</span><span class="sxs-lookup"><span data-stu-id="579f6-120">A WinSNMP application can request that the implementation create or delete resource handles, but the implementation performs the operation.</span></span> <span data-ttu-id="579f6-121">Дополнительные сведения об освобождении отдельных ресурсов см. в статье [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**снмпфривбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**снмпфриентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)и [**снмпфриконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .</span><span class="sxs-lookup"><span data-stu-id="579f6-121">For additional information about freeing individual resources, see the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), and [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) functions.</span></span>

 

 




