---
description: На основе кода возврата из предыдущего вызова AcceptSecurityContext (Общие) сервер может ожидать ответа от клиента и может участвовать в дополнительных обменах с клиентом.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Продолжение сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06863a0e94fcfe65c7ab695d30be92044fe7341ffa0eb9091c5f1a81acdffc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918293"
---
# <a name="server-continuation"></a>Продолжение сервера

На основе кода возврата из предыдущего вызова [**AcceptSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)сервер может ожидать ответа от клиента и может участвовать в дополнительных обменах с клиентом. Чтобы продолжить протокол проверки подлинности, сервер повторяет вызовы **AcceptSecurityContext (Общие)**.

Состояние, возвращаемое функцией [**AcceptSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) , проверяется на необходимость ожидания сервером дополнительных сообщений от клиента. В большинстве протоколов проверки подлинности для взаимной проверки подлинности существует максимальное количество обменов. В настоящее время [*протоколы*](../secgloss/k-gly.md) NTLM и Kerberos выполняют взаимную проверку подлинности с тремя Exchange.

 

 
