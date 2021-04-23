---
title: Назначение идентификаторов запросов
description: WinSNMP-приложение может вызвать функцию Снмпкреатепду или функцию Снмпсетпдудата для назначения идентификаторов запросов, генерируемых приложением, в PDU. Приложение должно передать значение в \_ параметре идентификатора запроса.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772854"
---
# <a name="assigning-request-identifiers"></a><span data-ttu-id="cb0fb-104">Назначение идентификаторов запросов</span><span class="sxs-lookup"><span data-stu-id="cb0fb-104">Assigning Request Identifiers</span></span>

<span data-ttu-id="cb0fb-105">WinSNMP-приложение может вызвать функцию [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) или функцию [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) для назначения идентификаторов запросов, генерируемых приложением, в PDU.</span><span class="sxs-lookup"><span data-stu-id="cb0fb-105">A WinSNMP application can call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function to assign an application-generated request identifier to a PDU.</span></span> <span data-ttu-id="cb0fb-106">Приложение должно передать значение в параметре *\_ идентификатора запроса* .</span><span class="sxs-lookup"><span data-stu-id="cb0fb-106">The application must pass the value in the *request\_id* parameter.</span></span>

<span data-ttu-id="cb0fb-107">Приложение может запросить, чтобы реализация Microsoft WinSNMP создавала и назначила идентификатор запроса PDU, передав нуль в параметре *\_ идентификатора запроса* функции [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) .</span><span class="sxs-lookup"><span data-stu-id="cb0fb-107">An application can request that the Microsoft WinSNMP implementation generate and assign a request identifier to a PDU by passing zero in the *request\_id* parameter of the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="cb0fb-108">Приложение может получить назначенный идентификатор запроса с помощью вызова функции [**снмпжетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="cb0fb-108">The application can retrieve the assigned request identifier with a call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function.</span></span>

<span data-ttu-id="cb0fb-109">Чтобы назначить идентификатор запроса, равный определенному значению, включая ноль, приложение должно передать это значение в параметре *\_ идентификатора запроса* функции [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="cb0fb-109">To assign a request identifier equal to a specific value, including zero, the application must pass that value in the *request\_id* parameter of the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span>

<span data-ttu-id="cb0fb-110">Когда реализация выполняет политику повторной передачи приложения, она включает в себя поле **\_ идентификатор запроса** исходного PDU в каждом переданном сообщении SNMP.</span><span class="sxs-lookup"><span data-stu-id="cb0fb-110">When the implementation executes the application's retransmission policy, it includes the **request\_id** field of the original PDU in each retransmitted SNMP message.</span></span> <span data-ttu-id="cb0fb-111">Дополнительные сведения см. в статье о повторной [передаче](about-retransmission.md) и [управлении политикой](managing-the-retransmission-policy.md)повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="cb0fb-111">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

> [!Note]  
> <span data-ttu-id="cb0fb-112">Когда реализация получает ловушки от сущности в стандарте, она присваивает ненулевое значение полю **\_ идентификатора запроса** PDU.</span><span class="sxs-lookup"><span data-stu-id="cb0fb-112">When the implementation receives traps from an SNMPv1 entity, it assigns a non-zero value to the **request\_id** field of the PDU.</span></span> <span data-ttu-id="cb0fb-113">Это значение может дублировать идентификатор запроса, используемый приложением в PDU запроса.</span><span class="sxs-lookup"><span data-stu-id="cb0fb-113">This value may duplicate a request identifier used by the application in a request PDU.</span></span> <span data-ttu-id="cb0fb-114">Приложения должны проверять наличие дублирования.</span><span class="sxs-lookup"><span data-stu-id="cb0fb-114">Applications must check for duplication.</span></span>

 

 

 




