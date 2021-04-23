---
description: В следующем примере сообщение подписывается с помощью закрытого ключа отправителя и шифрует подписанное сообщение с помощью открытого ключа получателя.
ms.assetid: f2863e4a-d22a-4ff0-91d8-052eeaade14e
title: 'Пример программы на языке C: отправка и получение подписанного и зашифрованного сообщения'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c2ce7c5ba04d6fb57afbb0c15e32c115dcbd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911596"
---
# <a name="example-c-program-sending-and-receiving-a-signed-and-encrypted-message"></a><span data-ttu-id="dd942-103">Пример программы на языке C: отправка и получение подписанного и зашифрованного сообщения</span><span class="sxs-lookup"><span data-stu-id="dd942-103">Example C Program: Sending and Receiving a Signed and Encrypted Message</span></span>

<span data-ttu-id="dd942-104">В следующем примере сообщение подписывается с помощью [*закрытого ключа*](../secgloss/p-gly.md) отправителя и шифрует подписанное сообщение с помощью [*открытого ключа*](../secgloss/p-gly.md)получателя.</span><span class="sxs-lookup"><span data-stu-id="dd942-104">The following example signs a message using a sender's [*private key*](../secgloss/p-gly.md) and encrypts the signed message using a receiver's [*public key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="dd942-105">Затем в примере расшифровывается сообщение с помощью закрытого ключа получателя и проверяется подпись с помощью открытого ключа отправителя.</span><span class="sxs-lookup"><span data-stu-id="dd942-105">The example then decrypts the message using the receiver's private key and verifies the signature using the sender's public key.</span></span> <span data-ttu-id="dd942-106">Сертификат отправителя, содержащий необходимый открытый ключ, включается в зашифрованное сообщение.</span><span class="sxs-lookup"><span data-stu-id="dd942-106">The sender's certificate containing the needed public key is included in the encrypted message.</span></span> <span data-ttu-id="dd942-107">В этом примере также записывается подписанное и зашифрованное сообщение в файл.</span><span class="sxs-lookup"><span data-stu-id="dd942-107">This example also writes the signed and encrypted message to a file.</span></span> <span data-ttu-id="dd942-108">Дополнительные сведения см. в разделе [Пример программы C: получение подписанного и зашифрованного сообщения](example-c-program-receiving-a-signed-and-encrypted-message.md).</span><span class="sxs-lookup"><span data-stu-id="dd942-108">For more information, see [Example C Program: Receiving a Signed and Encrypted Message](example-c-program-receiving-a-signed-and-encrypted-message.md).</span></span>

<span data-ttu-id="dd942-109">Чтобы подписать сообщение, должен быть доступен закрытый ключ и сертификат подписавший.</span><span class="sxs-lookup"><span data-stu-id="dd942-109">To sign the message, the signer's private key and the signer's certificate must be available.</span></span> <span data-ttu-id="dd942-110">Чтобы зашифровать подписанное сообщение, должен быть доступен сертификат получателя, включая открытый ключ получателя.</span><span class="sxs-lookup"><span data-stu-id="dd942-110">To encrypt the signed message, a receiver's certificate including the receiver's public key must be available.</span></span>

<span data-ttu-id="dd942-111">Для расшифровки сообщения закрытый ключ получателя должен быть доступен.</span><span class="sxs-lookup"><span data-stu-id="dd942-111">To decrypt the message, the receiver's private key must be available.</span></span> <span data-ttu-id="dd942-112">После расшифровки сообщения подпись проверяется с помощью открытого ключа из сертификата, включенного в зашифрованное сообщение.</span><span class="sxs-lookup"><span data-stu-id="dd942-112">After the message is decrypted, the signature is verified using the public key from the certificate included in the encrypted message.</span></span>

> [!Note]  
> <span data-ttu-id="dd942-113">Не все сертификаты в [*хранилище сертификатов*](../secgloss/c-gly.md) предоставляют доступ к [*закрытому ключу*](../secgloss/p-gly.md) , связанному с этим сертификатом.</span><span class="sxs-lookup"><span data-stu-id="dd942-113">Not all of the certificates in a [*certificate store*](../secgloss/c-gly.md) provide access to the [*private key*](../secgloss/p-gly.md) associated with that certificate.</span></span> <span data-ttu-id="dd942-114">Когда сообщение подписывается и шифруется, необходимо использовать сертификат, принадлежащий подписавшего, с доступом к закрытому ключу этого подписавшего.</span><span class="sxs-lookup"><span data-stu-id="dd942-114">When the message is signed and encrypted, a certificate belonging to the signer with access to the private key of that signer must be used.</span></span> <span data-ttu-id="dd942-115">Кроме того, получатель сообщения должен иметь доступ к закрытому ключу, связанному с открытым ключом, используемым для шифрования сообщения.</span><span class="sxs-lookup"><span data-stu-id="dd942-115">In addition, the receiver of the message must have access to the private key associated with the public key used to encrypt the message.</span></span>

 

<span data-ttu-id="dd942-116">В этом примере показаны следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="dd942-116">This example illustrates the following tasks:</span></span>

-   <span data-ttu-id="dd942-117">Открытие и закрытие хранилищ сертификатов системы.</span><span class="sxs-lookup"><span data-stu-id="dd942-117">Opening and closing system certificate stores.</span></span>
-   <span data-ttu-id="dd942-118">Поиск сертификатов для отправителя и получателя сообщений в открытых хранилищах сертификатов.</span><span class="sxs-lookup"><span data-stu-id="dd942-118">Finding certificates for a message sender and message receiver in the open certificate stores.</span></span>
-   <span data-ttu-id="dd942-119">Поиск и печать имени субъекта из сертификатов.</span><span class="sxs-lookup"><span data-stu-id="dd942-119">Finding and printing the subject name from certificates.</span></span>
-   <span data-ttu-id="dd942-120">Инициализация структур данных, необходимых для подписания, шифрования, расшифровки и проверки сообщения.</span><span class="sxs-lookup"><span data-stu-id="dd942-120">Initializing data structures needed to sign, encrypt, decrypt, and verify a message.</span></span>
-   <span data-ttu-id="dd942-121">Вызов функции CryptoAPI для поиска требуемого размера буфера, выделения буфера требуемого размера и повторного вызова функции CryptoAPI для заполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="dd942-121">Calling a CryptoAPI function to find the required size of a buffer, allocating the buffer of the required size, and calling the CryptoAPI function again to fill the buffer.</span></span> <span data-ttu-id="dd942-122">Дополнительные сведения см. в разделе [Получение данных неизвестной длины](retrieving-data-of-unknown-length.md).</span><span class="sxs-lookup"><span data-stu-id="dd942-122">For more information, see [Retrieving Data of Unknown Length](retrieving-data-of-unknown-length.md).</span></span>
-   <span data-ttu-id="dd942-123">Отображение некоторых зашифрованных содержимого буфера.</span><span class="sxs-lookup"><span data-stu-id="dd942-123">Displaying some of the encrypted contents of a buffer.</span></span> <span data-ttu-id="dd942-124">Добавленная локальная функция **шовбитес** отображает символы в буфере со значениями от 0 до z.</span><span class="sxs-lookup"><span data-stu-id="dd942-124">The included local function, **ShowBytes**, displays characters in the buffer with values between '0' and 'z'.</span></span> <span data-ttu-id="dd942-125">Все остальные символы отображаются как символ "-".</span><span class="sxs-lookup"><span data-stu-id="dd942-125">All other characters are displayed as the '-' character.</span></span>

<span data-ttu-id="dd942-126">В этом примере используются следующие функции CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="dd942-126">This example uses the following CryptoAPI functions:</span></span>

-   [<span data-ttu-id="dd942-127">**цертопенсторе**</span><span class="sxs-lookup"><span data-stu-id="dd942-127">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)
-   [<span data-ttu-id="dd942-128">**цертфиндцертификатеинсторе**</span><span class="sxs-lookup"><span data-stu-id="dd942-128">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
-   [<span data-ttu-id="dd942-129">**цертжетнаместринг**</span><span class="sxs-lookup"><span data-stu-id="dd942-129">**CertGetNameString**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)
-   [<span data-ttu-id="dd942-130">**криптаккуирецертификатеприватекэй**</span><span class="sxs-lookup"><span data-stu-id="dd942-130">**CryptAcquireCertificatePrivateKey**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey)
-   [<span data-ttu-id="dd942-131">**криптсигнанденкриптмессаже**</span><span class="sxs-lookup"><span data-stu-id="dd942-131">**CryptSignAndEncryptMessage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)
-   [<span data-ttu-id="dd942-132">**криптдекриптандверифимессажесигнатуре**</span><span class="sxs-lookup"><span data-stu-id="dd942-132">**CryptDecryptAndVerifyMessageSignature**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature)
-   [<span data-ttu-id="dd942-133">**цертфрицертификатеконтекст**</span><span class="sxs-lookup"><span data-stu-id="dd942-133">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)
-   [<span data-ttu-id="dd942-134">**цертклосесторе**</span><span class="sxs-lookup"><span data-stu-id="dd942-134">**CertCloseStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

<span data-ttu-id="dd942-135">В этом примере используются отдельные функции для отображения процесса подписывания и шифрования, а также процесса расшифровки и проверки подписи.</span><span class="sxs-lookup"><span data-stu-id="dd942-135">This example uses separate functions to show the signing/encryption process and the decryption/signature-verification process.</span></span> <span data-ttu-id="dd942-136">Он также использует [**михандлиррор**](myhandleerror.md) для корректного выхода из программы в случае любого сбоя.</span><span class="sxs-lookup"><span data-stu-id="dd942-136">It also uses [**MyHandleError**](myhandleerror.md) to exit the program gracefully in case of any failure.</span></span> <span data-ttu-id="dd942-137">Код **михандлиррор** включен в пример, и его также можно найти вместе с другими вспомогательными функциями в разделе [функции общего назначения](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="dd942-137">The code **MyHandleError** is included with the example and can also be found along with other auxiliary functions under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
// Example C Program: 
// Signs a message by using a sender's private key and encrypts the
// signed message by using a receiver's public key.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
#define MAX_NAME  128

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// SIGNER_NAME is used with the CertFindCertificateInStore  
// function to retrieve the certificate of the message signer.
// Replace the Unicode string below with the certificate subject 
// name of the message signer.

#define SIGNER_NAME L"DUMMY_SIGNER_NAME"

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the standard  
//  error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

//-------------------------------------------------------------------
// The local function ShowBytes is declared here and defined after 
// main.

void ShowBytes(BYTE *s, DWORD len);

//-------------------------------------------------------------------
// Declare local functions SignAndEncrypt, DecryptAndVerify, and 
// WriteSignedAndEncryptedBlob.
// These functions are defined after main.

BYTE* SignAndEncrypt(
     const BYTE     *pbToBeSignedAndEncrypted,
     DWORD          cbToBeSignedAndEncrypted,
     DWORD          *pcbSignedAndEncryptedBlob);

BYTE* DecryptAndVerify(
     BYTE  *pbSignedAndEncryptedBlob,
     DWORD  cbSignedAndEncryptedBlob);

void WriteSignedAndEncryptedBlob(
     DWORD  cbBlob,
     BYTE   *pbBlob);

void main (void)
{
    //---------------------------------------------------------------
    // Declare and initialize local variables.

    //---------------------------------------------------------------
    //  pbToBeSignedAndEncrypted is the message to be 
    //  encrypted and signed.

    const BYTE *pbToBeSignedAndEncrypted =
            (const unsigned char *)"Insert the message to be signed "
            "here";
    //---------------------------------------------------------------
    // This is the length of the message to be
    // encrypted and signed. Note that it is one
    // more that the length returned by strlen()
    // to include the terminating null character.

    DWORD cbToBeSignedAndEncrypted = 
        lstrlenA((const char *)pbToBeSignedAndEncrypted) + 1;

    //---------------------------------------------------------------
    // Pointer to a buffer that will hold the
    // encrypted and signed message.

    BYTE *pbSignedAndEncryptedBlob;

    //---------------------------------------------------------------
    // A DWORD to hold the length of the signed 
    // and encrypted message.

    DWORD cbSignedAndEncryptedBlob;
    BYTE *pReturnMessage;

    //---------------------------------------------------------------
    // Call the local function SignAndEncrypt.
    // This function returns a pointer to the 
    // signed and encrypted BLOB and also returns
    // the length of that BLOB.

    pbSignedAndEncryptedBlob = SignAndEncrypt(
        pbToBeSignedAndEncrypted,
        cbToBeSignedAndEncrypted,
        &cbSignedAndEncryptedBlob);

    _tprintf(TEXT("The following is the signed and encrypted ")
        TEXT("message.\n"));
    ShowBytes(pbSignedAndEncryptedBlob,cbSignedAndEncryptedBlob/4);

    // Open a file and write the signed and 
    // encrypted message to the file.

    WriteSignedAndEncryptedBlob(
        cbSignedAndEncryptedBlob,
        pbSignedAndEncryptedBlob);

    //---------------------------------------------------------------
    // Call the local function DecryptAndVerify.
    // This function decrypts and displays the 
    // encrypted message and also verifies the 
    // message's signature.
       
    if(pReturnMessage = DecryptAndVerify(
        pbSignedAndEncryptedBlob,
        cbSignedAndEncryptedBlob))
    {
        _tprintf(TEXT(" The returned, verified message is ->\n%s\n"),
            pReturnMessage);
        _tprintf(TEXT(" The program executed without error.\n"));
    }
    else
    {
        _tprintf(TEXT("Verification failed.\n"));
    }

} // End Main.

//-------------------------------------------------------------------
// Begin definition of the SignAndEncrypt function.

BYTE* SignAndEncrypt(
     const BYTE *pbToBeSignedAndEncrypted,
     DWORD cbToBeSignedAndEncrypted,
     DWORD *pcbSignedAndEncryptedBlob)
{
    //---------------------------------------------------------------
    // Declare and initialize local variables.

    FILE *hToSave;
    HCERTSTORE hCertStore;

    //---------------------------------------------------------------
    // pSignerCertContext will be the certificate of 
    // the message signer.

    PCCERT_CONTEXT pSignerCertContext ;

    //---------------------------------------------------------------
    // pReceiverCertContext will be the certificate of the 
    // message receiver.

    PCCERT_CONTEXT pReceiverCertContext;

    TCHAR pszNameString[256];
    CRYPT_SIGN_MESSAGE_PARA SignPara;
    CRYPT_ENCRYPT_MESSAGE_PARA EncryptPara;
    DWORD cRecipientCert;
    PCCERT_CONTEXT rgpRecipientCert[5];
    BYTE *pbSignedAndEncryptedBlob = NULL;
    CERT_NAME_BLOB Subject_Blob;
    BYTE *pbDataIn;
    DWORD dwKeySpec;
    HCRYPTPROV hCryptProv;

    //---------------------------------------------------------------
    // Open the MY certificate store. 
    // For more information, see the CertOpenStore function 
    // PSDK reference page. 
    // Note: Case is not significant in certificate store names.

    if ( !( hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"my")))
    {
        MyHandleError(TEXT("The MY store could not be opened."));
    }

    //---------------------------------------------------------------
    // Get the certificate for the signer.

    if(!(pSignerCertContext = CertFindCertificateInStore(
        hCertStore,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_STR,
        SIGNER_NAME,
        NULL)))
    {
        MyHandleError(TEXT("Cert not found.\n"));
    }

    //---------------------------------------------------------------
    // Get and print the name of the message signer.
    // The following two calls to CertGetNameString with different
    // values for the second parameter get two different forms of 
    // the certificate subject's name.

    if(CertGetNameString(
        pSignerCertContext ,
        CERT_NAME_SIMPLE_DISPLAY_TYPE,
        0,
        NULL,
        pszNameString,
        MAX_NAME) > 1)
    {
        _tprintf(
            TEXT("The SIMPLE_DISPLAY_TYPE message signer's name is ")
            TEXT("%s \n"),
            pszNameString);
    }
    else
    {
        MyHandleError(
            TEXT("Getting the name of the signer failed.\n"));
    }

    if(CertGetNameString(
        pSignerCertContext,
        CERT_NAME_RDN_TYPE,
        0,
        NULL,
        pszNameString,
        MAX_NAME) > 1)
    {
        _tprintf(
            TEXT("The RDM_TYPE message signer's name is %s \n"),
            pszNameString);
    }
    else
    {
        MyHandleError(
            TEXT("Getting the name of the signer failed.\n"));
    }

    if(!( CryptAcquireCertificatePrivateKey(
        pSignerCertContext,
        0,
        NULL,
        &hCryptProv,
        &dwKeySpec,
        NULL)))
    {
        MyHandleError(TEXT("CryptAcquireCertificatePrivateKey.\n"));
    }

    //---------------------------------------------------------------
    // Get the certificate for the receiver. In this case,  
    // a BLOB with the name of the receiver is saved in a file.

    // Note: To decrypt the message signed and encrypted here,
    // this program must use the certificate of the intended
    // receiver. The signed and encrypted message can only be
    // decrypted and verified by the owner of the recipient
    // certificate. That user must have access to the private key
    // associated with the public key of the recipient's certificate.

    // To run this sample, the file contains information that allows 
    // the program to find one of the current user's certificates. 
    // The current user should have access to the private key of the
    // certificate and thus can test the verification and decryption. 

    // In normal use, the file would contain information used to find
    // the certificate of an intended receiver of the message. 
    // The signed and encrypted message would be written
    // to a file or otherwise sent to the intended receiver.

    //---------------------------------------------------------------
    // Open a file and read in the receiver name
    // BLOB.


    if( !(hToSave= fopen("s.txt","rb")))
    {
        MyHandleError(TEXT("Source file was not opened.\n"));
    }

    fread(
        &(Subject_Blob.cbData),
        sizeof(DWORD),
        1,
        hToSave);

    if(ferror(hToSave))
    {
        MyHandleError(TEXT("The size of the BLOB was not read.\n"));
    }

    if(!(pbDataIn = (BYTE *) malloc(Subject_Blob.cbData)))
    {
        MyHandleError(TEXT("Memory allocation error."));
    }

    fread(
        pbDataIn,
        Subject_Blob.cbData,
        1,
        hToSave);

    if(ferror(hToSave))
    {
        MyHandleError(TEXT("BLOB not read."));
    }

    fclose(hToSave);

    Subject_Blob.pbData = pbDataIn;

    //---------------------------------------------------------------
    // Use the BLOB just read in from the file to find its associated
    // certificate in the MY store.
    // This call to CertFindCertificateInStore uses the
    // CERT_FIND_SUBJECT_NAME dwFindType.

    if(!(pReceiverCertContext = CertFindCertificateInStore(
        hCertStore,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_NAME,
        &Subject_Blob,
        NULL)))
    {
        MyHandleError(TEXT("Receiver certificate not found."));
    }

    //---------------------------------------------------------------
    // Get and print the subject name from the receiver's
    // certificate.

    if(CertGetNameString(
        pReceiverCertContext ,
        CERT_NAME_SIMPLE_DISPLAY_TYPE,
        0,
        NULL,
        pszNameString,
        MAX_NAME) > 1)
    {
        _tprintf(TEXT("The message receiver is  %s \n"), 
            pszNameString);
    }
    else
    {
        MyHandleError(
            TEXT("Getting the name of the receiver failed.\n"));
    }

    //---------------------------------------------------------------
    // Initialize variables and data structures
    // for the call to CryptSignAndEncryptMessage.

    SignPara.cbSize = sizeof(CRYPT_SIGN_MESSAGE_PARA);
    SignPara.dwMsgEncodingType = MY_ENCODING_TYPE;
    SignPara.pSigningCert = pSignerCertContext ;
    SignPara.HashAlgorithm.pszObjId = szOID_RSA_MD2;
    SignPara.HashAlgorithm.Parameters.cbData = 0;
    SignPara.pvHashAuxInfo = NULL;
    SignPara.cMsgCert = 1;
    SignPara.rgpMsgCert = &pSignerCertContext ;
    SignPara.cMsgCrl = 0;
    SignPara.rgpMsgCrl = NULL;
    SignPara.cAuthAttr = 0;
    SignPara.rgAuthAttr = NULL;
    SignPara.cUnauthAttr = 0;
    SignPara.rgUnauthAttr = NULL;
    SignPara.dwFlags = 0;
    SignPara.dwInnerContentType = 0;

    EncryptPara.cbSize = sizeof(CRYPT_ENCRYPT_MESSAGE_PARA);
    EncryptPara.dwMsgEncodingType = MY_ENCODING_TYPE;
    EncryptPara.hCryptProv = 0;
    EncryptPara.ContentEncryptionAlgorithm.pszObjId = szOID_RSA_RC4;
    EncryptPara.ContentEncryptionAlgorithm.Parameters.cbData = 0;
    EncryptPara.pvEncryptionAuxInfo = NULL;
    EncryptPara.dwFlags = 0;
    EncryptPara.dwInnerContentType = 0;

    cRecipientCert = 1;
    rgpRecipientCert[0] = pReceiverCertContext;
    *pcbSignedAndEncryptedBlob = 0;
    pbSignedAndEncryptedBlob = NULL;

    if( CryptSignAndEncryptMessage(
        &SignPara,
        &EncryptPara,
        cRecipientCert,
        rgpRecipientCert,
        pbToBeSignedAndEncrypted,
        cbToBeSignedAndEncrypted,
        NULL, // the pbSignedAndEncryptedBlob
        pcbSignedAndEncryptedBlob))
    {
        _tprintf(TEXT("%d bytes for the buffer .\n"),
            *pcbSignedAndEncryptedBlob);
    }
    else
    {
        MyHandleError(TEXT("Getting the buffer length failed."));
    }

    //---------------------------------------------------------------
    // Allocate memory for the buffer.

    if(!(pbSignedAndEncryptedBlob = 
        (unsigned char *)malloc(*pcbSignedAndEncryptedBlob)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    //---------------------------------------------------------------
    // Call the function a second time to copy the signed and 
    // encrypted message into the buffer.

    if( CryptSignAndEncryptMessage(
        &SignPara,
        &EncryptPara,
        cRecipientCert,
        rgpRecipientCert,
        pbToBeSignedAndEncrypted,
        cbToBeSignedAndEncrypted,
        pbSignedAndEncryptedBlob,
        pcbSignedAndEncryptedBlob))
    {
        _tprintf(TEXT("The message is signed and encrypted.\n"));
    }
    else
    {
        MyHandleError(
            TEXT("The message failed to sign and encrypt."));
    }

    //---------------------------------------------------------------
    // Clean up.

    if(pSignerCertContext )
    {
        CertFreeCertificateContext(pSignerCertContext);
    }
    
    if(pReceiverCertContext )
    {
        CertFreeCertificateContext(pReceiverCertContext);
    }
    
    CertCloseStore(hCertStore, 0);

    //---------------------------------------------------------------
    // Return the signed and encrypted message.

    return pbSignedAndEncryptedBlob;

}  // End SignAndEncrypt.

//-------------------------------------------------------------------
// Define the DecryptAndVerify function.

BYTE* DecryptAndVerify(
     BYTE  *pbSignedAndEncryptedBlob,
     DWORD  cbSignedAndEncryptedBlob)
{
    //---------------------------------------------------------------
    // Declare and initialize local variables.

    HCERTSTORE hCertStore;
    CRYPT_DECRYPT_MESSAGE_PARA DecryptPara;
    CRYPT_VERIFY_MESSAGE_PARA VerifyPara;
    DWORD dwSignerIndex = 0;
    BYTE *pbDecrypted;
    DWORD cbDecrypted;

    //---------------------------------------------------------------
    // Open the certificate store.

    if ( !( hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"my")))
    {
        MyHandleError(TEXT("The MY store could not be opened."));
    }

    //---------------------------------------------------------------
    // Initialize the needed data structures.

    DecryptPara.cbSize = sizeof(CRYPT_DECRYPT_MESSAGE_PARA);
    DecryptPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    DecryptPara.cCertStore = 1;
    DecryptPara.rghCertStore = &hCertStore;

    VerifyPara.cbSize = sizeof(CRYPT_VERIFY_MESSAGE_PARA);
    VerifyPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    VerifyPara.hCryptProv = 0;
    VerifyPara.pfnGetSignerCertificate = NULL;
    VerifyPara.pvGetArg = NULL;
    pbDecrypted = NULL;
    cbDecrypted = 0;

    //---------------------------------------------------------------
    // Call CryptDecryptAndVerifyMessageSignature a first time
    // to determine the needed size of the buffer to hold the 
    // decrypted message.

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbSignedAndEncryptedBlob,
        cbSignedAndEncryptedBlob,
        NULL,           // pbDecrypted
        &cbDecrypted,
        NULL,
        NULL)))
    {
        MyHandleError(TEXT("Failed getting size."));
    }

    //---------------------------------------------------------------
    // Allocate memory for the buffer to hold the decrypted
    // message.

    if(!(pbDecrypted = (BYTE *)malloc(cbDecrypted)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbSignedAndEncryptedBlob,
        cbSignedAndEncryptedBlob,
        pbDecrypted,
        &cbDecrypted,
        NULL,
        NULL)))
    {
        pbDecrypted = NULL;
    }

    //---------------------------------------------------------------
    // Close the certificate store.

    CertCloseStore(
        hCertStore,
        0);

    //---------------------------------------------------------------
    // Return the decrypted string or NULL.

    return pbDecrypted;

} // End of DecryptandVerify.

