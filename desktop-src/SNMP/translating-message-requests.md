---
title: Преобразование запросов сообщений
description: В этом разделе описывается процесс перевода запросов в неуправляемый статус в запросы SNMPv2.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2a67ecb78b16f818ea50158faf827e19d4eba5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531964"
---
# <a name="translating-message-requests"></a><span data-ttu-id="4b616-103">Преобразование запросов сообщений</span><span class="sxs-lookup"><span data-stu-id="4b616-103">Translating Message Requests</span></span>

<span data-ttu-id="4b616-104">В этом разделе описывается процесс перевода запросов в неуправляемый статус в запросы SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="4b616-104">This topic describes the process of translating SNMPv1 requests into SNMPv2 requests.</span></span>

<span data-ttu-id="4b616-105">Если приложение WinSNMP запрашивает функции, доступные в инфраструктуре SNMP версии 2C (SNMPv2C), но целевая сущность поддерживает только платформу SNMP версии 1, реализация Microsoft WinSNMP пытается перевести запрос в формат CLR.</span><span class="sxs-lookup"><span data-stu-id="4b616-105">If a WinSNMP application requests functionality that is available under the SNMP version 2C framework (SNMPv2C), but the target entity supports only the SNMP version 1 framework (SNMPv1), the Microsoft WinSNMP implementation attempts to translate the request to the SNMPv1 format.</span></span> <span data-ttu-id="4b616-106">Для этого в реализации используются процедуры, определенные в документе RFC 1908 "сосуществование между версией 1 и версией 2 Internet-Standard инфраструктуры управления сетью".</span><span class="sxs-lookup"><span data-stu-id="4b616-106">To do this, the implementation uses the procedures defined in RFC 1908, "Coexistence Between Version 1 and Version 2 of the Internet-Standard Network Management Framework."</span></span> <span data-ttu-id="4b616-107">Если перевод невозможен, функция [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) завершается ошибкой, если операция снмпапи кода расширенной ошибки \_ \_ недопустима.</span><span class="sxs-lookup"><span data-stu-id="4b616-107">If translation is not possible, the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function fails with the extended error code SNMPAPI\_OPERATION\_INVALID.</span></span>

 

 




