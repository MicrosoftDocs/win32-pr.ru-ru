---
title: О повторной передаче
description: WinSNMP-приложение может выполнять запросы операций SNMP различными способами.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a26ba632cec096300927911c2277cbcf5911e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329115"
---
# <a name="about-retransmission"></a><span data-ttu-id="8d62c-103">О повторной передаче</span><span class="sxs-lookup"><span data-stu-id="8d62c-103">About Retransmission</span></span>

<span data-ttu-id="8d62c-104">WinSNMP-приложение может выполнять запросы операций SNMP различными способами.</span><span class="sxs-lookup"><span data-stu-id="8d62c-104">A WinSNMP application can make SNMP operation requests in various ways.</span></span> <span data-ttu-id="8d62c-105">Приложение может выдавать несколько запросов агенту SNMP, не дожидаясь ответа, или выдавать один запрос и ожидать ответа.</span><span class="sxs-lookup"><span data-stu-id="8d62c-105">The application can issue several requests to an SNMP agent, without waiting for a response, or it can issue a single request and wait for the response.</span></span> <span data-ttu-id="8d62c-106">Так как протокол SNMP может быть реализован на нескольких транспортных протоколах, механизмы доставки и характеристики надежности могут различаться.</span><span class="sxs-lookup"><span data-stu-id="8d62c-106">Since SNMP can be implemented on multiple transport protocols, delivery mechanisms and reliability characteristics can vary.</span></span>

<span data-ttu-id="8d62c-107">При создании кода для приложения WinSNMP необходимо определить уровень надежности, необходимый для операций связи, в зависимости от способа, которым приложение выдает запросы операций.</span><span class="sxs-lookup"><span data-stu-id="8d62c-107">When you code the WinSNMP application you must determine the level of reliability you need for communications operations, based on the way the application issues operation requests.</span></span> <span data-ttu-id="8d62c-108">Затем необходимо выбрать стратегию повторной передачи и реализовать политику повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="8d62c-108">Then you must select a retransmission strategy and implement a retransmission policy.</span></span>

<span data-ttu-id="8d62c-109">Политика повторной передачи содержит период времени ожидания и число повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="8d62c-109">A retransmission policy includes a time-out period and a retry count.</span></span> <span data-ttu-id="8d62c-110">Время ожидания — это затраченное время в сотых долях секунды между выдачей [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) запроса приложения и его получением соответствующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="8d62c-110">A time-out period is the elapsed time, in hundredths of a second, between an application's issuance of an [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) request and its receipt of the corresponding message.</span></span> <span data-ttu-id="8d62c-111">Приложение получает сообщение в результате вызова функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="8d62c-111">The application receives the message as a result of a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function.</span></span> <span data-ttu-id="8d62c-112">Значение времени ожидания — это период времени, в течение которого реализация Microsoft WinSNMP ожидает ответа сущности на запрос на соединение.</span><span class="sxs-lookup"><span data-stu-id="8d62c-112">The time-out value is the period of time the Microsoft WinSNMP implementation waits for an entity to respond to a communication request.</span></span> <span data-ttu-id="8d62c-113">Если в течение времени ожидания нет ответа, реализация повторно передает запрос, если значение счетчика повторных попыток указывает на попытки повторной передачи или не вызывает [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span><span class="sxs-lookup"><span data-stu-id="8d62c-113">If there is no response within the time-out period, the implementation either retransmits the request if the retry count value specifies retransmission attempts, or it fails the call to [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span> <span data-ttu-id="8d62c-114">Число повторных попыток — это максимальное число попыток повторной передачи, которые делают реализация при сбое запроса на передачу SNMP.</span><span class="sxs-lookup"><span data-stu-id="8d62c-114">A retry count is the maximum number of retransmission attempts the implementation makes if an SNMP transmission request fails.</span></span>

<span data-ttu-id="8d62c-115">В реализации сохраняются значения времени ожидания и количество повторных попыток в базе данных для приложения.</span><span class="sxs-lookup"><span data-stu-id="8d62c-115">The implementation stores time-out values and retry counts in its database for the application.</span></span> <span data-ttu-id="8d62c-116">Реализация хранит отдельные значения для каждой целевой сущности.</span><span class="sxs-lookup"><span data-stu-id="8d62c-116">The implementation stores individual values for each destination entity.</span></span>

<span data-ttu-id="8d62c-117">Приложения должны устанавливать собственные частоты опроса, и они должны управлять переменными таймера.</span><span class="sxs-lookup"><span data-stu-id="8d62c-117">Applications must establish their own polling frequencies and they must manage timer variables.</span></span> <span data-ttu-id="8d62c-118">Дополнительные сведения см. [в разделе Управление политикой](managing-the-retransmission-policy.md)повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="8d62c-118">For more information, see [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 




