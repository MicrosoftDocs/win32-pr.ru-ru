---
description: Объясняется, как использовать поддержку сообщений SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Использование поддержки сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664030"
---
# <a name="using-message-support"></a><span data-ttu-id="c2315-103">Использование поддержки сообщений</span><span class="sxs-lookup"><span data-stu-id="c2315-103">Using Message Support</span></span>

<span data-ttu-id="c2315-104">После завершения подтверждения и установления безопасного подключения приложение может использовать функции [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**енкриптмессаже (Общие)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)и [**декриптмессаже (Общие)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) для обмена подписанными или зашифрованными данными приложения с удаленным компьютером.</span><span class="sxs-lookup"><span data-stu-id="c2315-104">After a handshake has been completed and a secure connection has been established, an application can use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature), and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions to exchange signed or encrypted application data with the remote computer.</span></span>

<span data-ttu-id="c2315-105">Примеры использования этих функций после установки [*контекста безопасности*](../secgloss/s-gly.md) демонстрируются в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c2315-105">Examples that use these functions after a [*security context*](../secgloss/s-gly.md) has been established are demonstrated in the following sections:</span></span>

-   [<span data-ttu-id="c2315-106">Подписывание сообщения</span><span class="sxs-lookup"><span data-stu-id="c2315-106">Signing a Message</span></span>](signing-a-message.md)
-   [<span data-ttu-id="c2315-107">Проверка сообщения</span><span class="sxs-lookup"><span data-stu-id="c2315-107">Verifying a Message</span></span>](verifying-a-message.md)
-   [<span data-ttu-id="c2315-108">Шифрование сообщения</span><span class="sxs-lookup"><span data-stu-id="c2315-108">Encrypting a Message</span></span>](encrypting-a-message.md)
-   [<span data-ttu-id="c2315-109">Расшифровка сообщения</span><span class="sxs-lookup"><span data-stu-id="c2315-109">Decrypting a Message</span></span>](decrypting-a-message.md)

 

 
