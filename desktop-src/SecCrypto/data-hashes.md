---
description: Хэш текста или другой строки байтов — это связанное, статистическо уникальное значение фиксированной длины.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Хэши данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913044"
---
# <a name="data-hashes"></a><span data-ttu-id="2de84-103">Хэши данных</span><span class="sxs-lookup"><span data-stu-id="2de84-103">Data Hashes</span></span>

<span data-ttu-id="2de84-104">[*Хэш*](../secgloss/h-gly.md) текста или другой строки байтов — это связанное, статистическо уникальное значение фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="2de84-104">A [*hash*](../secgloss/h-gly.md) of a text or other string of bytes is an associated, statistically unique, fixed-length value.</span></span> <span data-ttu-id="2de84-105">В некоторых документах *хэш* текста также называется дайджестом; Однако в этой документации термин hash будет использоваться всегда.</span><span class="sxs-lookup"><span data-stu-id="2de84-105">In some documents, a *hash* of a text is also called a digest; however, in this documentation the term hash will always be used.</span></span> <span data-ttu-id="2de84-106">Функции CryptoAPI предоставляют средства для создания хэша для любого текста или другой строки байтов.</span><span class="sxs-lookup"><span data-stu-id="2de84-106">CryptoAPI functions provide a means to create a hash for any text or other string of bytes.</span></span> <span data-ttu-id="2de84-107">Затем этот хэш можно использовать в качестве уникального идентификатора связанных с ним данных.</span><span class="sxs-lookup"><span data-stu-id="2de84-107">That hash, then, can be used as a unique identifier of its associated data.</span></span>

<span data-ttu-id="2de84-108">Чтобы обеспечить [*целостность*](../secgloss/i-gly.md) текста, для сопровождающего текста можно отправить [*хэш*](../secgloss/h-gly.md) текста.</span><span class="sxs-lookup"><span data-stu-id="2de84-108">To ensure the [*integrity*](../secgloss/i-gly.md) of a text, a [*hash*](../secgloss/h-gly.md) of a text can be sent to accompany the text.</span></span> <span data-ttu-id="2de84-109">Затем получатель может вычислить хэш на полученных данных и сравнить хэш, вычисленный с полученным хэшем.</span><span class="sxs-lookup"><span data-stu-id="2de84-109">The receiver can then compute a hash on the data received and compare the hash computed with the hash received.</span></span> <span data-ttu-id="2de84-110">Если эти два совпадения, полученные данные должны совпадать с данными, из которых был создан полученный хэш.</span><span class="sxs-lookup"><span data-stu-id="2de84-110">If the two match, the data received must be the same as the data from which the received hash was created.</span></span>

<span data-ttu-id="2de84-111">Чтобы получить хэш-значение, создайте хэш-объект с помощью [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="2de84-111">To obtain a hash value, create a hash object using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="2de84-112">Этот объект будет накапливать данные для проверки.</span><span class="sxs-lookup"><span data-stu-id="2de84-112">This object will accumulate the data to be verified.</span></span> <span data-ttu-id="2de84-113">Затем данные добавляются в хэш-объект с помощью функции [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="2de84-113">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="2de84-114">После добавления последнего блока данных в хэш функция [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) используется для получения хэш-значения данных.</span><span class="sxs-lookup"><span data-stu-id="2de84-114">After the last block of data is added to the hash, the [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) function is used to obtain the hash value of the data.</span></span>

<span data-ttu-id="2de84-115">Более высокая безопасность обеспечивается путем уничтожения хэш-объекта с [**криптдестройхаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) , как только получено хэш-значение.</span><span class="sxs-lookup"><span data-stu-id="2de84-115">Better security is provided by destroying the hash object with [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) as soon as the hash value has been obtained.</span></span>

 

 
