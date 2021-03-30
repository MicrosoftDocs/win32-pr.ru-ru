---
title: Отправка SNMP-сообщений
description: Ошибка WinSNMP-приложения инициирует запрос на передачу, отправляя сообщение SNMP. SNMP-сообщения включают в себя единицу данных протокола SNMP. Дополнительные сведения см. в разделе Работа с единицами данных протокола.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331347"
---
# <a name="sending-snmp-messages"></a><span data-ttu-id="4357e-105">Отправка SNMP-сообщений</span><span class="sxs-lookup"><span data-stu-id="4357e-105">Sending SNMP Messages</span></span>

<span data-ttu-id="4357e-106">Ошибка WinSNMP-приложения инициирует запрос на передачу, отправляя сообщение SNMP.</span><span class="sxs-lookup"><span data-stu-id="4357e-106">A WinSNMP application initiates a transmission request by sending an SNMP message.</span></span> <span data-ttu-id="4357e-107">SNMP-сообщения включают в себя единицу данных протокола SNMP.</span><span class="sxs-lookup"><span data-stu-id="4357e-107">SNMP messages include an SNMP protocol data unit.</span></span> <span data-ttu-id="4357e-108">Дополнительные сведения см. в разделе [Работа с единицами данных протокола](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="4357e-108">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

<span data-ttu-id="4357e-109">Приложение WinSNMP должно вызывать функцию [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) , чтобы запросить передачу PDU с помощью реализации Microsoft WinSNMP с другими необходимыми элементами сообщения, определенными соответствующим документом RFC.</span><span class="sxs-lookup"><span data-stu-id="4357e-109">A WinSNMP application must call the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit the PDU, with the other required message elements defined by the relevant RFC.</span></span> <span data-ttu-id="4357e-110">В дополнение к целевой сущности, приложение должно указать исходную сущность и контекст для запроса.</span><span class="sxs-lookup"><span data-stu-id="4357e-110">In addition to the destination entity, the application must specify the source entity and a context for the request.</span></span> <span data-ttu-id="4357e-111">Функция [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="4357e-111">The [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function executes asynchronously.</span></span>

<span data-ttu-id="4357e-112">Для получения ответа на запрос **снмпсендмсг** в приложении WinSNMP необходимо вызвать функцию [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="4357e-112">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an **SnmpSendMsg** request.</span></span>

<span data-ttu-id="4357e-113">Реализация проверяет допустимость PDU и других элементов сообщения, когда приложение вызывает [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span><span class="sxs-lookup"><span data-stu-id="4357e-113">The implementation verifies the validity of the PDU and the other message elements when an application calls [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span>

 

 




