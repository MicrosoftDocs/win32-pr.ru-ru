---
description: Описывает действия по шифрованию сообщения с использованием базовых криптографических функций.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Шифрование данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44db44db08268241e399107d8af4088dac3c0c2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562867"
---
# <a name="encrypting-data"></a><span data-ttu-id="f711b-103">Шифрование данных</span><span class="sxs-lookup"><span data-stu-id="f711b-103">Encrypting Data</span></span>

<span data-ttu-id="f711b-104">В следующей процедуре описываются действия, которые необходимо выполнить для шифрования сообщения с использованием базовых криптографических функций.</span><span class="sxs-lookup"><span data-stu-id="f711b-104">The following procedure describes steps to take to encrypt a message with the Base Cryptography Functions.</span></span> <span data-ttu-id="f711b-105">Для шифрования сообщений с использованием \# стандартов PKCS 7 см. раздел [низкоуровневые функции сообщений](cryptography-functions.md) и [упрощенные функции сообщений](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f711b-105">To encrypt messages using PKCS \#7 standards, see [Low-level Message Functions](cryptography-functions.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="f711b-106">**Шифрование сообщения**</span><span class="sxs-lookup"><span data-stu-id="f711b-106">**To encrypt a message**</span></span>

1.  <span data-ttu-id="f711b-107">Создайте сеансовый ключ с помощью функции [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="f711b-107">Generate a session key by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>

    <span data-ttu-id="f711b-108">При выполнении этого вызова создается случайный ключ и возвращается маркер, чтобы ключ можно было использовать для шифрования и расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="f711b-108">Making this call generates a random key and returns a handle so the key can be used to encrypt and decrypt data.</span></span> <span data-ttu-id="f711b-109">На этом этапе также указывается используемый алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="f711b-109">The encryption algorithm to use is also specified at this point.</span></span> <span data-ttu-id="f711b-110">Поскольку интерфейс CryptoAPI не позволяет приложениям использовать алгоритмы открытого ключа для шифрования данных большого объема, укажите симметричный алгоритм, например RC2 или RC4, с помощью вызова [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="f711b-110">Because CryptoAPI does not permit applications to use public key algorithms to encrypt bulk data, specify a symmetric algorithm such as RC2 or RC4 with the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) call.</span></span>

2.  <span data-ttu-id="f711b-111">Кроме того, можно использовать функцию [**криптдеривекэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) для преобразования пароля в ключ, подходящий для шифрования.</span><span class="sxs-lookup"><span data-stu-id="f711b-111">Alternatively, use the [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) function to transform a password into a key suitable for encryption.</span></span>

    <span data-ttu-id="f711b-112">Если приложению необходимо зашифровать сообщение, чтобы любой пользователь с указанным паролем мог расшифровать данные, используйте [**криптдеривекэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) для преобразования пароля в ключ, подходящий для шифрования.</span><span class="sxs-lookup"><span data-stu-id="f711b-112">If an application needs to encrypt the message so that anyone with a specified password can decrypt the data, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) to transform the password into a key suitable for encryption.</span></span>

    > [!Note]  
    > <span data-ttu-id="f711b-113">В этом случае эта функция вызывается вместо функции [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , а последующие вызовы [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) не требуются.</span><span class="sxs-lookup"><span data-stu-id="f711b-113">In this case, this function is called instead of the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function and the subsequent [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls are not needed.</span></span>

     

3.  <span data-ttu-id="f711b-114">При необходимости задайте дополнительные криптографические свойства ключа с помощью функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) .</span><span class="sxs-lookup"><span data-stu-id="f711b-114">If necessary, set extra cryptographic properties of the key by using the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function</span></span>

    <span data-ttu-id="f711b-115">После создания ключа дополнительные криптографические свойства ключа можно задать с помощью функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="f711b-115">After the key has been generated, extra cryptographic properties of the key can be set with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)function.</span></span> <span data-ttu-id="f711b-116">Эта функция позволяет шифровать разные разделы файла с другими ключевыми Salt-файлами и предоставляет способ изменения режима шифрования или вектора инициализации ключа.</span><span class="sxs-lookup"><span data-stu-id="f711b-116">This function allows different sections of the file to be encrypted with different key salts and provides a way to change the cipher mode or initialization vector of the key.</span></span> <span data-ttu-id="f711b-117">Эти параметры можно использовать для обеспечения соответствия шифрования определенному стандарту шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="f711b-117">These parameters can be used to make the encryption conform with a particular data encryption standard.</span></span>

