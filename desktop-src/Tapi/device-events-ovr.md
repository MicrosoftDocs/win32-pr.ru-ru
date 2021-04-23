---
description: TAPI реагирует на такие изменения устройств, как Телефон, который начал звонить, или модем, который был удален при обработке событий устройства.
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: События устройства (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f5508e74424a13117facc1c4c370144ecd46de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809869"
---
# <a name="device-events-telephony-api"></a><span data-ttu-id="1934a-103">События устройства (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="1934a-103">Device Events (Telephony API)</span></span>

<span data-ttu-id="1934a-104">TAPI реагирует на такие изменения устройств, как Телефон, который начал звонить, или модем, который был удален при обработке событий устройства.</span><span class="sxs-lookup"><span data-stu-id="1934a-104">TAPI responds to device changes such as a phone that has started ringing or a modem that has been removed by firing device events.</span></span> <span data-ttu-id="1934a-105">Приложение TAPI должно реагировать на событие устройства путем запроса определенного изменения, которое произошло, и принятия соответствующего действия.</span><span class="sxs-lookup"><span data-stu-id="1934a-105">A TAPI application should respond to a device event by querying for the specific change that has occurred and then taking appropriate action.</span></span> <span data-ttu-id="1934a-106">Приложение может экранировать события, которые он получит с помощью [уведомления о событии](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="1934a-106">An application may screen for events it will receive using [event notification](event-notification.md).</span></span>

<span data-ttu-id="1934a-107">**Интерфейс TAPI 2. x:** Приложения получают уведомления о событиях устройства с помощью сообщения [**Line \_ линедевстате**](./line-linedevstate.md) .</span><span class="sxs-lookup"><span data-stu-id="1934a-107">**TAPI 2.x:** Applications receive notification of device events using the [**LINE\_LINEDEVSTATE**](./line-linedevstate.md) message.</span></span> <span data-ttu-id="1934a-108">Текущее состояние адреса определяется путем вызова [**линежетаддрессстатус**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), который возвращает сведения в структуре [**линеаддрессстатус**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="1934a-108">The current status of an address is determined by calling [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), which returns its information in a [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="1934a-109">Состояние указанного устройства Open Line получается путем вызова [**линежетлинедевстатус**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), который возвращает сведения в структуре [**линедевстатус**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="1934a-109">The status of a specified open line device is obtained by calling [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), which returns its information in a [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure.</span></span>

<span data-ttu-id="1934a-110">**Интерфейс TAPI 3. x:** Приложения получают уведомление [**о \_ событии адреса**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , которое обрабатывается с помощью интерфейса [**итаддрессевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) .</span><span class="sxs-lookup"><span data-stu-id="1934a-110">**TAPI 3.x:** Applications receive an [**ADDRESS\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) notification, which is processed using the [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) interface.</span></span> <span data-ttu-id="1934a-111">Затем [**итаддресскапабилитиес**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) можно использовать для получения более подробных сведений.</span><span class="sxs-lookup"><span data-stu-id="1934a-111">The [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) can then be used to acquire more detail information.</span></span>

 

 
