---
description: На основе кода возврата из предыдущего вызова AcceptSecurityContext (Общие) сервер может ожидать ответа от клиента и может участвовать в дополнительных обменах с клиентом.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Продолжение сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663017"
---
# <a name="server-continuation"></a>Продолжение сервера

На основе кода возврата из предыдущего вызова [**AcceptSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)сервер может ожидать ответа от клиента и может участвовать в дополнительных обменах с клиентом. Чтобы продолжить протокол проверки подлинности, сервер повторяет вызовы **AcceptSecurityContext (Общие)**.

Состояние, возвращаемое функцией [**AcceptSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) , проверяется на необходимость ожидания сервером дополнительных сообщений от клиента. В большинстве протоколов проверки подлинности для взаимной проверки подлинности существует максимальное количество обменов. В настоящее время [*протоколы*](../secgloss/k-gly.md) NTLM и Kerberos выполняют взаимную проверку подлинности с тремя Exchange.

 

 
