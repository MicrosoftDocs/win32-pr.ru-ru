---
title: О ловушках и уведомлениях
description: Одним из типов сообщений, которые приложение агента SNMP может отправить в приложение WinSNMP, является асинхронное сообщение, которое информирует приложение о значительных событиях.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888428"
---
# <a name="about-traps-and-notifications"></a><span data-ttu-id="70ce8-103">О ловушках и уведомлениях</span><span class="sxs-lookup"><span data-stu-id="70ce8-103">About Traps and Notifications</span></span>

<span data-ttu-id="70ce8-104">Одним из типов сообщений, которые приложение агента SNMP может отправить в приложение WinSNMP, является асинхронное сообщение, которое информирует приложение о значительных событиях.</span><span class="sxs-lookup"><span data-stu-id="70ce8-104">One type of message an SNMP agent application can send to a WinSNMP application is an asynchronous message that informs the application of a significant event.</span></span> <span data-ttu-id="70ce8-105">Примером значительного события является ситуация, когда сетевая связь завершается или происходит сбой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="70ce8-105">An example of a significant event is when a network link shuts down or when an authentication failure occurs.</span></span>

<span data-ttu-id="70ce8-106">Эти типы сообщений называются ловушками в версии с и уведомлениями в разделе SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="70ce8-106">These types of messages are called traps under SNMPv1 and notifications under SNMPv2C.</span></span> <span data-ttu-id="70ce8-107">Реализация Microsoft WinSNMP всегда преобразует ловушки в формат SNMPv2C, как определено в RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="70ce8-107">The Microsoft WinSNMP implementation always translates SNMPv1 traps to the SNMPv2C format, as defined by RFC 1908.</span></span>

<span data-ttu-id="70ce8-108">При вызове функции [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) для создания PDU ловушки можно создать только PDU ловушки SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="70ce8-108">When you call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function to create a trap PDU, you can create only an SNMPv2C trap PDU.</span></span> <span data-ttu-id="70ce8-109">Единственный тип PDU ловушки, который можно обновить с помощью вызова функции [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) , — это PDU ловушки SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="70ce8-109">The only type of trap PDU you can update with a call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function is an SNMPv2C trap PDU.</span></span>

<span data-ttu-id="70ce8-110">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="70ce8-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="70ce8-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="70ce8-111">Topic</span></span>                                                                                    | <span data-ttu-id="70ce8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="70ce8-112">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="70ce8-113">Перевод ловушек с SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="70ce8-113">Translating Traps from SNMPv1 to SNMPv2C</span></span>](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [<span data-ttu-id="70ce8-114">Форматы ловушек</span><span class="sxs-lookup"><span data-stu-id="70ce8-114">Trap Formats</span></span>](trap-formats.md)                                                         |             |



 

 

 




