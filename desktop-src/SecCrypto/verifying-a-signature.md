---
description: Чтобы проверить подпись, создайте хэш-объект с помощью CryptCreateHash. Этот объект хэша накапливает данные для проверки. Затем данные добавляются в хэш-объект с помощью функции CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Проверка подписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155071"
---
# <a name="verifying-a-signature"></a><span data-ttu-id="bd48a-105">Проверка подписи</span><span class="sxs-lookup"><span data-stu-id="bd48a-105">Verifying a Signature</span></span>

<span data-ttu-id="bd48a-106">Чтобы проверить подпись, создайте [*хэш-объект*](../secgloss/h-gly.md) с помощью [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="bd48a-106">To verify a signature, create a [*hash object*](../secgloss/h-gly.md) using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="bd48a-107">Этот объект хэша накапливает данные для проверки.</span><span class="sxs-lookup"><span data-stu-id="bd48a-107">This hash object accumulates the data to be verified.</span></span> <span data-ttu-id="bd48a-108">Затем данные добавляются в хэш-объект с помощью функции [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="bd48a-108">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="bd48a-109">После добавления последнего блока данных в хэш используйте [**криптверифисигнатуре**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) для проверки подписи.</span><span class="sxs-lookup"><span data-stu-id="bd48a-109">After the last block of data is added to the hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) to verify the signature.</span></span> <span data-ttu-id="bd48a-110">Адрес данных подписи, маркер для хэш-объекта, а также маркер открытых ключей передаются в **криптверифисигнатуре**.</span><span class="sxs-lookup"><span data-stu-id="bd48a-110">The address of the signature data, a handle to the hash object, and the handle of the public keys are passed to **CryptVerifySignature**.</span></span>

<span data-ttu-id="bd48a-111">После проверки подписи (или неудачной проверки) удалите хэш-объект с помощью функции [**криптдестройхаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="bd48a-111">After the signature has been verified (or has failed the verification), destroy the hash object using the [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) function.</span></span>

 

 
