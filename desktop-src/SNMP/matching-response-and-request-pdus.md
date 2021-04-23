---
title: Сопоставление устройств распределения питания и запросов
description: Порядок, в котором WinSNMP-приложение получает SNMP-ответы, может не соответствовать порядку, в котором приложение отправляет запросы операции SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986653"
---
# <a name="matching-response-and-request-pdus"></a><span data-ttu-id="78781-103">Сопоставление устройств распределения питания и запросов</span><span class="sxs-lookup"><span data-stu-id="78781-103">Matching Response and Request PDUs</span></span>

<span data-ttu-id="78781-104">Порядок, в котором WinSNMP-приложение получает SNMP-ответы, может не соответствовать порядку, в котором приложение отправляет запросы операции SNMP.</span><span class="sxs-lookup"><span data-stu-id="78781-104">The order in which the WinSNMP application receives SNMP responses may not match the order in which the application submits SNMP operation requests.</span></span> <span data-ttu-id="78781-105">Чтобы сопоставить ответ с запросом, приложение должно использовать поле идентификатора запроса ( **\_ идентификатор запроса**) ответа.</span><span class="sxs-lookup"><span data-stu-id="78781-105">To match the response with the request, the application must use the request identifier field (the **request\_id**) of the response.</span></span>

<span data-ttu-id="78781-106">Поле **\_ идентификатора запроса** — это уникальное числовое значение, идентифицирующее PDU.</span><span class="sxs-lookup"><span data-stu-id="78781-106">The **request\_id** field is a unique numeric value that identifies the PDU.</span></span> <span data-ttu-id="78781-107">Приложения могут назначать идентификаторы запросов путем вызова функции [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) или функции [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="78781-107">Applications can assign request identifiers by calling the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span> <span data-ttu-id="78781-108">Вызовите функцию [**снмпжетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) , чтобы получить **\_ идентификатор запроса** PDU.</span><span class="sxs-lookup"><span data-stu-id="78781-108">Call the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function to retrieve a PDU's **request\_id**.</span></span>

 

 