//-------------------------------------------------------------------
// Define the MyHandleError function.

void WriteSignedAndEncryptedBlob(
     DWORD cbBlob,
     BYTE *pbBlob)
{
    // Open an output file, write the file, and close the file.
    // This function would be used to save the signed and encrypted 
    // message to a file that would be sent to the intended receiver.
    // Note: The only receiver able to decrypt and verify this
    // message will have access to the private key associated 
    // with the public key from the certificate used when 
    // the message was encrypted.

    FILE *hOutputFile;

    if( !(hOutputFile = _tfopen(TEXT("sandvout.txt"), TEXT("wb"))))
    {
        MyHandleError(TEXT("Output file was not opened.\n"));
    }

    fwrite(
        &cbBlob,
        sizeof(DWORD),
        1,
        hOutputFile);

    if(ferror(hOutputFile))
    {
        MyHandleError(
            TEXT("The size of the BLOB was not written.\n"));
    }

    fwrite(
        pbBlob,
        cbBlob,
        1,
        hOutputFile);

    if(ferror(hOutputFile))
    {
        MyHandleError(
            TEXT("The bytes of the BLOB were not written.\n"));
    }
    else
    {
        _tprintf(TEXT("The BLOB has been written to the file.\n"));
    }
    
    fclose(hOutputFile);
}  // End of WriteSignedAndEcryptedBlob.


//-------------------------------------------------------------------
// Define the ShowBytes function.
// This function displays the contents of a BYTE buffer. Characters
// less than '0' or greater than 'z' are all displayed as '-'.

void ShowBytes(BYTE *s, DWORD len)
{
    DWORD TotalChars = 0;
    DWORD ThisLine = 0;

    while(TotalChars < len)
    {
        if(ThisLine > 70)
        {
            ThisLine = 0;
            _tprintf(TEXT("\n"));
        }
        if( s[TotalChars] < '0' || s[TotalChars] > 'z')
        {
            _tprintf(TEXT("-"));
        }
        else
        {
            _tprintf(TEXT("%c"), s[TotalChars]);
        }

        TotalChars++;
        ThisLine++;
    }

    _tprintf(TEXT("\n"));
} // End of ShowBytes.

```



 

 
