---
title: Получение сообщений SNMP
description: Для получения ответа на запрос Снмпсендмсг в приложении WinSNMP необходимо вызвать функцию Снмпреквмсг.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529420deaf637cec8598a8e8becc87ab514b40b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778599"
---
# <a name="receiving-snmp-messages"></a><span data-ttu-id="e1928-103">Получение сообщений SNMP</span><span class="sxs-lookup"><span data-stu-id="e1928-103">Receiving SNMP Messages</span></span>

<span data-ttu-id="e1928-104">Для получения ответа на запрос [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) в приложении WinSNMP необходимо вызвать функцию [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="e1928-104">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) request.</span></span>

<span data-ttu-id="e1928-105">Функция [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) передает в реализацию Microsoft WinSNMP маркер окна приложения и идентификатор сообщения уведомления.</span><span class="sxs-lookup"><span data-stu-id="e1928-105">The [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function passes an application window handle and a notification message identifier to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="e1928-106">Когда окно приложения получает это сообщение, оно сообщает приложению о необходимости вызова функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) с помощью обработчика сеанса, возвращенного [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span><span class="sxs-lookup"><span data-stu-id="e1928-106">When the application window receives this message, it signals the application to call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function using the session handle returned by [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span>

<span data-ttu-id="e1928-107">Функция [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) возвращает два дескриптора сущности, дескриптор контекста и дескриптор PDU.</span><span class="sxs-lookup"><span data-stu-id="e1928-107">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function returns two entity handles, a context handle, and the handle to a PDU.</span></span> <span data-ttu-id="e1928-108">Рекомендуется освобождать приложение WinSNMP с помощью функций [**снмпфриентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**снмпфриконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)и [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .</span><span class="sxs-lookup"><span data-stu-id="e1928-108">It is recommended that the WinSNMP application free these resources using the [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) functions.</span></span>

<span data-ttu-id="e1928-109">Дополнительные сведения об управлении временем между вызовом функции [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) и получением соответствующего ответа см. в разделе о повторной [передаче](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="e1928-109">For additional information about managing the time between a call to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function and the receipt of the corresponding response, see [About Retransmission](about-retransmission.md).</span></span> <span data-ttu-id="e1928-110">Дополнительные сведения об использовании поля " **\_ идентификатор запроса** " PDU для сопоставления PDU ответа с соответствующим PDU запроса см. в разделе [сопоставление PDU и запросов распределения питания](matching-response-and-request-pdus.md).</span><span class="sxs-lookup"><span data-stu-id="e1928-110">For additional information about using the **request\_id** PDU field to match a response PDU with its request PDU, see [Matching Response and Request PDUs](matching-response-and-request-pdus.md).</span></span>

 

 




