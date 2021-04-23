---
description: Следующий пример сочетает подписывание и кодирование сообщения и декодирование подписанного сообщения и проверку подписи.
ms.assetid: 2cad11a8-75ad-4726-a7bb-82870b71c721
title: 'Пример программы на языке C: подписывание, кодирование, декодирование и проверка сообщения'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128b4368a75d5f7636394fdf9a3b1b2694f45176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810259"
---
# <a name="example-c-program-signing-encoding-decoding-and-verifying-a-message"></a><span data-ttu-id="2ad13-103">Пример программы на языке C: подписывание, кодирование, декодирование и проверка сообщения</span><span class="sxs-lookup"><span data-stu-id="2ad13-103">Example C Program: Signing, Encoding, Decoding, and Verifying a Message</span></span>

<span data-ttu-id="2ad13-104">Следующий пример сочетает подписывание и кодирование сообщения и декодирование подписанного сообщения и проверку подписи.</span><span class="sxs-lookup"><span data-stu-id="2ad13-104">The following example combines signing and encoding a message, and decoding a signed message and verifying the signature.</span></span> <span data-ttu-id="2ad13-105">Эти две операции обычно находятся в отдельных программах.</span><span class="sxs-lookup"><span data-stu-id="2ad13-105">The two operations would usually be in separate programs.</span></span> <span data-ttu-id="2ad13-106">В примере кодировки можно создать закодированное сообщение, сохранить его в файл на диске или каким-либо другим способом отправить его другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="2ad13-106">The encoding example would create the encoded message, save it to a disk file or in some other way send it to another user.</span></span> <span data-ttu-id="2ad13-107">Пример декодирования может получить закодированное сообщение, декодировать его и проверить подпись.</span><span class="sxs-lookup"><span data-stu-id="2ad13-107">The decoding example would receive the encoded message, decode it, and verify the signature.</span></span> <span data-ttu-id="2ad13-108">Эти два процесса объединены здесь, чтобы отобразить обе процедуры.</span><span class="sxs-lookup"><span data-stu-id="2ad13-108">The two processes have been combined here to show both procedures working.</span></span>

<span data-ttu-id="2ad13-109">Подписывание и кодирование сообщения не гарантирует конфиденциальности этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="2ad13-109">Signing and encoding a message does not ensure privacy for that message.</span></span> <span data-ttu-id="2ad13-110">Вместо этого он гарантирует подлинность сообщения.</span><span class="sxs-lookup"><span data-stu-id="2ad13-110">Rather it ensures the authenticity of the message.</span></span> <span data-ttu-id="2ad13-111">Поскольку сообщение подписано с помощью закрытого ключа отправителя, когда получатель сообщения расшифровывает подпись с помощью [*открытого ключа*](../secgloss/p-gly.md) отправителя (доступного из сертификата, который отправляется вместе с сообщением), получатель может убедиться, что сообщение было отправлено пользователем или объектом, связанным с сертификатом, и что сообщение не было изменено после того, как оно было подписано.</span><span class="sxs-lookup"><span data-stu-id="2ad13-111">Because the message is signed with the sender's private key, when the receiver of the message decrypts the signature with the sender's [*public key*](../secgloss/p-gly.md) (available from the certificate that is sent along with the message), the receiver can be sure that the message was sent by the person or entity associated with the certificate and that the message was not changed after it was signed.</span></span>

<span data-ttu-id="2ad13-112">В этом примере показаны следующие задачи и функции CryptoAPI для кодирования сообщения.</span><span class="sxs-lookup"><span data-stu-id="2ad13-112">This example illustrates the following tasks and CryptoAPI functions for encoding a message:</span></span>

