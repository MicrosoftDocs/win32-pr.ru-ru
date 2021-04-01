---
title: Регистрация приложения агента SNMP
description: Помимо операций диспетчера SNMP, API-интерфейс WinSNMP версии 2,0 также поддерживает операции агента SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986651"
---
# <a name="registering-an-snmp-agent-application"></a><span data-ttu-id="7f8e1-103">Регистрация приложения агента SNMP</span><span class="sxs-lookup"><span data-stu-id="7f8e1-103">Registering an SNMP Agent Application</span></span>

<span data-ttu-id="7f8e1-104">Помимо операций диспетчера SNMP, API-интерфейс WinSNMP версии 2,0 также поддерживает операции агента SNMP.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-104">In addition to SNMP manager operations, the WinSNMP API version 2.0 also supports SNMP agent operations.</span></span>

<span data-ttu-id="7f8e1-105">Чтобы зарегистрировать приложение WinSNMP в качестве агента SNMP, приложение может вызвать функцию [**снмплистен**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) .</span><span class="sxs-lookup"><span data-stu-id="7f8e1-105">To register a WinSNMP application as an SNMP agent, the application can call the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function.</span></span> <span data-ttu-id="7f8e1-106">Эта функция информирует реализацию Microsoft WinSNMP о том, что сущность SNMP будет действовать в роли агента SNMP.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-106">This function informs the Microsoft WinSNMP implementation that an SNMP entity will be acting in the role of an SNMP agent.</span></span> <span data-ttu-id="7f8e1-107">Приложение также может вызвать **снмплистен** , чтобы сообщить о реализации, когда она больше не будет действовать как агент.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-107">The application can also call **SnmpListen** to inform the implementation when it will no longer be acting as an agent.</span></span>

<span data-ttu-id="7f8e1-108">Если приложение вызывает функцию [**снмплистен**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) и передает значение снмпапи \_ On в параметре *лстатус* , выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-108">If an application calls the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function and passes the value SNMPAPI\_ON in the *lStatus* parameter, the following actions occur:</span></span>

1.  <span data-ttu-id="7f8e1-109">Сущность, которая будет работать в роли агента SNMP, привязывается к назначенному ему порту и прослушивает входящие запросы SNMP-сообщений.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-109">The entity that will be functioning in an SNMP agent role binds to its assigned port, and "listens" for incoming SNMP message requests.</span></span>
2.  <span data-ttu-id="7f8e1-110">Агент использует логику конкретного приложения для обработки каждого SNMP-запроса.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-110">The agent uses application-specific logic to process each SNMP request.</span></span>
3.  <span data-ttu-id="7f8e1-111">Агент формирует соответствующие ответы на каждый запрос.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-111">The agent forms appropriate responses to each request.</span></span>
4.  <span data-ttu-id="7f8e1-112">Агент передает ответ запрашивающей сущности, вызывая функцию [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="7f8e1-112">The agent transmits the response to the requesting entity by calling the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span> <span data-ttu-id="7f8e1-113">Когда агент вызывает **снмпсендмсг**, он задает адрес агента в параметре *срцентити* и адрес сущности удаленного диспетчера в параметре *дстентити* .</span><span class="sxs-lookup"><span data-stu-id="7f8e1-113">When the agent calls **SnmpSendMsg**, it specifies the address of the agent in the *srcEntity* parameter, and the address of the remote manager entity in the *dstEntity* parameter.</span></span> <span data-ttu-id="7f8e1-114">(Эти значения являются обратными значениями сущности агента, полученной в этих параметрах при вызове функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) для получения SNMP-запроса.)</span><span class="sxs-lookup"><span data-stu-id="7f8e1-114">(These values are the reverse of the values the agent entity received in these parameters when it called the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve an SNMP request.)</span></span>

<span data-ttu-id="7f8e1-115">Дополнительные сведения о приложениях и агентах управления SNMP см. в разделе [About SNMP](about-snmp.md).</span><span class="sxs-lookup"><span data-stu-id="7f8e1-115">For more information about SNMP management applications and agent applications, see [About SNMP](about-snmp.md).</span></span>

 

 




