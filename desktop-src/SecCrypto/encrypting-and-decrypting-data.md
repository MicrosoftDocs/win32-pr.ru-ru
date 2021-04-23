---
description: Если документ или текст должен иметь конфиденциальность, защищенную одним пользователем, или если документ должен быть общим для небольшой группы людей, имеющих доступ к одному и тому же паролю секрета, можно выполнить простое шифрование и расшифровку.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Шифрование и расшифровка данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999138"
---
# <a name="encrypting-and-decrypting-data"></a><span data-ttu-id="4f298-103">Шифрование и расшифровка данных</span><span class="sxs-lookup"><span data-stu-id="4f298-103">Encrypting and Decrypting Data</span></span>

<span data-ttu-id="4f298-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4f298-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4f298-105">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="4f298-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="4f298-106">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="4f298-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="4f298-107">Если документ или текст должен иметь конфиденциальность, защищенную одним пользователем, или если документ должен быть общим для небольшой группы людей, имеющих доступ к одному и тому же паролю секрета, можно выполнить простое шифрование и расшифровку.</span><span class="sxs-lookup"><span data-stu-id="4f298-107">When a document or text needs to have privacy protected by a single user or when the document is to be shared among a small group of people who all have access to the same secret password, simple encryption/decryption can be done.</span></span> <span data-ttu-id="4f298-108">CAPICOM не поддерживает \# тип содержимого EncryptedData, но использует нестандартную структуру ASN для EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="4f298-108">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a non-standard ASN structure for EncryptedData.</span></span> <span data-ttu-id="4f298-109">Таким образом, только CAPICOM может расшифровать объект CAPICOM EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="4f298-109">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

<span data-ttu-id="4f298-110">В следующих разделах приведены примеры задач шифрования и расшифровки.</span><span class="sxs-lookup"><span data-stu-id="4f298-110">The following sections show examples for encryption and decryption tasks:</span></span>

-   [<span data-ttu-id="4f298-111">Шифрование сообщения в CAPICOM</span><span class="sxs-lookup"><span data-stu-id="4f298-111">Encrypting a Message in CAPICOM</span></span>](encrypting-a-message-in-capicom.md)
-   [<span data-ttu-id="4f298-112">Расшифровка сообщения в CAPICOM</span><span class="sxs-lookup"><span data-stu-id="4f298-112">Decrypting a Message in CAPICOM</span></span>](decrypting-a-message-in-capicom.md)

 

 