-   <span data-ttu-id="2ad13-113">Открытие хранилища сертификатов с помощью [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="2ad13-113">Opening a certificate store using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
-   <span data-ttu-id="2ad13-114">Получение сертификата с указанным именем субъекта с помощью [**цертфиндцертификатеинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span><span class="sxs-lookup"><span data-stu-id="2ad13-114">Retrieving a certificate with a specific subject name using [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span></span>
-   <span data-ttu-id="2ad13-115">Получение и печать имени субъекта сертификата с помощью [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="2ad13-115">Getting and printing a certificate's subject name using [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>
-   <span data-ttu-id="2ad13-116">Инициализация структуры с [**\_ \_ сообщением \_ о знаке шифрования**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) , которая будет использоваться при вызове [**криптсигнмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span><span class="sxs-lookup"><span data-stu-id="2ad13-116">Initializing a [**CRYPT\_SIGN\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) structure to be used in a call to [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span>
-   <span data-ttu-id="2ad13-117">Подписывание и кодирование сообщения с помощью [**криптсигнмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span><span class="sxs-lookup"><span data-stu-id="2ad13-117">Signing and encoding a message with [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span>

<span data-ttu-id="2ad13-118">В этом примере показаны следующие задачи и функции CryptoAPI для декодирования сообщения и проверки подписи.</span><span class="sxs-lookup"><span data-stu-id="2ad13-118">This example illustrates the following tasks and CryptoAPI functions for decoding a message and verifying the signature:</span></span>

-   <span data-ttu-id="2ad13-119">Открытие сообщения для декодирования с помощью [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span><span class="sxs-lookup"><span data-stu-id="2ad13-119">Opening a message for decoding with [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span></span>
-   <span data-ttu-id="2ad13-120">Добавление закодированного [*BLOB-объекта*](../secgloss/b-gly.md) в сообщение для декодирования с помощью [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span><span class="sxs-lookup"><span data-stu-id="2ad13-120">Adding the encoded [*BLOB*](../secgloss/b-gly.md) to the message to be decoded by using [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span></span>
-   <span data-ttu-id="2ad13-121">Декодирование сообщения с помощью [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span><span class="sxs-lookup"><span data-stu-id="2ad13-121">Decoding the message using [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span></span>
-   <span data-ttu-id="2ad13-122">Открытие хранилища сертификатов в памяти с [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) , используя полученное и декодированное сообщение.</span><span class="sxs-lookup"><span data-stu-id="2ad13-122">Opening a certificate store in memory with [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) using the message received and decoded.</span></span>
-   <span data-ttu-id="2ad13-123">Использование [**цертжетсубжектцертификатефромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) для получения сертификата для подписания сообщения.</span><span class="sxs-lookup"><span data-stu-id="2ad13-123">Using [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) to get the certificate of the message's signer.</span></span>
-   <span data-ttu-id="2ad13-124">Проверка подписи сообщения с помощью [**криптмсгконтрол**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol).</span><span class="sxs-lookup"><span data-stu-id="2ad13-124">Verifying a message's signature using [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol).</span></span>
-   <span data-ttu-id="2ad13-125">Освобождение памяти, закрытие [*хранилищ сертификатов*](../secgloss/c-gly.md)и освобождение [*контекста сертификата*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2ad13-125">Freeing memory, closing [*certificate stores*](../secgloss/c-gly.md), and freeing [*certificate context*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="2ad13-126">Пример выполнения этих аналогичных операций с помощью обратного вызова потока см. в разделе [Пример программы C: кодирование и декодирование сообщения с помощью потока](example-c-program--encoding-and-decoding-a-message-using-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="2ad13-126">For an example of how to perform these similar operations using a stream callback, see [Example C Program: Encoding and Decoding a Message Using a Stream](example-c-program--encoding-and-decoding-a-message-using-a-stream.md).</span></span>

<span data-ttu-id="2ad13-127">В этом примере используется функция [**михандлиррор**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="2ad13-127">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="2ad13-128">Код для этой функции включен в пример.</span><span class="sxs-lookup"><span data-stu-id="2ad13-128">Code for this function is included with the sample.</span></span> <span data-ttu-id="2ad13-129">Код для этой и других вспомогательных функций также указан в [разделе \_ \_ функции общего назначения](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2ad13-129">Code for this and other auxiliary functions is also listed under [General\_Purpose\_Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Example of encoding and decoding a signed message.

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

#define MAX_NAME 256

#define CERTIFICATE_STORE_NAME L"MY"

//-------------------------------------------------------------------
//    Declare local functions.

//-------------------------------------------------------------------
BOOL EncodeMessage(PCRYPT_DATA_BLOB pEncodedData,
                   LPWSTR pwszSignerName);
void DecodeMessage(PCRYPT_DATA_BLOB pEncodedData,
                   LPWSTR pwszSignerName);

//  Define function MyHandleError.
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

void ReportFailure()
{
    switch (GetLastError())
    {
        case CRYPT_E_AUTH_ATTR_MISSING:
            printf("Message does not contain an expected "
                "attribute.\n");
            break;
        case CRYPT_E_BAD_ENCODE:
            printf("An error encountered encoding or decoding.\n");
            break;
        case CRYPT_E_HASH_VALUE:
            printf("The hash value is not correct.\n");
            break;
        case CRYPT_E_INVALID_MSG_TYPE:
            printf("The message type is not valid.\n");
            break;
        case CRYPT_E_OSS_ERROR:
            printf("OSS error.\n");
            break;
        case CRYPT_E_SIGNER_NOT_FOUND:
            printf("Signer not found.\n");
            break;
        case CRYPT_E_UNEXPECTED_ENCODING:
            printf("Unexpected encoding. \n");
            break;
        case CRYPT_E_UNKNOWN_ALGO:
            printf("Unknown algorithm.\n");
            break;
        case E_OUTOFMEMORY:
            printf("Out of memory.\n");
            break;
        case ERROR_INVALID_HANDLE:
            printf("The handle from verify signature is not valid." \
                "function.\n");
            break;
        case ERROR_INVALID_PARAMETER:
            printf("The parameter from verify signature "
                "is not valid.\n");
            break;
        case NTE_BAD_FLAGS:
            printf("Bad Flags from verify signature function.\n");
            break;
        case NTE_BAD_HASH:
            printf("Bad Hash from verify signature function.\n");
            break;
        case NTE_BAD_KEY:
            printf("Bad Key from verify signature function.\n");
            break;
        case NTE_BAD_SIGNATURE:
            printf("Bad signature from verify signature " \
                "function.\n");
            break;
        case NTE_BAD_UID:
            printf("Bad UID from verify signature function.\n");
            break;
    }  // End switch.
}  // End ReportFailure.

void EncodeAndDecodeMessage(LPWSTR pwszSignerName)
{
    CRYPT_DATA_BLOB EncodedBlob;

    if(EncodeMessage(&EncodedBlob, pwszSignerName))
    {
        DecodeMessage(&EncodedBlob, pwszSignerName);
    }
}

BOOL EncodeMessage(PCRYPT_DATA_BLOB pEncodedBlob,
                   LPWSTR pwszSignerName)
{
    /*---------------------------------------------------------------
        Declare and initialize variables. This includes getting a 
        pointer to the message content. This sample creates 
        the message content and gets a pointer to it. In most 
        situations, the content will exist somewhere, and a 
        pointer to it will get passed to the application. 
    ---------------------------------------------------------------*/

    HCERTSTORE hSystemStoreHandle;
    CRYPT_SIGN_MESSAGE_PARA SignMessagePara;

    //---------------------------------------------------------------
    //   The message to be signed and encoded.

    BYTE* pbContent = (BYTE*) "The quick brown fox jumped over " \
        "the lazy dog.";

    /*---------------------------------------------------------------
        The length of the message. This must be one more than the 
        value returned by strlen() to include the terminal NULL 
        character.
    ---------------------------------------------------------------*/
    DWORD cbContent = lstrlenA((char *) pbContent) + 1;

    //---------------------------------------------------------------
    //    Arrays to hold the message to be signed and its length.

    const BYTE *rgpbToBeSigned[1] ;
    DWORD rgcbToBeSigned[1];

    //---------------------------------------------------------------
    //    The signer's certificate.

    PCCERT_CONTEXT pSignerCert; 

    //---------------------------------------------------------------
    //    Buffer to hold the name of the subject of a certificate.

    char pszNameString[MAX_NAME];

    //---------------------------------------------------------------
    //  The following variables are used only in the decoding phase.

    DWORD cbData = sizeof(DWORD);

    //---------------------------------------------------------------
    //  Begin processing. Display the original message.

    rgpbToBeSigned[0] = pbContent;
    rgcbToBeSigned[0] = cbContent;

    printf("The original message = \n%s\n\n",
        rgpbToBeSigned[0]);

    //---------------------------------------------------------------
    // Open a certificate store.

    if(hSystemStoreHandle = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        CERTIFICATE_STORE_NAME))
    {
        printf("The certificate store is open. \n");
    }
    else
    {
        MyHandleError( "Error Getting Store Handle");
    }

    /*---------------------------------------------------------------
        Find a certificate in the store. This certificate will be 
        used to sign the message. To sign the message, the 
        certificate must have a private key accessible.
    ---------------------------------------------------------------*/

    if(pSignerCert = CertFindCertificateInStore(
        hSystemStoreHandle,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_STR,
        pwszSignerName,
        NULL))
    {
        //-----------------------------------------------------------
        //  Get and print the name of the subject of the certificate.

        if(CertGetNameString(
            pSignerCert,
            CERT_NAME_SIMPLE_DISPLAY_TYPE,
            0,
            NULL,
            pszNameString,
            MAX_NAME) > 1)
        {
            printf("The message signer is  %s \n",pszNameString);
        }
        else
        {
            MyHandleError("Getting the name of the signer " \
                "failed.\n");
        }
    }
    else
    {
        MyHandleError("Signer certificate not found.");
    }

    /*---------------------------------------------------------------
    Initialize the CRYPT_SIGN_MESSAGE_PARA structure. First, use 
    memset to set all members to zero or NULL. Then set the values of
    all members that must be nonzero.
    ---------------------------------------------------------------*/

    memset(&SignMessagePara, 0, sizeof(CRYPT_SIGN_MESSAGE_PARA));
    SignMessagePara.cbSize = sizeof(CRYPT_SIGN_MESSAGE_PARA);
    SignMessagePara.HashAlgorithm.pszObjId = szOID_RSA_MD2;
    SignMessagePara.pSigningCert = pSignerCert;
    SignMessagePara.dwMsgEncodingType = MY_ENCODING_TYPE;
    SignMessagePara.cMsgCert = 1;
    SignMessagePara.rgpMsgCert = &pSignerCert;

    /*---------------------------------------------------------------
        In two steps, sign and encode the message. First, get the 
        number of bytes required for the buffer to hold the signed 
        and encoded message.
    ---------------------------------------------------------------*/

    if( CryptSignMessage(
            &SignMessagePara,
            FALSE,
            1,
            rgpbToBeSigned,
            rgcbToBeSigned,
            NULL,
            &pEncodedBlob->cbData))
    {
        printf("The needed length is %d \n", pEncodedBlob->cbData);
    }
    else
    {
        MyHandleError("Getting the length failed.\n");
    }

    //---------------------------------------------------------------
    //   Allocate memory for the required buffer.
    pEncodedBlob->pbData = (BYTE *)malloc(pEncodedBlob->cbData);
    if(!pEncodedBlob->pbData)
    {
        MyHandleError("Memory allocation failed.");
    }

    //---------------------------------------------------------------
    //   Call CryptSignMessage a second time to
    //   copy the signed and encoded message to the buffer.

    if( CryptSignMessage(
        &SignMessagePara,
        FALSE,
        1,
        rgpbToBeSigned,
        rgcbToBeSigned,
        pEncodedBlob->pbData,
        &pEncodedBlob->cbData))
    {
        printf("Signing worked \n");
    }
    else
    {
        MyHandleError("Signing failed.\n");
    }

    //---------------------------------------------------------------
    //  Clean up after signing and encoding.

    if(pSignerCert)
    {
        CertFreeCertificateContext(pSignerCert);
    }
    
    if(hSystemStoreHandle)
    {
        CertCloseStore(hSystemStoreHandle,
            CERT_CLOSE_STORE_FORCE_FLAG);
    }

    return TRUE;
}

void DecodeMessage(PCRYPT_DATA_BLOB pEncodedBlob,
                   LPWSTR pwszSignerName)
{
    //---------------------------------------------------------------
    //    Buffer to hold the name of the subject of a certificate.

    char pszNameString[MAX_NAME];

    //---------------------------------------------------------------
    //  The following variables are used only in the decoding phase.

    HCRYPTMSG hMsg;
    HCERTSTORE hStoreHandle;           // certificate store handle
    DWORD cbData = sizeof(DWORD);
    DWORD cbDecoded;
    BYTE *pbDecoded;
    DWORD cbSignerCertInfo;
    PCERT_INFO pSignerCertInfo;
    PCCERT_CONTEXT pSignerCertContext;

    /*---------------------------------------------------------------
        The following code decodes the message and verifies the 
        message signature.  This code would normally be in a 
        stand-alone program that would read the signed and encoded 
        message and its length from a file from an email message, 
        or from some other source.
    ---------------------------------------------------------------*/

    //---------------------------------------------------------------
    //  Open a message for decoding.

    if(hMsg = CryptMsgOpenToDecode(
        MY_ENCODING_TYPE,      // encoding type
        0,                     // flags
        0,                     // use the default message type
                               // the message type is 
                               // listed in the message header
        NULL,                  // cryptographic provider 
                               // use NULL for the default provider
        NULL,                  // recipient information
        NULL))                 // stream information
    {
        printf("The message to decode is open. \n");
    }
    else
    {
        MyHandleError("OpenToDecode failed");
    }
    //---------------------------------------------------------------
    //  Update the message with an encoded BLOB.

    if(CryptMsgUpdate(
        hMsg,                 // handle to the message
        pEncodedBlob->pbData, // pointer to the encoded BLOB
        pEncodedBlob->cbData, // size of the encoded BLOB
        TRUE))                // last call
    {
        printf("The encoded BLOB has been added to the message. \n");
    }
    else
    {
        MyHandleError("Decode MsgUpdate failed");
    }

    //---------------------------------------------------------------
    //  Get the number of bytes needed for a buffer
    //  to hold the decoded message.

    if(CryptMsgGetParam(
        hMsg,                  // handle to the message
        CMSG_CONTENT_PARAM,    // parameter type
        0,                     // index
        NULL,                  
        &cbDecoded))           // size of the returned information
    {
        printf("The message parameter has been acquired. \n");
    }
    else
    {
        MyHandleError("Decode CMSG_CONTENT_PARAM failed.");
    }
    //---------------------------------------------------------------
    // Allocate memory.

    if(!(pbDecoded = (BYTE *) malloc(cbDecoded)))
    {
        MyHandleError("Decode memory allocation failed.");
    }

    //---------------------------------------------------------------
    // Copy the content to the buffer.

    if(CryptMsgGetParam(
        hMsg,                 // handle to the message
        CMSG_CONTENT_PARAM,   // parameter type
        0,                    // index
        pbDecoded,            // address for returned information
        &cbDecoded))          // size of the returned information
    {
        printf("The decoded message is =>\n%s\n\n",
            (LPSTR)pbDecoded);
    }
    else
    {
        MyHandleError("Decode CMSG_CONTENT_PARAM #2 failed");
    }

    //---------------------------------------------------------------
    // Verify the signature.
    // First, get the signer CERT_INFO from the message.

    //---------------------------------------------------------------
    // Get the size of memory required for the certificate.

    if(CryptMsgGetParam(
        hMsg,                         // handle to the message
        CMSG_SIGNER_CERT_INFO_PARAM,  // parameter type
        0,                            // index
        NULL,   
        &cbSignerCertInfo))           // size of the returned 
                                      // information
    {
        printf("%d bytes needed for the buffer.\n", 
            cbSignerCertInfo);
    }
    else
    {
        MyHandleError("Verify SIGNER_CERT_INFO #1 failed.");
    }

    //---------------------------------------------------------------
    // Allocate memory.

    if(!(pSignerCertInfo = (PCERT_INFO) malloc(cbSignerCertInfo)))
    {
        MyHandleError("Verify memory allocation failed.");
    }

    //---------------------------------------------------------------
    // Get the message certificate information (CERT_INFO
    // structure).

    if(!(CryptMsgGetParam(
        hMsg,                         // handle to the message
        CMSG_SIGNER_CERT_INFO_PARAM,  // parameter type
        0,                            // index
        pSignerCertInfo,              // address for returned 
                                      // information
        &cbSignerCertInfo)))          // size of the returned 
                                      // information
    {
        MyHandleError("Verify SIGNER_CERT_INFO #2 failed");
    }

    //---------------------------------------------------------------
    // Open a certificate store in memory using CERT_STORE_PROV_MSG,
    // which initializes it with the certificates from the message.

    if(hStoreHandle = CertOpenStore(
        CERT_STORE_PROV_MSG,         // store provider type 
        MY_ENCODING_TYPE,            // encoding type
        NULL,                        // cryptographic provider
                                     // use NULL for the default
        0,                           // flags
        hMsg))                       // handle to the message
    {
        printf("The certificate store to be used for message " \
            "verification has been opened.\n");
    }
    else  
    {
        MyHandleError("Verify open store failed");
    }

    //---------------------------------------------------------------
    // Find the signer's certificate in the store.

    if(pSignerCertContext = CertGetSubjectCertificateFromStore(
        hStoreHandle,       // handle to the store
        MY_ENCODING_TYPE,   // encoding type
        pSignerCertInfo))   // pointer to retrieved CERT_CONTEXT
    {
        if(CertGetNameString(
            pSignerCertContext,
            CERT_NAME_SIMPLE_DISPLAY_TYPE,
            0,
            NULL,
            pszNameString,
            MAX_NAME) > 1)
        {
            printf("The message signer is  %s \n",pszNameString);
        }
        else
        {
            MyHandleError("Getting the signer's name failed.\n");
        }
    }
    else
    {
        MyHandleError("Verify GetSubjectCert failed");
    }

    //---------------------------------------------------------------
    // Use the CERT_INFO from the signer certificate to verify
    // the signature.

    if(CryptMsgControl(
        hMsg,
        0,
        CMSG_CTRL_VERIFY_SIGNATURE,
        pSignerCertContext->pCertInfo))
    {
        printf("Verify signature succeeded. \n");
    }
    else
    {
        printf("The signature was not verified. \n");
        ReportFailure();
    }
    //---------------------------------------------------------------
    // Clean up.
    if(pEncodedBlob->pbData)
    {
        free(pEncodedBlob->pbData);
        pEncodedBlob->pbData = NULL;
    }
    if(pbDecoded)
    {
        free(pbDecoded);
    }
    if(pSignerCertInfo)
    {
        free(pSignerCertInfo);
    }
    if(pSignerCertContext)
    {
        CertFreeCertificateContext(pSignerCertContext); 
    }
    if(hStoreHandle)
    {
        CertCloseStore(hStoreHandle, CERT_CLOSE_STORE_FORCE_FLAG);
    }
    if(hMsg)
    {
        CryptMsgClose(hMsg);
    }
}
```



 

 