4.  <span data-ttu-id="f711b-118">Зашифруйте данные в файле с помощью функции [**криптенкрипт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="f711b-118">Encrypt the data in the file with the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function.</span></span>

    <span data-ttu-id="f711b-119">Функция [**криптенкрипт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) принимает сеансовый ключ, созданный на предыдущем шаге, и шифрует буфер данных.</span><span class="sxs-lookup"><span data-stu-id="f711b-119">The [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function takes the session key that was generated in the previous step and encrypts a buffer of data.</span></span>

    > [!Note]  
    > <span data-ttu-id="f711b-120">При шифровании данных данные могут быть немного расширены алгоритмом шифрования.</span><span class="sxs-lookup"><span data-stu-id="f711b-120">As the data is encrypted, the data may be slightly expanded by the encryption algorithm.</span></span> <span data-ttu-id="f711b-121">Приложение отвечает за запоминание длины зашифрованных данных, чтобы впоследствии можно было указать правильную длину для функции [**криптдекрипт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="f711b-121">The application is responsible for remembering the length of the encrypted data so the proper length can later be specified for the [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span>

     

5.  <span data-ttu-id="f711b-122">При необходимости используйте функцию [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , чтобы разрешить текущему пользователю расшифровывать данные в будущем.</span><span class="sxs-lookup"><span data-stu-id="f711b-122">Optionally, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function to allow the current user to decrypt the data in the future.</span></span>

    <span data-ttu-id="f711b-123">Чтобы разрешить текущему пользователю расшифровывать данные в будущем, функция [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) используется для сохранения ключа дешифрования в зашифрованном виде (BLOB-объект ключа), который можно расшифровать только с помощью закрытого ключа пользователя.</span><span class="sxs-lookup"><span data-stu-id="f711b-123">To allow the current user to decrypt the data in the future, the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function is used to save the decryption key in an encrypted form (a key BLOB) that can only be decrypted with the user's private key.</span></span> <span data-ttu-id="f711b-124">Для этой функции требуется открытый ключ обмена ключами пользователя для этой цели, который можно получить с помощью функции [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) .</span><span class="sxs-lookup"><span data-stu-id="f711b-124">This function requires the user's key exchange public key for this purpose, which can be obtained by using the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function.</span></span> <span data-ttu-id="f711b-125">Функция **криптекспорткэй** вернет большой двоичный объект ключа, который должен храниться в приложении для использования при расшифровке файла.</span><span class="sxs-lookup"><span data-stu-id="f711b-125">The **CryptExportKey** function will return a key BLOB that must be stored by the application for use in decrypting the file</span></span>

> [!Note]  
> <span data-ttu-id="f711b-126">Если приложение имеет сертификаты (или открытые ключи) для других пользователей, оно может Разрешите другим пользователям расшифровать файл, выполнив вызовы [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) для каждого пользователя, который должен получить доступ.</span><span class="sxs-lookup"><span data-stu-id="f711b-126">If the application has certificates (or public keys) for other users, it can permit other users to decrypt the file by performing [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls for each user who should receive access.</span></span> <span data-ttu-id="f711b-127">Возвращаемые ключевые большие двоичные объекты должны храниться в приложении, как показано на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="f711b-127">The returned key BLOBs must be stored by the application, as in step 5.</span></span>

 

## <a name="creating-an-encrypted-message"></a><span data-ttu-id="f711b-128">Создание зашифрованного сообщения</span><span class="sxs-lookup"><span data-stu-id="f711b-128">Creating an Encrypted Message</span></span>

<span data-ttu-id="f711b-129">Упрощенные функции сообщений упрощают шифрование и расшифровку данных.</span><span class="sxs-lookup"><span data-stu-id="f711b-129">The simplified message functions make it easier to encrypt and decrypt data.</span></span> <span data-ttu-id="f711b-130">На следующем рисунке показаны отдельные задачи, которые необходимо выполнить для шифрования сообщения.</span><span class="sxs-lookup"><span data-stu-id="f711b-130">The following illustration depicts the individual tasks that must be accomplished to encrypt a message.</span></span> <span data-ttu-id="f711b-131">Шаги описаны в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="f711b-131">The steps are described in the following list.</span></span>

![Шифрование сообщения](images/encmsg.png)

<span data-ttu-id="f711b-133">**Шифрование сообщения**</span><span class="sxs-lookup"><span data-stu-id="f711b-133">**To encrypt a message**</span></span>

1.  <span data-ttu-id="f711b-134">Возвращает указатель на сообщение с открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="f711b-134">Get a pointer to the plaintext message.</span></span>
2.  <span data-ttu-id="f711b-135">Создание симметричного ключа (сеанса).</span><span class="sxs-lookup"><span data-stu-id="f711b-135">Generate a symmetric (session) key.</span></span>
3.  <span data-ttu-id="f711b-136">Шифрование данных сообщения с помощью симметричного ключа и указанного алгоритма шифрования.</span><span class="sxs-lookup"><span data-stu-id="f711b-136">Using the symmetric key and specified encryption algorithm, encrypt the message data.</span></span>
4.  <span data-ttu-id="f711b-137">Откройте хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="f711b-137">Open a certificate store.</span></span>
5.  <span data-ttu-id="f711b-138">Получение сертификата получателя.</span><span class="sxs-lookup"><span data-stu-id="f711b-138">Get the recipient's certificate.</span></span>
6.  <span data-ttu-id="f711b-139">Получите открытый ключ из сертификата получателя.</span><span class="sxs-lookup"><span data-stu-id="f711b-139">Get the public key from the recipient's certificate.</span></span>
7.  <span data-ttu-id="f711b-140">С помощью открытого ключа получателя зашифруйте симметричный ключ.</span><span class="sxs-lookup"><span data-stu-id="f711b-140">Using the recipient's public key, encrypt the symmetric key.</span></span>
8.  <span data-ttu-id="f711b-141">Получите идентификатор получателя из сертификата получателя.</span><span class="sxs-lookup"><span data-stu-id="f711b-141">Get the recipient's identifier from the recipient's certificate.</span></span>
9.  <span data-ttu-id="f711b-142">Включите в сообщение с цифровой подписью следующие сведения: алгоритм шифрования данных, зашифрованные данные, зашифрованный симметричный ключ и идентификатор получателя.</span><span class="sxs-lookup"><span data-stu-id="f711b-142">Include the following in the digitally enveloped message: the data encryption algorithm, the encrypted data, the encrypted symmetric key, and the recipient identifier.</span></span>

 

 



