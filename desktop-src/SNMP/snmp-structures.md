---
title: Структуры SNMP
description: В следующей таблице перечислены структуры, используемые с SNMP.
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP структуры SNMP
- Структуры SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254dfebeb3d468add8871d4b6f28f268341e9ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413536"
---
# <a name="snmp-structures"></a><span data-ttu-id="38442-105">Структуры SNMP</span><span class="sxs-lookup"><span data-stu-id="38442-105">SNMP Structures</span></span>

<span data-ttu-id="38442-106">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="38442-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="38442-107">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="38442-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="38442-108">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="38442-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="38442-109">В следующей таблице перечислены структуры, используемые с SNMP.</span><span class="sxs-lookup"><span data-stu-id="38442-109">The following table lists structures that are used with SNMP.</span></span>



| <span data-ttu-id="38442-110">Структура SNMP</span><span class="sxs-lookup"><span data-stu-id="38442-110">SNMP Structure</span></span>                                         | <span data-ttu-id="38442-111">Описание</span><span class="sxs-lookup"><span data-stu-id="38442-111">Description</span></span>                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38442-112">**аснани**</span><span class="sxs-lookup"><span data-stu-id="38442-112">**AsnAny**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | <span data-ttu-id="38442-113">Описывает тип и значение указанной переменной SNMP.</span><span class="sxs-lookup"><span data-stu-id="38442-113">Describes the type and value of a specified SNMP variable.</span></span>                                              |
| <span data-ttu-id="38442-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38442-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span></span>               | <span data-ttu-id="38442-115">Содержит 64-разрядный счетчик, заданный двумя значениями, описывающими его младшие и старшие разряды.</span><span class="sxs-lookup"><span data-stu-id="38442-115">Contains a 64-bit counter that is specified by two values describing its low-order and high-order bits.</span></span> |
| [<span data-ttu-id="38442-116">**аснобжектидентифиер**</span><span class="sxs-lookup"><span data-stu-id="38442-116">**AsnObjectIdentifier**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | <span data-ttu-id="38442-117">Описывает идентификатор объекта (OID).</span><span class="sxs-lookup"><span data-stu-id="38442-117">Describes an object identifier (OID).</span></span>                                                                   |
| [<span data-ttu-id="38442-118">**асноктетстринг**</span><span class="sxs-lookup"><span data-stu-id="38442-118">**AsnOctetString**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | <span data-ttu-id="38442-119">Представляет строку октетов, обычно в байтовых значениях.</span><span class="sxs-lookup"><span data-stu-id="38442-119">Represents a string of octets, usually in byte values.</span></span>                                                  |
| [<span data-ttu-id="38442-120">**снмпварбинд**</span><span class="sxs-lookup"><span data-stu-id="38442-120">**SnmpVarBind**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | <span data-ttu-id="38442-121">Описывает привязку переменной SNMP.</span><span class="sxs-lookup"><span data-stu-id="38442-121">Describes an SNMP variable binding.</span></span>                                                                     |
| [<span data-ttu-id="38442-122">**снмпварбиндлист**</span><span class="sxs-lookup"><span data-stu-id="38442-122">**SnmpVarBindList**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | <span data-ttu-id="38442-123">Содержит список привязок к переменным SNMP.</span><span class="sxs-lookup"><span data-stu-id="38442-123">Contains a list of SNMP variable bindings.</span></span>                                                              |



 

 

 