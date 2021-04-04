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
# <a name="device-events-telephony-api"></a>События устройства (API телефонии)

TAPI реагирует на такие изменения устройств, как Телефон, который начал звонить, или модем, который был удален при обработке событий устройства. Приложение TAPI должно реагировать на событие устройства путем запроса определенного изменения, которое произошло, и принятия соответствующего действия. Приложение может экранировать события, которые он получит с помощью [уведомления о событии](event-notification.md).

**Интерфейс TAPI 2. x:** Приложения получают уведомления о событиях устройства с помощью сообщения [**Line \_ линедевстате**](./line-linedevstate.md) . Текущее состояние адреса определяется путем вызова [**линежетаддрессстатус**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), который возвращает сведения в структуре [**линеаддрессстатус**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) . Состояние указанного устройства Open Line получается путем вызова [**линежетлинедевстатус**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), который возвращает сведения в структуре [**линедевстатус**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .

**Интерфейс TAPI 3. x:** Приложения получают уведомление [**о \_ событии адреса**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , которое обрабатывается с помощью интерфейса [**итаддрессевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) . Затем [**итаддресскапабилитиес**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) можно использовать для получения более подробных сведений.

 

 
