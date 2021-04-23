---
title: Отмена повторной передачи
description: Если в течение времени ожидания, указанного для целевой сущности, нет ответа на запрос на соединение и если для сущности указаны повторные передачи, реализация Microsoft WinSNMP повторно передает запрос.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067968"
---
# <a name="canceling-retransmission"></a><span data-ttu-id="1ee40-103">Отмена повторной передачи</span><span class="sxs-lookup"><span data-stu-id="1ee40-103">Canceling Retransmission</span></span>

<span data-ttu-id="1ee40-104">Если в течение времени ожидания, указанного для целевой сущности, нет ответа на запрос на соединение и если для сущности указаны повторные передачи, реализация Microsoft WinSNMP повторно передает запрос.</span><span class="sxs-lookup"><span data-stu-id="1ee40-104">If there is no response to a communication request within the time-out period specified for a destination entity, and if retransmissions are specified for the entity, the Microsoft WinSNMP implementation retransmits the request.</span></span> <span data-ttu-id="1ee40-105">Вызов функции [**снмпканцелмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) может отменить этот цикл повторной передачи и освободить внутренние структуры данных, связанные с запросом сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ee40-105">A call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function can cancel this retransmission cycle and release internal data structures associated with the message request.</span></span>

<span data-ttu-id="1ee40-106">Обратите внимание, что конечная сущность может получить сообщение SNMP, которое было отменено вызовом функции [**снмпканцелмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) .</span><span class="sxs-lookup"><span data-stu-id="1ee40-106">Note that it is possible for a destination entity to receive an SNMP message that has been canceled by a call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function.</span></span> <span data-ttu-id="1ee40-107">Также возможно, что целевая сущность может отвечать на отмененное сообщение SNMP.</span><span class="sxs-lookup"><span data-stu-id="1ee40-107">It is also possible that a destination entity can respond to a canceled SNMP message.</span></span> <span data-ttu-id="1ee40-108">Это обусловлено тем, что очередь транзакций выполняется на нескольких уровнях.</span><span class="sxs-lookup"><span data-stu-id="1ee40-108">This is because transaction queuing occurs at multiple levels.</span></span> <span data-ttu-id="1ee40-109">Однако после того, как сообщение было отменено вызовом [**снмпканцелмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), реализация Microsoft WinSNMP не передает сообщение, отправляет PDU ответа или отправляет в приложение уведомление о превышении времени ожидания для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ee40-109">However, once a message has been canceled by a call to [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), the Microsoft WinSNMP implementation will not retransmit the message, submit a response PDU, or send a time-out notification to the application for that message.</span></span>

 

 




