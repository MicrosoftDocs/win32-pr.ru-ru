---
description: Сообщение, упакованное в оболочку, является сообщением, зашифрованным для получателя или набора получателей.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Создание и получение сообщений с запечатанными данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662328"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a><span data-ttu-id="6a650-103">Создание и получение сообщений с запечатанными данными</span><span class="sxs-lookup"><span data-stu-id="6a650-103">Creating and Receiving Enveloped Data Messages</span></span>

<span data-ttu-id="6a650-104">Сообщение, упакованное в оболочку, является сообщением, зашифрованным для набора получателей.</span><span class="sxs-lookup"><span data-stu-id="6a650-104">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="6a650-105">В процессе енвелопмент создается ключ шифрования сеанса, и сообщение шифруется с помощью этого ключа.</span><span class="sxs-lookup"><span data-stu-id="6a650-105">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="6a650-106">Затем сам ключ шифрования шифруется отдельно для каждого получателя с помощью открытых ключей из каждого назначенного сертификата получателя.</span><span class="sxs-lookup"><span data-stu-id="6a650-106">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="6a650-107">Сообщение с оболочкой состоит из зашифрованного сообщения, сертификатов предполагаемых получателей и набора зашифрованных ключей, по одному для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="6a650-107">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="6a650-108">Созданное сообщение находится в формате [*PKCS \# 7*](../secgloss/p-gly.md)/КМС.</span><span class="sxs-lookup"><span data-stu-id="6a650-108">The message generated is in [*PKCS \#7*](../secgloss/p-gly.md)/CMS format.</span></span>

<span data-ttu-id="6a650-109">В следующих разделах приведены процедуры и примеры задач с упакованными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6a650-109">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="6a650-110">Кодирование запечатанных данных</span><span class="sxs-lookup"><span data-stu-id="6a650-110">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)
-   [<span data-ttu-id="6a650-111">Декодирование упакованных данных</span><span class="sxs-lookup"><span data-stu-id="6a650-111">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)
-   [<span data-ttu-id="6a650-112">Альтернативный код для кодирования запечатанного сообщения</span><span class="sxs-lookup"><span data-stu-id="6a650-112">Alternate Code for Encoding an Enveloped Message</span></span>](alternate-code-for-encoding-an-enveloped-message.md)
-   [<span data-ttu-id="6a650-113">Пример программы на языке C. кодирование подписанного сообщения с подписью</span><span class="sxs-lookup"><span data-stu-id="6a650-113">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
