---
description: Объясняется, как защитить сообщения с помощью Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Защита сообщений с помощью Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650872"
---
# <a name="protecting-messages-using-microsoft-digest"></a><span data-ttu-id="3868e-103">Защита сообщений с помощью Microsoft Digest</span><span class="sxs-lookup"><span data-stu-id="3868e-103">Protecting Messages Using Microsoft Digest</span></span>

## <a name="http-and-sasl"></a><span data-ttu-id="3868e-104">HTTP и SASL</span><span class="sxs-lookup"><span data-stu-id="3868e-104">HTTP and SASL</span></span>

<span data-ttu-id="3868e-105">В качестве средства обнаружения определенных типов нарушений безопасности клиент и сервер используют функции [*проверки целостности*](../secgloss/i-gly.md) сообщений [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) и [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) для защиты сообщений в [интерфейсе поставщика поддержки безопасности](sspi.md) (SSPI).</span><span class="sxs-lookup"><span data-stu-id="3868e-105">As a means of detecting certain types of security violations, the client and server use the [security support provider interface](sspi.md) (SSPI) message [*integrity*](../secgloss/i-gly.md) functions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) to protect messages.</span></span>

<span data-ttu-id="3868e-106">Клиент вызывает функцию [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) для подписывания сообщения с помощью [*контекста безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3868e-106">A client calls the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to sign a message using its [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="3868e-107">Сервер использует функцию [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) для проверки источника сообщения.</span><span class="sxs-lookup"><span data-stu-id="3868e-107">The server uses the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function to verify the message's origin.</span></span> <span data-ttu-id="3868e-108">Кроме проверки [*подписи*](../secgloss/d-gly.md) , сопровождающей сообщение, функция **VerifySignature** также проверяет, что число [*nonce*](../secgloss/n-gly.md) (заданное директивой NC) больше, чем Последнее число, отправленное для nonce.</span><span class="sxs-lookup"><span data-stu-id="3868e-108">In addition to verifying the [*signature*](../secgloss/d-gly.md) that accompanies the message, the **VerifySignature** function also checks that the [*nonce*](../secgloss/n-gly.md) count (specified by the nc directive) is one greater than the last count sent for the nonce.</span></span> <span data-ttu-id="3868e-109">Если это не так, функция **VerifySignature** возвращает \_ \_ \_ код ошибки с непоследовательной последовательностью.</span><span class="sxs-lookup"><span data-stu-id="3868e-109">If this is not the case, the **VerifySignature** function returns an SEC\_OUT\_OF\_SEQUENCE error code.</span></span>

## <a name="sasl-only"></a><span data-ttu-id="3868e-110">Только SASL</span><span class="sxs-lookup"><span data-stu-id="3868e-110">SASL Only</span></span>

<span data-ttu-id="3868e-111">Функции [**енкриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) и [**декриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) предоставляют конфиденциальность сообщений после проверки подлинности, которыми обмениваются клиент и сервер.</span><span class="sxs-lookup"><span data-stu-id="3868e-111">The [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions supply confidentiality for post-authentication messages exchanged between client and server.</span></span>

<span data-ttu-id="3868e-112">Чтобы использовать функции обеспечения конфиденциальности сообщений, сервер и клиент должны установить [*контекст безопасности*](../secgloss/s-gly.md) со следующими атрибутами:</span><span class="sxs-lookup"><span data-stu-id="3868e-112">In order to use the message confidentiality functions, the server and client must have established a [*security context*](../secgloss/s-gly.md) with the following attributes:</span></span>

-   <span data-ttu-id="3868e-113">Качество защиты, заданное директивой КОП, должно иметь значение "auth-conf".</span><span class="sxs-lookup"><span data-stu-id="3868e-113">Quality of protection, specified by the qop directive, must be "auth-conf".</span></span>
-   <span data-ttu-id="3868e-114">Механизм шифрования должен быть указан с помощью директивы шифра.</span><span class="sxs-lookup"><span data-stu-id="3868e-114">An encryption mechanism must have been specified by means of the cipher directive.</span></span>

 

 
