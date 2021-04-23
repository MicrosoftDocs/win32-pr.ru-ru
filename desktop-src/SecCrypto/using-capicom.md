---
description: В этом разделе содержатся сценарии, в которых используются процедуры CAPICOM.
ms.assetid: f886e04a-4ea7-4d24-a05f-3e08742fe134
title: Использование элемента CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81b1a346b6186ead6544b7194259cc52ae2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543522"
---
# <a name="using-capicom"></a><span data-ttu-id="57168-103">Использование элемента CAPICOM</span><span class="sxs-lookup"><span data-stu-id="57168-103">Using CAPICOM</span></span>

<span data-ttu-id="57168-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="57168-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="57168-105">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="57168-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="57168-106">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="57168-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="57168-107">В этом разделе содержатся сценарии, в которых используются процедуры CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="57168-107">This section includes scenarios that use CAPICOM procedures.</span></span>

> [!Note]  
> <span data-ttu-id="57168-108">Создание [*цифровых подписей*](../secgloss/d-gly.md) и запечатывание сообщений с помощью CAPICOM выполняется с помощью криптографии инфраструктуры открытых ключей (PKI). это можно сделать только в том случае, если подписавший или пользователь, расшифрованный запечатанный текст, имеет доступ к сертификату с доступным закрытым ключом.</span><span class="sxs-lookup"><span data-stu-id="57168-108">Creating [*digital signatures*](../secgloss/d-gly.md) and un-enveloping messages with CAPICOM is done using Public Key Infrastructure (PKI) cryptography and can only be done if the signer or user decrypting an enveloped message has access to a certificate with an available, associated private key.</span></span> <span data-ttu-id="57168-109">Для расшифровки запечатанного сообщения сертификат с доступом к закрытому ключу должен находиться в хранилище MY.</span><span class="sxs-lookup"><span data-stu-id="57168-109">To decrypt an enveloped message, a certificate with access to the private key must be in the MY store.</span></span>

 

<span data-ttu-id="57168-110">Обсуждения и примеры сценариев на основе задач были разделены на следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="57168-110">Task-based scenarios discussions and examples have been separated into the following sections:</span></span>

-   [<span data-ttu-id="57168-111">Альтернативы использованию CAPICOM</span><span class="sxs-lookup"><span data-stu-id="57168-111">Alternatives to Using CAPICOM</span></span>](alternatives-to-using-capicom.md)
-   [<span data-ttu-id="57168-112">Подготовка к использованию элемента CAPICOM</span><span class="sxs-lookup"><span data-stu-id="57168-112">Getting Ready to Use CAPICOM</span></span>](getting-ready-to-use-capicom.md)
-   [<span data-ttu-id="57168-113">Шифрование и расшифровка данных</span><span class="sxs-lookup"><span data-stu-id="57168-113">Encrypting and Decrypting Data</span></span>](encrypting-and-decrypting-data.md)
-   [<span data-ttu-id="57168-114">Подписывание данных и проверка цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="57168-114">Signing Data and Verifying Digital Signatures</span></span>](signing-data-and-verifying-digital-signatures.md)
-   [<span data-ttu-id="57168-115">Использование хранилищ сертификатов</span><span class="sxs-lookup"><span data-stu-id="57168-115">Using Certificate Stores</span></span>](using-certificate-stores.md)
-   [<span data-ttu-id="57168-116">Создание и получение сообщений с запечатанными данными</span><span class="sxs-lookup"><span data-stu-id="57168-116">Creating and Receiving Enveloped Data Messages</span></span>](creating-and-receiving-enveloped-data-messages-in-capicom.md)

 

 
