---
description: Эти действия проверяют подпись подписанных данных.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Проверка подписанного сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664384"
---
# <a name="verifying-a-signed-message"></a><span data-ttu-id="92874-103">Проверка подписанного сообщения</span><span class="sxs-lookup"><span data-stu-id="92874-103">Verifying a Signed Message</span></span>

<span data-ttu-id="92874-104">Эти действия проверяют подпись подписанных данных.</span><span class="sxs-lookup"><span data-stu-id="92874-104">These steps verify the signature of signed data.</span></span> <span data-ttu-id="92874-105">На следующем рисунке показаны отдельные задачи, которые должны быть выполнены, как показано в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="92874-105">The following illustration depicts the individual tasks that must be accomplished, as shown in the list that follows it.</span></span>

![Проверка подписанного сообщения](images/verifmsg.png)

<span data-ttu-id="92874-107">**Проверка подписи подписанного сообщения**</span><span class="sxs-lookup"><span data-stu-id="92874-107">**To verify the signature of a signed message**</span></span>

1.  <span data-ttu-id="92874-108">Получение указателя на подписанное сообщение.</span><span class="sxs-lookup"><span data-stu-id="92874-108">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="92874-109">Откройте [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="92874-109">Open a [*certificate store*](../secgloss/c-gly.md).</span></span>
3.  <span data-ttu-id="92874-110">Используя идентификатор лица, содержащийся в сообщении, получите сертификат отправителя и получите маркер его [*открытого ключа*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="92874-110">Using the signer ID contained in the message, get the sender's certificate and get a handle to its [*public key*](../secgloss/p-gly.md).</span></span>

    <span data-ttu-id="92874-111">В качестве альтернативы этапам 2 и 3 можно использовать сертификат, содержащийся в сообщении, для получения открытого ключа подписавших.</span><span class="sxs-lookup"><span data-stu-id="92874-111">As an alternative to steps 2 and 3, you can use the certificate contained in the message to retrieve the signer's public key.</span></span>

4.  <span data-ttu-id="92874-112">С помощью открытого ключа подписи расшифровывать цифровую подпись, создавая первоначальный дайджест данных в сообщении.</span><span class="sxs-lookup"><span data-stu-id="92874-112">Using the signer's public key, decrypt the digital signature, producing the original digest of the data in the message.</span></span>
5.  <span data-ttu-id="92874-113">Используя хэш-алгоритм, содержащийся в сообщении, следует [*хэшировать*](../secgloss/h-gly.md) данные, содержащиеся в сообщении, выдавая новый дайджест.</span><span class="sxs-lookup"><span data-stu-id="92874-113">Using the hash algorithm contained in the message, [*hash*](../secgloss/h-gly.md) the data contained in the message, yielding a new digest.</span></span>
6.  <span data-ttu-id="92874-114">Сравните дайджест, полученный из сообщения, с новым только что созданным дайджестом.</span><span class="sxs-lookup"><span data-stu-id="92874-114">Compare the digest retrieved from the message with the new digest just created.</span></span>
7.  <span data-ttu-id="92874-115">Если эти две дайджеста совпадают, подпись проверяется.</span><span class="sxs-lookup"><span data-stu-id="92874-115">If the two digests match, the signature is verified.</span></span> <span data-ttu-id="92874-116">Это означает, что [*закрытый ключ*](../secgloss/p-gly.md) , который использовался для подписывания данных, соответствует открытому ключу, только что использовался для расшифровки подписи, и что данные не изменялись с момента подписания данных.</span><span class="sxs-lookup"><span data-stu-id="92874-116">This means that the [*private key*](../secgloss/p-gly.md) that was used to sign the data matches the public key just used to decrypt the signature, and that the data has not changed since the data was signed.</span></span>

    <span data-ttu-id="92874-117">Если два дайджеста не совпадают, подпись не проверяется, а закрытые или открытые ключи не совпадают или данные были изменены с момента подписания или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="92874-117">If the two digests do not match, the signature is not verified, and either the private/public keys do not match, or the data has been changed since the data was signed, or both.</span></span>

<span data-ttu-id="92874-118">Для проверки подписи можно использовать одну функцию [**криптверифимессажесигнатуре**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), как показано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="92874-118">A single function, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), can be used to verify a signature, as shown in the following procedure.</span></span>

<span data-ttu-id="92874-119">**Проверка подписанного сообщения**</span><span class="sxs-lookup"><span data-stu-id="92874-119">**To verify a signed message**</span></span>

1.  <span data-ttu-id="92874-120">Получение указателя на подписанное сообщение.</span><span class="sxs-lookup"><span data-stu-id="92874-120">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="92874-121">Возвращает размер подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="92874-121">Get the size of the signed message.</span></span>
3.  <span data-ttu-id="92874-122">Получение маркера для поставщика служб шифрования.</span><span class="sxs-lookup"><span data-stu-id="92874-122">Get a handle on a cryptographic provider.</span></span>
4.  <span data-ttu-id="92874-123">Инициализируйте структуру " [**Проверка шифрования сообщения с помощью \_ \_ \_ абзаца**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) ".</span><span class="sxs-lookup"><span data-stu-id="92874-123">Initialize the [**CRYPT\_VERIFY\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) structure.</span></span>
5.  <span data-ttu-id="92874-124">Вызовите [**криптверифимессажесигнатуре**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) , чтобы проверить подпись.</span><span class="sxs-lookup"><span data-stu-id="92874-124">Call [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) to verify the signature.</span></span>

<span data-ttu-id="92874-125">Код, реализующий эту процедуру, включен в [Пример программы на языке C: подпись сообщения и проверка подписи сообщения](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="92874-125">Code that implements this procedure is included in [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
