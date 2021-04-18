---
title: Включение и отключение повторной отправки
description: Приложение может установить режим повторной передачи с помощью вызова функции Снмпсетретрансмитмоде. Новый режим повторной передачи применяется к последующим вызовам функции Снмпсендмсг.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681398"
---
# <a name="turning-retransmission-on-and-off"></a><span data-ttu-id="6deef-104">Включение и отключение повторной отправки</span><span class="sxs-lookup"><span data-stu-id="6deef-104">Turning Retransmission On and Off</span></span>

<span data-ttu-id="6deef-105">Приложение может установить режим повторной передачи с помощью вызова функции [**снмпсетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="6deef-105">An application can set the retransmission mode with a call to the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="6deef-106">Новый режим повторной передачи применяется к последующим вызовам функции [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="6deef-106">The new retransmission mode applies to subsequent calls to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span>

<span data-ttu-id="6deef-107">Когда приложение вызывает **снмпсетретрансмитмоде** с ПАРАМЕТРом снмпапи в режиме повторной передачи \_ , реализация Microsoft WinSNMP начинает выполнение политики повторной передачи приложения.</span><span class="sxs-lookup"><span data-stu-id="6deef-107">When the application calls **SnmpSetRetransmitMode** with the retransmission mode value SNMPAPI\_ON, the Microsoft WinSNMP implementation begins execution of the application's retransmission policy.</span></span> <span data-ttu-id="6deef-108">Новый режим повторной передачи не влияет на необработанные SNMP-сообщения.</span><span class="sxs-lookup"><span data-stu-id="6deef-108">The new retransmission mode does not affect outstanding SNMP messages.</span></span> <span data-ttu-id="6deef-109">Необработанное сообщение — это запрос, не имеющий ответа на момент, когда приложение изменяет режим повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="6deef-109">An outstanding message is one that has no response at the time the application changes the retransmission mode.</span></span>

<span data-ttu-id="6deef-110">Если приложение WinSNMP вызывает функцию [**снмпсетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) с параметром mode повторной передачи снмпапи \_ Off, реализация прекращает выполнение политики повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="6deef-110">When the WinSNMP application calls the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function with the retransmission mode value SNMPAPI\_OFF, the implementation stops executing the retransmission policy.</span></span> <span data-ttu-id="6deef-111">Реализация отменяет попытки повторной передачи для необработанных SNMP-сообщений.</span><span class="sxs-lookup"><span data-stu-id="6deef-111">The implementation cancels retransmission attempts for outstanding SNMP messages.</span></span> <span data-ttu-id="6deef-112">Это связано с тем, что реализация может не обрабатывать все необработанные SNMP-запросы и операции, а также новые запросы, прежде чем время ожидания приложения или счетчик повторных попыток сигнализирует о событии.</span><span class="sxs-lookup"><span data-stu-id="6deef-112">This is because it may not be possible for the implementation to handle all outstanding SNMP requests and operations plus new requests, before an application time-out or retry counter signals an event.</span></span>

 

 




