---
description: Демонстрирует использование функций Криптмсгопентоенкоде, Криптмсгопентодекоде и Криптмсгупдате с \_ \_ структурой сведений о потоке КМСГ для кодирования и декодирования сообщения с помощью функций потоковой передачи этих функций.
ms.assetid: 6c9c0509-1ad9-42cd-9589-e77752df6739
title: 'Пример программы на языке C: кодирование и декодирование сообщения с помощью потока'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 962420bfba05caabb272419e305ee01f76d39c63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811783"
---
# <a name="example-c-program-encoding-and-decoding-a-message-using-a-stream"></a><span data-ttu-id="78054-103">Пример программы на языке C: кодирование и декодирование сообщения с помощью потока</span><span class="sxs-lookup"><span data-stu-id="78054-103">Example C Program: Encoding and Decoding a Message Using a Stream</span></span>

<span data-ttu-id="78054-104">В следующем примере показано, как использовать функции [**криптмсгопентоенкоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)и [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) со структурой [**\_ \_ сведений о потоке КМСГ**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) для кодирования и декодирования сообщения с помощью функций потоковой передачи этих функций.</span><span class="sxs-lookup"><span data-stu-id="78054-104">The following example demonstrates how to use the [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), and [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) functions with the [**CMSG\_STREAM\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) structure to encode and decode a message using the streaming features of these functions.</span></span>

<span data-ttu-id="78054-105">Подписывание и кодирование сообщения не гарантирует конфиденциальности этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="78054-105">Signing and encoding a message does not ensure privacy for that message.</span></span> <span data-ttu-id="78054-106">Вместо этого он гарантирует подлинность сообщения.</span><span class="sxs-lookup"><span data-stu-id="78054-106">Rather it ensures the authenticity of the message.</span></span> <span data-ttu-id="78054-107">Поскольку сообщение подписано с помощью закрытого ключа отправителя, когда получатель сообщения расшифровывает подпись с помощью [*открытого ключа*](../secgloss/p-gly.md) отправителя (доступного из сертификата, который отправляется вместе с сообщением), получатель может убедиться, что сообщение было отправлено пользователем или объектом, связанным с сертификатом, и что сообщение не было изменено после того, как оно было подписано.</span><span class="sxs-lookup"><span data-stu-id="78054-107">Because the message is signed with the sender's private key, when the receiver of the message decrypts the signature with the sender's [*public key*](../secgloss/p-gly.md) (available from the certificate that is sent along with the message), the receiver can be sure that the message was sent by the person or entity associated with the certificate and that the message was not changed after it was signed.</span></span>

