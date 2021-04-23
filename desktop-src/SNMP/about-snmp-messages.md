---
title: Сообщения SNMP
description: Протокол простого сетевого управления использует сообщения для обмена данными между удаленными сущностями SNMP и обмена ими.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410756"
---
# <a name="about-snmp-messages"></a><span data-ttu-id="1fe87-103">Сообщения SNMP</span><span class="sxs-lookup"><span data-stu-id="1fe87-103">About SNMP Messages</span></span>

<span data-ttu-id="1fe87-104">Протокол простого сетевого управления использует сообщения для обмена данными между удаленными сущностями SNMP и обмена ими.</span><span class="sxs-lookup"><span data-stu-id="1fe87-104">The Simple Network Management Protocol uses messages to communicate and exchange information between remote SNMP entities.</span></span> <span data-ttu-id="1fe87-105">SNMP-сообщения содержат единицы данных протокола (PDU) и дополнительные элементы заголовка сообщения, определенные соответствующим RFC.</span><span class="sxs-lookup"><span data-stu-id="1fe87-105">SNMP messages contain protocol data units (PDUs) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="1fe87-106">PDU — это пакет данных, содержащий компоненты данных SNMP (или поля).</span><span class="sxs-lookup"><span data-stu-id="1fe87-106">A PDU is a data packet that contains SNMP data components (or fields).</span></span>

<span data-ttu-id="1fe87-107">Формат SNMP-сообщения одинаков для версий с SNMPv2C и выше.</span><span class="sxs-lookup"><span data-stu-id="1fe87-107">The format of an SNMP message is the same for both SNMPv1 and SNMPv2C.</span></span> <span data-ttu-id="1fe87-108">Однако SNMPv2C поддерживает дополнительные типы PDU.</span><span class="sxs-lookup"><span data-stu-id="1fe87-108">However, SNMPv2C supports additional PDU types.</span></span> <span data-ttu-id="1fe87-109">Например, он поддерживает тип запроса [ \_ распределения PDU \_ SNMP](snmp-variable-types-and-request-pdu-types.md) , который позволяет приложению эффективно получать большие блоки данных из целевых сущностей.</span><span class="sxs-lookup"><span data-stu-id="1fe87-109">For example, it supports the [SNMP\_PDU\_GETBULK](snmp-variable-types-and-request-pdu-types.md) request type, which enables an application to efficiently retrieve large blocks of data from target entities.</span></span>

 

 




