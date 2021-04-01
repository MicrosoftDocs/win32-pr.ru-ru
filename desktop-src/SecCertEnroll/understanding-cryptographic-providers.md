---
description: Поставщики реализуют алгоритмы шифрования, создают ключи, предоставляют хранилище ключей и выполняют проверку подлинности пользователей. Поставщики можно реализовать в оборудовании, программном обеспечении или в обоих случаях.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Общие сведения о поставщиках служб шифрования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999070"
---
# <a name="understanding-cryptographic-providers"></a><span data-ttu-id="46567-104">Общие сведения о поставщиках служб шифрования</span><span class="sxs-lookup"><span data-stu-id="46567-104">Understanding Cryptographic Providers</span></span>

<span data-ttu-id="46567-105">Концепция поставщика служб шифрования, представленная в API криптографии ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) и которая в некоторой степени развивалась в [*API шифрования: следующее поколение*](/windows/desktop/SecGloss/c-gly) (CNG) является центральной для безопасной реализации криптографических функций в операционных системах Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="46567-105">The cryptographic provider concept that was introduced in Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) and which evolved somewhat in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) is central to the secure implementation of cryptographic functionality on Microsoft operating systems.</span></span> <span data-ttu-id="46567-106">Эти два пакета SDK использовались для создания множества приложений и вызываются внутренним образом другими пакетами SDK.</span><span class="sxs-lookup"><span data-stu-id="46567-106">These two SDKs have been used to create many applications and are called internally by other SDKs.</span></span> <span data-ttu-id="46567-107">Например, службы сертификации Active Directory и API регистрации сертификатов полагаются на CryptoAPI и CNG.</span><span class="sxs-lookup"><span data-stu-id="46567-107">For example, Active Directory Certificate Services and the Certificate Enrollment API rely on CryptoAPI and CNG.</span></span>

<span data-ttu-id="46567-108">Как правило, поставщики реализуют алгоритмы шифрования, создают ключи, предоставляют хранилище ключей и выполняют проверку подлинности пользователей.</span><span class="sxs-lookup"><span data-stu-id="46567-108">In general, providers implement cryptographic algorithms, generate keys, provide key storage, and authenticate users.</span></span> <span data-ttu-id="46567-109">Поставщики можно реализовать в оборудовании, программном обеспечении или в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="46567-109">Providers can be implemented in hardware, software, or both.</span></span> <span data-ttu-id="46567-110">Приложения, построенные с помощью CryptoAPI или CNG, не могут изменять ключи, созданные поставщиками, и не могут изменять реализацию алгоритма шифрования.</span><span class="sxs-lookup"><span data-stu-id="46567-110">Applications built by using CryptoAPI or CNG cannot alter the keys created by providers, and they cannot alter cryptographic algorithm implementation.</span></span> <span data-ttu-id="46567-111">Несколько поставщиков, созданных корпорацией Майкрософт, распространяются вместе с операционными системами.</span><span class="sxs-lookup"><span data-stu-id="46567-111">The multiple providers created by Microsoft are distributed with the operating systems.</span></span> <span data-ttu-id="46567-112">Другие поставщики были созданы и распространены третьими сторонами.</span><span class="sxs-lookup"><span data-stu-id="46567-112">Other providers have been created and distributed by third parties.</span></span>

<span data-ttu-id="46567-113">В следующих разделах рассматриваются различия между поставщиками, связанными с CryptoAPI, и теми, которые связаны с CNG.</span><span class="sxs-lookup"><span data-stu-id="46567-113">The following topics highlight the differences between providers associated with CryptoAPI and those associated with CNG.</span></span> <span data-ttu-id="46567-114">Как правило, эта документация относится к поставщикам без ссылки на пакет SDK, с которым они связаны, и отмечается только тогда, когда они актуальны.</span><span class="sxs-lookup"><span data-stu-id="46567-114">Typically, this documentation refers to providers without reference to the SDK with which they are associated, noting the association only when it is relevant.</span></span>

-   [<span data-ttu-id="46567-115">Поставщики служб шифрования CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="46567-115">CryptoAPI Cryptographic Service Providers</span></span>](cryptoapi-cryptographic-service-providers.md)
-   [<span data-ttu-id="46567-116">Поставщики алгоритмов шифрования CNG</span><span class="sxs-lookup"><span data-stu-id="46567-116">CNG Cryptographic Algorithm Providers</span></span>](cng-cryptographic-algorithm-providers.md)
-   [<span data-ttu-id="46567-117">Поставщики хранилища ключей CNG</span><span class="sxs-lookup"><span data-stu-id="46567-117">CNG Key Storage Providers</span></span>](cng-key-storage-providers.md)
-   [<span data-ttu-id="46567-118">Перечисление установленных поставщиков</span><span class="sxs-lookup"><span data-stu-id="46567-118">Enumerating Installed Providers</span></span>](enumerating-installed-providers.md)

## <a name="related-topics"></a><span data-ttu-id="46567-119">См. также</span><span class="sxs-lookup"><span data-stu-id="46567-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46567-120">Использование API регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="46567-120">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
