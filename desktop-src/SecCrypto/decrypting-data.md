---
description: Представляет шаги для расшифровки зашифрованного сообщения.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Расшифровка данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970f16862bb8c6693b2ff11f519af3f7c412024b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350155"
---
# <a name="decrypting-data"></a><span data-ttu-id="db423-103">Расшифровка данных</span><span class="sxs-lookup"><span data-stu-id="db423-103">Decrypting Data</span></span>

<span data-ttu-id="db423-104">В этом разделе описываются действия по расшифровке зашифрованного сообщения.</span><span class="sxs-lookup"><span data-stu-id="db423-104">This section presents the steps to decrypt an encrypted message.</span></span>

<span data-ttu-id="db423-105">**Расшифровка зашифрованного сообщения**</span><span class="sxs-lookup"><span data-stu-id="db423-105">**To decrypt an encrypted message**</span></span>

1.  <span data-ttu-id="db423-106">Получает указатель на сообщение с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="db423-106">Get a pointer to the digitally enveloped message.</span></span>
2.  <span data-ttu-id="db423-107">Откройте хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="db423-107">Open a certificate store.</span></span>
3.  <span data-ttu-id="db423-108">В сообщении получите идентификатор получателя (My ID).</span><span class="sxs-lookup"><span data-stu-id="db423-108">From the message, retrieve the recipient identifier (My ID).</span></span>
4.  <span data-ttu-id="db423-109">Используйте идентификатор получателя для получения сертификата.</span><span class="sxs-lookup"><span data-stu-id="db423-109">Use the recipient identifier to retrieve the certificate.</span></span>
5.  <span data-ttu-id="db423-110">Получите закрытый ключ для сертификата.</span><span class="sxs-lookup"><span data-stu-id="db423-110">Get the private key for the certificate.</span></span>
6.  <span data-ttu-id="db423-111">Используйте закрытый ключ для расшифровки симметричного ключа (сеанса).</span><span class="sxs-lookup"><span data-stu-id="db423-111">Use the private key to decrypt the symmetric (session) key.</span></span>
7.  <span data-ttu-id="db423-112">Получение алгоритма шифрования из сообщения.</span><span class="sxs-lookup"><span data-stu-id="db423-112">Retrieve the encryption algorithm from the message.</span></span>
8.  <span data-ttu-id="db423-113">Расшифровка данных с помощью расшифрованного ключа сеанса и алгоритма шифрования.</span><span class="sxs-lookup"><span data-stu-id="db423-113">Using the decrypted session key and the encryption algorithm, decrypt the data.</span></span>

<span data-ttu-id="db423-114">[**Криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) выполняет все задачи для расшифровки сообщения; Тем не менее, все еще необходимо инициализировать структуры и другие данные.</span><span class="sxs-lookup"><span data-stu-id="db423-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) does all of the tasks for decrypting a message; however, initialization of structures and other data is still necessary.</span></span>

<span data-ttu-id="db423-115">**Расшифровка данных с помощью Криптдекриптмессаже**</span><span class="sxs-lookup"><span data-stu-id="db423-115">**To decrypt data using CryptDecryptMessage**</span></span>

1.  <span data-ttu-id="db423-116">Получите указатель на зашифрованный большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="db423-116">Get a pointer to the encrypted BLOB.</span></span>
2.  <span data-ttu-id="db423-117">Откройте хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="db423-117">Open a certificate store.</span></span>
3.  <span data-ttu-id="db423-118">Создайте массив хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="db423-118">Create a certificate store array.</span></span>
4.  <span data-ttu-id="db423-119">Инициализируйте [**структуру \_ расшифровки расшифрованного сообщения в виде \_ \_ абзаца**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) .</span><span class="sxs-lookup"><span data-stu-id="db423-119">Initialize the [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) structure.</span></span>
5.  <span data-ttu-id="db423-120">Вызовите [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) , чтобы расшифровать данные, содержащиеся в сообщении.</span><span class="sxs-lookup"><span data-stu-id="db423-120">Call [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to decrypt the data contained in the message.</span></span>

<span data-ttu-id="db423-121">[Пример программы на языке C. Использование криптенкриптмессаже и криптдекриптмессаже](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) реализует только что представленную процедуру.</span><span class="sxs-lookup"><span data-stu-id="db423-121">[Example C Program: Using CryptEncryptMessage and CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implements the procedure just presented.</span></span> <span data-ttu-id="db423-122">Комментарии показывают, какие элементы кода выполняют каждый шаг в процедуре.</span><span class="sxs-lookup"><span data-stu-id="db423-122">Comments show which code elements accomplish each step in the procedure.</span></span> <span data-ttu-id="db423-123">Дополнительные сведения о функции см. в разделе [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage), а дополнительные сведения о структуре данных см. в разделе [**\_ Шифрование расшифровки сообщения с помощью \_ \_ абзаца**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span><span class="sxs-lookup"><span data-stu-id="db423-123">For details about the function, see [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage), and for details about the data structure, see [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span></span>

 

 