<span data-ttu-id="78054-108">В этой части примера для подписи кода показаны следующие задачи и функции CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="78054-108">This encoding signing portion of this example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="78054-109">Открытие хранилища сертификатов с помощью [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="78054-109">Opening a certificate store by using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
-   <span data-ttu-id="78054-110">Получение сертификата с указанным именем субъекта с помощью [**цертфиндцертификатеинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span><span class="sxs-lookup"><span data-stu-id="78054-110">Retrieving a certificate with a specific subject name by using [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span></span>
-   <span data-ttu-id="78054-111">Получение и печать имени субъекта сертификата с помощью [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="78054-111">Getting and printing a certificate's subject name by using [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>
-   <span data-ttu-id="78054-112">Получение маркера поставщику служб шифрования, который может предоставить закрытый ключ с помощью функции [**криптаккуирецертификатеприватекэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey) .</span><span class="sxs-lookup"><span data-stu-id="78054-112">Getting the handle to a cryptographic provider that can provide a private key with the [**CryptAcquireCertificatePrivateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey) function.</span></span>
-   <span data-ttu-id="78054-113">Инициализация [**\_ \_ \_ сведений о кодировке со знаком КМСГ**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) и структур [**\_ \_ сведений о потоке КМСГ**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) , которые будут использоваться в вызове [**криптмсгопентоенкоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode).</span><span class="sxs-lookup"><span data-stu-id="78054-113">Initializing the [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) and [**CMSG\_STREAM\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) structures to be used in a call to [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode).</span></span>
-   <span data-ttu-id="78054-114">Подписывание и кодирование сообщения с помощью [**криптмсгопентоенкоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode) и [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span><span class="sxs-lookup"><span data-stu-id="78054-114">Signing and encoding a message by using [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode) and [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span></span>
-   <span data-ttu-id="78054-115">Реализация функции обратного вызова Stream, которая может сохранять закодированные и подписанные сообщения в любом постоянном формате, например при записи в файл.</span><span class="sxs-lookup"><span data-stu-id="78054-115">Implementing a stream callback function that can save an encoded and signed message in any persistent format, such as writing it to a file.</span></span>

<span data-ttu-id="78054-116">Декодирование в этом примере иллюстрирует следующие задачи и функции CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="78054-116">The decoding portion of this example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="78054-117">Инициализация [**структуры \_ \_ сведений о потоке КМСГ**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) для использования в вызове [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span><span class="sxs-lookup"><span data-stu-id="78054-117">Initializing a [**CMSG\_STREAM\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) structure to be used in a call to [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span></span>
-   <span data-ttu-id="78054-118">Реализация функции обратного вызова Stream, которая может сохранить декодированное сообщение в любом постоянном формате, например при печати на экране.</span><span class="sxs-lookup"><span data-stu-id="78054-118">Implementing a stream callback function that can save a decoded message in any persistent format, such as printing it to the screen.</span></span>
-   <span data-ttu-id="78054-119">Чтение закодированного сообщения из файла и декодирование сообщения с помощью [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span><span class="sxs-lookup"><span data-stu-id="78054-119">Reading an encoded message from a file and decoding the message by using [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span></span>

<span data-ttu-id="78054-120">Пример выполнения таких операций без использования обратного вызова потока см. в разделе [Пример программы C: подписывание, кодирование, декодирование и проверка сообщения](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="78054-120">For an example of how to perform these same operations without using a stream callback, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

<span data-ttu-id="78054-121">В этом примере используется функция [**михандлиррор**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="78054-121">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="78054-122">Код для этой функции включен в пример.</span><span class="sxs-lookup"><span data-stu-id="78054-122">Code for this function is included with the sample.</span></span> <span data-ttu-id="78054-123">Код для этой и других вспомогательных функций также указан в [разделе \_ \_ функции общего назначения](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="78054-123">Code for this and other auxiliary functions is also listed under [General\_Purpose\_Functions](general-purpose-functions.md).</span></span>


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

#define MAX_NAME 256

#define ENCODED_FILE_NAME L"testStream.p7s"

//-------------------------------------------------------------------
//  Define function MyHandleError.
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

//+----------------------------------------------
// Callback function used for streamed Signing. 
//-----------------------------------------------
BOOL 
WINAPI
EncodeCallback(
    const void *pvArg,
    BYTE *pbData,
    DWORD cbData,
    BOOL fFinal)
{
    DWORD dwWrittenBytes = 0;
    HANDLE hFileToWrite = INVALID_HANDLE_VALUE;
        
    hFileToWrite = *((HANDLE *)pvArg);
    if ( !WriteFile(
            hFileToWrite,
            pbData,
            cbData,
            &dwWrittenBytes,
            NULL) ||
        (dwWrittenBytes != cbData))
    {
        return FALSE;
    }

    return TRUE;
}

//+----------------------------------------------
// Callback function used for decoding streamed Signing.
//-----------------------------------------------
BOOL 
WINAPI
DecodeCallback(
    const void *pvArg,
    BYTE *pbData,
    DWORD cbData,
    BOOL fFinal)
{
    if (pbData != NULL && cbData > 0)
    {
        *(pbData+cbData) = 0;
        printf("%s", (char*)pbData);
    }

    return TRUE;
}

void EncodeMessageWithStream(LPWSTR pwszSignerName)
{
    //---------------------------------------------------------------
    // Declare and initialize variables. This includes declaring and 
    // initializing a pointer to message content to be countersigned 
    // and encoded. Usually, the message content will exist somewhere
    // and a pointer to it is passed to the application. 

    BYTE* pbContent1 = (BYTE*)"First sentence. ";
    DWORD cbContent1 = lstrlenA((char *)pbContent1);
    BYTE* pbContent2 = (BYTE*)"Second sentence. ";
    DWORD cbContent2 = lstrlenA((char *)pbContent2);

    HCRYPTPROV hCryptProv;         // CSP handle
    HCERTSTORE hStoreHandle;       // store handle
    PCCERT_CONTEXT pSignerCert;    // signer certificate
    CMSG_SIGNER_ENCODE_INFO SignerEncodeInfo;
    CMSG_SIGNER_ENCODE_INFO SignerEncodeInfoArray[1];
    CERT_BLOB SignerCertBlob;
    CERT_BLOB SignerCertBlobArray[1];
    CMSG_SIGNED_ENCODE_INFO SignedMsgEncodeInfo;
    HCRYPTMSG hMsg;
    LPWSTR pszNameString;
    DWORD dwKeySpec;

    //---------------------------------------------------------------
    // Open the My system certificate store.

    if(!(hStoreHandle = CertOpenStore(
        // The system store will be a virtual store.
        CERT_STORE_PROV_SYSTEM,
        // Encoding type not needed with this PROV.
        0,
        // Accept the default HCRYPTPROV. 
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        // Set the system store location in the registry. Other 
        // predefined system stores could have been used, including 
        // trust, Ca, or root.
        L"MY")))                
    {
        MyHandleError(L"Could not open the MY system store.");
    }

    //---------------------------------------------------------------
    // Get a pointer to a signer's signature certificate.

    if(pSignerCert = CertFindCertificateInStore(
        hStoreHandle,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_STR,
        pwszSignerName,
        NULL))
    {
        //-----------------------------------------------------------
        //   A certificate was found. Get and print the name of the 
        //   subject of the certificate.

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
            MyHandleError(L"CertGetNameString failed.\n");
        }
    }
    else
    {
        MyHandleError(L"Cert not found.\n");
    }

    //---------------------------------------------------------------
    // Initialize the CMSG_SIGNER_ENCODE_INFO structure.

    //---------------------------------------------------------------
    // Get a handle to a cryptographic provider. 
    if(!(CryptAcquireCertificatePrivateKey(
        pSignerCert,
        0,
        NULL,
        &hCryptProv,
        &dwKeySpec,
        NULL)))
    {
        DWORD dwError = GetLastError();
        if(NTE_BAD_PUBLIC_KEY == dwError)
        {
            printf("NTE_BAD_PUBLIC_KEY\n");
        }

        MyHandleError(L"CryptAcquireContext failed");
    }
     
    memset(&SignerEncodeInfo, 0, sizeof(CMSG_SIGNER_ENCODE_INFO));
    SignerEncodeInfo.cbSize = sizeof(CMSG_SIGNER_ENCODE_INFO);
    SignerEncodeInfo.pCertInfo = pSignerCert->pCertInfo;
    SignerEncodeInfo.hCryptProv = hCryptProv;
    SignerEncodeInfo.dwKeySpec = dwKeySpec;
    SignerEncodeInfo.HashAlgorithm.pszObjId = szOID_RSA_MD5;
    SignerEncodeInfo.pvHashAuxInfo = NULL;

    //---------------------------------------------------------------
    // Initialize the first element of an array of signers. 
    // Note: Currently, there is only one signer.

    SignerEncodeInfoArray[0] = SignerEncodeInfo;

    //---------------------------------------------------------------
    // Initialize the CMSG_SIGNED_ENCODE_INFO structure.

    SignerCertBlob.cbData = pSignerCert->cbCertEncoded;
    SignerCertBlob.pbData = pSignerCert->pbCertEncoded;

    //---------------------------------------------------------------
    //  Initialize the first element of an array of signer BLOBs.
    //  Note: In this program, there is only one signer BLOB used.

    SignerCertBlobArray[0] = SignerCertBlob;
    memset(&SignedMsgEncodeInfo, 0, sizeof(CMSG_SIGNED_ENCODE_INFO));
    SignedMsgEncodeInfo.cbSize = sizeof(CMSG_SIGNED_ENCODE_INFO);
    SignedMsgEncodeInfo.cSigners = 1;
    SignedMsgEncodeInfo.rgSigners = SignerEncodeInfoArray;
    SignedMsgEncodeInfo.cCertEncoded = 1;
    SignedMsgEncodeInfo.rgCertEncoded = SignerCertBlobArray;

    // Fill the CMSG_STREAM_INFO structure.
    CMSG_STREAM_INFO stStreamInfo;

    // BER_ENCODING
    stStreamInfo.cbContent = 0xffffffff;
    // DER_ENCODING 
    // stStreamInfo.cbContent = cbContent;

    stStreamInfo.pfnStreamOutput = EncodeCallback;
    HANDLE hOutMsgFile = INVALID_HANDLE_VALUE;
    hOutMsgFile = CreateFile(
            ENCODED_FILE_NAME,
            GENERIC_WRITE,
            FILE_SHARE_WRITE,
            NULL,
            CREATE_ALWAYS,
            FILE_ATTRIBUTE_NORMAL,
            NULL);
    if (INVALID_HANDLE_VALUE == hOutMsgFile)
    {
        MyHandleError(L"CreateFile (OUT MSG)");
    }

    stStreamInfo.pvArg = &hOutMsgFile; 

    //---------------------------------------------------------------
    // Open a message to encode.

    if(!(hMsg = CryptMsgOpenToEncode(
        MY_ENCODING_TYPE,      // encoding type
        0,                     // flags
        CMSG_SIGNED,           // message type
        &SignedMsgEncodeInfo,  // pointer to structure
        NULL,                  // inner content OID
        &stStreamInfo)))       // stream information
    {
        MyHandleError(L"OpenToEncode failed");
    }

    //---------------------------------------------------------------
    // Update the message with the data.

    if(!(CryptMsgUpdate(
        hMsg,        // handle to the message
        pbContent1,  // pointer to the content
        cbContent1,  // size of the content
        FALSE)))     // first call
    {
        MyHandleError(L"MsgUpdate failed");
    }

    if(!(CryptMsgUpdate(
        hMsg,        // handle to the message
        pbContent2,  // pointer to the content
        cbContent2,  // size of the content
        TRUE)))      // last call
    {
        MyHandleError(L"MsgUpdate failed");
    }

    //---------------------------------------------------------------
    // The message is signed and encoded.
    // Close the message handle and the certificate store.

    CryptMsgClose(hMsg);
    CertCloseStore(hStoreHandle, CERT_CLOSE_STORE_FORCE_FLAG);
    CryptReleaseContext(hCryptProv,0);
    CloseHandle(hOutMsgFile);
}

void DecodeMessageWithStream()
{
    //---------------------------------------------------------------
    // Open the message for decoding.

    HCRYPTMSG hMsg;

    // Fill the CMSG_STREAM_INFO structure.
    CMSG_STREAM_INFO stStreamInfo2;

    // BER_ENCODING
    stStreamInfo2.cbContent = 0xffffffff;
    stStreamInfo2.pfnStreamOutput = DecodeCallback;

    if(!(hMsg = CryptMsgOpenToDecode(
        MY_ENCODING_TYPE,   // encoding type
        0,                  // flags
        0,                  // message type (get from message)
        NULL,               // cryptographic provider
                            // use NULL for the default provider
        NULL,               // recipient information
        &stStreamInfo2)))   // stream information
    {
        MyHandleError(L"OpenToDecode failed.");
    }

    HANDLE hInMsgFile = INVALID_HANDLE_VALUE;
    hInMsgFile = CreateFile(
            ENCODED_FILE_NAME,
            GENERIC_READ,
            FILE_SHARE_READ,
            NULL,
            OPEN_EXISTING,
            FILE_ATTRIBUTE_NORMAL,
            NULL);
    if (INVALID_HANDLE_VALUE == hInMsgFile)
    {
        MyHandleError(L"CreateFile (IN MSG)");
    }

    const DWORD cbBytesToRead = 256;
    byte pbEncodedBlob[cbBytesToRead];
    DWORD cbBytesRead;
    BOOL lastCall = FALSE;

    while (ReadFile(
        hInMsgFile,
        pbEncodedBlob,
        cbBytesToRead,
        &cbBytesRead,
        NULL))
    {
        if (cbBytesRead < cbBytesToRead)
        {
            lastCall = TRUE;
        }

        if(!(CryptMsgUpdate(
            hMsg,            // handle to the message
            pbEncodedBlob,   // pointer to the encoded BLOB
            cbBytesRead,     // size of the encoded BLOB
            lastCall)))      // last call
        {
            MyHandleError(L"Decode MsgUpdate failed.");
        }

        if (lastCall)
        {
            break;
        }
    }

    CryptMsgClose(hMsg);
    CloseHandle(hInMsgFile);
}
```



 

 
