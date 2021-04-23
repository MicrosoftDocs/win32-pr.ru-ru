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
# <a name="server-continuation"></a><span data-ttu-id="39dab-103">Продолжение сервера</span><span class="sxs-lookup"><span data-stu-id="39dab-103">Server Continuation</span></span>

<span data-ttu-id="39dab-104">На основе кода возврата из предыдущего вызова [**AcceptSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)сервер может ожидать ответа от клиента и может участвовать в дополнительных обменах с клиентом.</span><span class="sxs-lookup"><span data-stu-id="39dab-104">Based on the return code from a previous call to [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), the server can wait for a response from the client and can participate in additional exchanges with the client.</span></span> <span data-ttu-id="39dab-105">Чтобы продолжить протокол проверки подлинности, сервер повторяет вызовы **AcceptSecurityContext (Общие)**.</span><span class="sxs-lookup"><span data-stu-id="39dab-105">To continue the authentication protocol, the server repeats calls to **AcceptSecurityContext (General)**.</span></span>

<span data-ttu-id="39dab-106">Состояние, возвращаемое функцией [**AcceptSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) , проверяется на необходимость ожидания сервером дополнительных сообщений от клиента.</span><span class="sxs-lookup"><span data-stu-id="39dab-106">The status returned by [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) is checked to see if the server needs to wait for additional messages from the client.</span></span> <span data-ttu-id="39dab-107">В большинстве протоколов проверки подлинности для взаимной проверки подлинности существует максимальное количество обменов.</span><span class="sxs-lookup"><span data-stu-id="39dab-107">In most authentication protocols, there is a maximum number of exchanges even for mutual authentication.</span></span> <span data-ttu-id="39dab-108">В настоящее время [*протоколы*](../secgloss/k-gly.md) NTLM и Kerberos выполняют взаимную проверку подлинности с тремя Exchange.</span><span class="sxs-lookup"><span data-stu-id="39dab-108">Currently, both the NTLM and [*Kerberos protocols*](../secgloss/k-gly.md) do mutual authentication with three exchanges.</span></span>

 

 
