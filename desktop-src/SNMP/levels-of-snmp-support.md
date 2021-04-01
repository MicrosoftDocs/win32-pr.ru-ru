---
title: Уровни поддержки SNMP
description: Реализация Microsoft WinSNMP обеспечивает поддержку SNMP-связи уровня 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132867"
---
# <a name="levels-of-snmp-support"></a><span data-ttu-id="af0f3-103">Уровни поддержки SNMP</span><span class="sxs-lookup"><span data-stu-id="af0f3-103">Levels of SNMP Support</span></span>

<span data-ttu-id="af0f3-104">Реализация Microsoft WinSNMP обеспечивает поддержку SNMP-связи уровня 2.</span><span class="sxs-lookup"><span data-stu-id="af0f3-104">The Microsoft WinSNMP implementation provides level 2 SNMP communications support.</span></span> <span data-ttu-id="af0f3-105">Уровень 2 поддерживает стандартный протокол SNMPv2, определенный в RFC 1902-1908.</span><span class="sxs-lookup"><span data-stu-id="af0f3-105">Level 2 supports the Internet Engineering Task Force (IETF) standard SNMPv2 protocol as defined in RFCs 1902-1908.</span></span> <span data-ttu-id="af0f3-106">Она также поддерживает оболочку сообщений на основе сообщества, как определено в RFC 1901 (SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="af0f3-106">It also supports the community-based message wrapper as defined in RFC 1901 (SNMPv2C).</span></span>

<span data-ttu-id="af0f3-107">Поддержка связи уровня 2 включает в себя кодирование сообщений и службы декодирования, ранее именуемые поддержкой связи уровня 0 в WinSNMP версии 1.1 a.</span><span class="sxs-lookup"><span data-stu-id="af0f3-107">Level 2 communications support includes message encoding and decoding services, previously called Level 0 communications support in WinSNMP version 1.1a.</span></span> <span data-ttu-id="af0f3-108">Уровень 2 также поддерживает все операции протокола в версиях, которые ранее назывались поддержкой связи уровня 1 в WinSNMP версии 1.1 a.</span><span class="sxs-lookup"><span data-stu-id="af0f3-108">Level 2 also supports all SNMPv1 protocol operations, previously called Level 1 communications support in WinSNMP version 1.1a.</span></span>

<span data-ttu-id="af0f3-109">Реализация Возвращает максимальный уровень SNMP-взаимодействия, который она поддерживает, в ответ на вызов функции WinSNMP приложением в функцию [**снмпстартуп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) .</span><span class="sxs-lookup"><span data-stu-id="af0f3-109">The implementation returns the maximum level of SNMP communications it supports in response to a call by the WinSNMP application to the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function.</span></span>

<span data-ttu-id="af0f3-110">Если приложение WinSNMP использует реализацию для кодирования сообщений SNMP и только для декодирования, приложение должно выполнить необходимые преобразования, которые будут выполнены в реализации.</span><span class="sxs-lookup"><span data-stu-id="af0f3-110">If the WinSNMP application uses the implementation for SNMP message encoding and decoding only, the application must perform required transformations that the implementation would have performed.</span></span> <span data-ttu-id="af0f3-111">Это включает преобразование ловушек в неограниченном числе, возвращенных вызовом функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) для SNMPv2c ловушек.</span><span class="sxs-lookup"><span data-stu-id="af0f3-111">This includes translating SNMPv1 traps returned by a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function, to SNMPv2C traps.</span></span> <span data-ttu-id="af0f3-112">Он также включает преобразование типов PDU, определенных в стандарте, в соответствующий тип PDU, определенный в SNMPv2C, в соответствии с RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="af0f3-112">It also includes translating PDU types defined by SNMPv1 to the relevant PDU type defined by SNMPv2C, in accordance with RFC 1908.</span></span>

 

 




