---
title: О реализации Microsoft WinSNMP
description: Реализация Microsoft WinSNMP соответствует WinSNMP версии 2,0.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986069"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a><span data-ttu-id="c1e1b-103">О реализации Microsoft WinSNMP</span><span class="sxs-lookup"><span data-stu-id="c1e1b-103">About the Microsoft WinSNMP Implementation</span></span>

<span data-ttu-id="c1e1b-104">Реализация Microsoft WinSNMP соответствует WinSNMP версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="c1e1b-104">The Microsoft WinSNMP implementation complies with WinSNMP version 2.0.</span></span> <span data-ttu-id="c1e1b-105">Он поддерживает все функции и операции, определенные как в спецификации WinSNMP версии 1.1, так и в дополнение к WinSNMP версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="c1e1b-105">It supports all the functions and operations defined in both the WinSNMP version 1.1a specification and the WinSNMP version 2.0 Addendum.</span></span> <span data-ttu-id="c1e1b-106">Реализация предоставляет следующие службы для WinSNMP Applications:</span><span class="sxs-lookup"><span data-stu-id="c1e1b-106">The implementation provides the following services for WinSNMP applications:</span></span>

-   <span data-ttu-id="c1e1b-107">Управляет обменом данными с сущностями управления и обратно.</span><span class="sxs-lookup"><span data-stu-id="c1e1b-107">Manages communications to and from management entities.</span></span> <span data-ttu-id="c1e1b-108">Сущность может находиться на локальном компьютере или быть подключена через локальную или глобальную сеть или через Интернет.</span><span class="sxs-lookup"><span data-stu-id="c1e1b-108">The entity can reside on the local computer or be connected through a local or wide-area network, or the Internet.</span></span> <span data-ttu-id="c1e1b-109">Дополнительные сведения см. в разделе [уровни поддержки SNMP](levels-of-snmp-support.md).</span><span class="sxs-lookup"><span data-stu-id="c1e1b-109">For more information, see [Levels of SNMP Support](levels-of-snmp-support.md).</span></span>
-   <span data-ttu-id="c1e1b-110">Скрывает сведения о протоколе SNMP, нотации абстрактного синтаксиса (ASN. 1) и основных правилах кодирования (ЛИЧЕСТВО) для описания синтаксиса перемещения.</span><span class="sxs-lookup"><span data-stu-id="c1e1b-110">Hides the details of SNMP protocol, Abstract Syntax Notation One (ASN.1), and the Basic Encoding Rules (BER) for describing transfer syntax.</span></span>
-   <span data-ttu-id="c1e1b-111">Проверяет правильность PDU и отклоняет недопустимые устройства PDU.</span><span class="sxs-lookup"><span data-stu-id="c1e1b-111">Verifies the correctness of PDUs and rejects invalid PDUs.</span></span> <span data-ttu-id="c1e1b-112">Дополнительные сведения см. в разделе [Работа с единицами данных протокола](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="c1e1b-112">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>
-   <span data-ttu-id="c1e1b-113">Преобразует типы PDU SNMPv2C при необходимости в соответствии с соответствующими RFC.</span><span class="sxs-lookup"><span data-stu-id="c1e1b-113">Transforms SNMPv2C PDU types when necessary in accordance with the relevant RFCs.</span></span>
-   <span data-ttu-id="c1e1b-114">Преобразует ловушки стандарта SNMPv2C в соответствии с RFC 1908, "сосуществование между версией 1 и версией 2 стандартной инфраструктуры управления сетью".</span><span class="sxs-lookup"><span data-stu-id="c1e1b-114">Converts SNMPv1 traps from an SNMPv1 agent to SNMPv2C traps in accordance with RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework."</span></span> <span data-ttu-id="c1e1b-115">Дополнительные сведения см. [в статье преобразование ловушек из SNMPv2c в](translating-traps-from-snmpv1-to-snmpv2c.md).</span><span class="sxs-lookup"><span data-stu-id="c1e1b-115">For more information, see [Translating Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).</span></span>
-   <span data-ttu-id="c1e1b-116">Поддерживает политику повторной передачи приложения и обеспечивает поддержку выполнения повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="c1e1b-116">Supports the application's retransmission policy and provides retransmission execution support.</span></span> <span data-ttu-id="c1e1b-117">Дополнительные сведения см. [в разделе базы данных WinSNMP](the-winsnmp-database.md) и о повторной [передаче](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="c1e1b-117">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [About Retransmission](about-retransmission.md).</span></span>
-   <span data-ttu-id="c1e1b-118">Обеспечивает поддержку перевода сущностей и контекста для приложения.</span><span class="sxs-lookup"><span data-stu-id="c1e1b-118">Provides entity and context translation support for the application.</span></span> <span data-ttu-id="c1e1b-119">Дополнительные сведения см. в статьях [базы данных WinSNMP](the-winsnmp-database.md) и [Настройка режима преобразования сущностей и контекста](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="c1e1b-119">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

<span data-ttu-id="c1e1b-120">Дополнительные сведения о связи между приложением WinSNMP и реализацией см. в разделе [понятия winsnmp управление данными концепций](winsnmp-data-management-concepts.md) и [WinSNMP Sessions](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="c1e1b-120">For additional information about the relationship between a WinSNMP application and the implementation, see [WinSNMP Data Management Concepts](winsnmp-data-management-concepts.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




