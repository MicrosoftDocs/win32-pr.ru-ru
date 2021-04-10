---
description: После установки контекста безопасности приложение может использовать функции поддержки сообщений для передачи сообщений, защищенных от изменения.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Обеспечение целостности связи во время обмена сообщениями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144485"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a><span data-ttu-id="c5717-103">Обеспечение целостности связи во время обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="c5717-103">Ensuring Communication Integrity During Message Exchange</span></span>

<span data-ttu-id="c5717-104">После установки [*контекста безопасности*](/windows/desktop/SecGloss/s-gly) приложение может использовать функции [поддержки сообщений](authentication-functions.md) для передачи сообщений, защищенных от изменения.</span><span class="sxs-lookup"><span data-stu-id="c5717-104">After a [*security context*](/windows/desktop/SecGloss/s-gly) is established, the application can use the [message support](authentication-functions.md) functions to transmit tamper-resistant messages.</span></span>

<span data-ttu-id="c5717-105">Клиент или сервер передает контекст безопасности и сообщение в функцию [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) для создания безопасной подписи, которая предотвращает изменение сообщения во время передачи.</span><span class="sxs-lookup"><span data-stu-id="c5717-105">The client or server passes the security context and a message to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a secure signature that prevents the message from being modified while in transit.</span></span> <span data-ttu-id="c5717-106">Получатель сообщения вызывает функцию [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) .</span><span class="sxs-lookup"><span data-stu-id="c5717-106">The receiver of the message calls the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function.</span></span> <span data-ttu-id="c5717-107">**VerifySignature** использует сведения в сигнатуре для проверки того, что полученное сообщение не было изменено во время передачи.</span><span class="sxs-lookup"><span data-stu-id="c5717-107">**VerifySignature** uses the information in the signature to verify that the message received was not modified during transmission.</span></span> <span data-ttu-id="c5717-108">Клиент и сервер могут также обмениваться зашифрованными сообщениями с помощью [**енкриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) и [**декриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="c5717-108">The client and server can also exchange encrypted messages using [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span>

<span data-ttu-id="c5717-109">Сервер в соединении с проверкой подлинности также может устанавливать соединения с другими удаленными компьютерами в имени клиента после вызова [**имперсонатесекуритиконтекст**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="c5717-109">The server in an authenticated connection can also make connections with other remote computers in the name of the client after calling [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span></span>

 

 
