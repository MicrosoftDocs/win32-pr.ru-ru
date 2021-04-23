---
description: хэширует и кодирует текстовое сообщение, а затем декодирует и проверяет сообщение.
ms.assetid: effe4080-63c1-4f35-a5e3-e7e60754b28f
title: 'Пример программы на языке C: кодирование и декодирование хэшированного сообщения'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5904a684d02a81acba1502162c779b9f124d3dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684099"
---
# <a name="example-c-program-encoding-and-decoding-a-hashed-message"></a><span data-ttu-id="4e436-103">Пример программы на языке C: кодирование и декодирование хэшированного сообщения</span><span class="sxs-lookup"><span data-stu-id="4e436-103">Example C Program: Encoding and Decoding a Hashed Message</span></span>

<span data-ttu-id="4e436-104">В следующем примере выполняется [*хэширование*](../secgloss/h-gly.md) и кодирование текстового сообщения, а затем декодируется и проверяется сообщение.</span><span class="sxs-lookup"><span data-stu-id="4e436-104">The following example [*hashes*](../secgloss/h-gly.md) and encodes a text message, and then decodes and verifies the message.</span></span>

<span data-ttu-id="4e436-105">Хотя для простоты в этом примере были объединены две различные функции, в более реалистичном параметре две части будут использоваться отдельно.</span><span class="sxs-lookup"><span data-stu-id="4e436-105">Although, for simplicity, the two different functions have been combined in this example, in a more realistic setting the two parts would be used separately.</span></span>

<span data-ttu-id="4e436-106">В этом примере показаны следующие задачи и функции CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="4e436-106">This example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="4e436-107">Вызов [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) для получения поставщика CSP.</span><span class="sxs-lookup"><span data-stu-id="4e436-107">Calling [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) to acquire a CSP provider.</span></span>
-   <span data-ttu-id="4e436-108">Использование [**криптмсгкалкулатинкодедленгс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) для вычисления длины закодированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e436-108">Using [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) to calculate the length of the encoded message.</span></span>
-   <span data-ttu-id="4e436-109">Выделение памяти для буфера для хранения закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="4e436-109">Allocating memory for a buffer to hold the encoded data.</span></span>
-   <span data-ttu-id="4e436-110">Открытие сообщения для кодирования с помощью [**криптмсгопентоенкоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode).</span><span class="sxs-lookup"><span data-stu-id="4e436-110">Opening a message to encode using [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode).</span></span>
-   <span data-ttu-id="4e436-111">Добавление содержимого в сообщение для кодирования с помощью [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span><span class="sxs-lookup"><span data-stu-id="4e436-111">Adding content to the message to encode using [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span></span>
-   <span data-ttu-id="4e436-112">Использование [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) для копирования закодированного сообщения в выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="4e436-112">Using [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to copy the encoded message to the allocated buffer.</span></span>
-   <span data-ttu-id="4e436-113">Открытие сообщения для декодирования с помощью [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span><span class="sxs-lookup"><span data-stu-id="4e436-113">Opening a message to decode using [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span></span>
-   <span data-ttu-id="4e436-114">Добавление закодированного сообщения в сообщение для декодирования с помощью [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span><span class="sxs-lookup"><span data-stu-id="4e436-114">Adding the encoded message to the message to decode using [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span></span>
-   <span data-ttu-id="4e436-115">Создание повторяющегося указателя на сообщение с помощью [**криптмсгдупликате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate).</span><span class="sxs-lookup"><span data-stu-id="4e436-115">Creating a duplicate pointer to the message using [**CryptMsgDuplicate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate).</span></span>
-   <span data-ttu-id="4e436-116">Проверка типа сообщений с помощью [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span><span class="sxs-lookup"><span data-stu-id="4e436-116">Checking the message type with [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span></span>
-   <span data-ttu-id="4e436-117">Использование [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) для декодирования сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e436-117">Using [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to decode the message.</span></span>
-   <span data-ttu-id="4e436-118">Проверка хэша с помощью [**криптмсгконтрол**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol).</span><span class="sxs-lookup"><span data-stu-id="4e436-118">Verifying the hash using [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol).</span></span>
-   <span data-ttu-id="4e436-119">Использование [**криптмсгклосе**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) для освобождения обработчика сообщений.</span><span class="sxs-lookup"><span data-stu-id="4e436-119">Using [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to release the message handle.</span></span>
-   <span data-ttu-id="4e436-120">Использование [**криптрелеасеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) для выпуска CSP.</span><span class="sxs-lookup"><span data-stu-id="4e436-120">Using [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) to release the CSP.</span></span>

<span data-ttu-id="4e436-121">В этом примере используется функция [**михандлиррор**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="4e436-121">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="4e436-122">Код для этой функции включен в пример.</span><span class="sxs-lookup"><span data-stu-id="4e436-122">Code for this function is included with the sample.</span></span>

<span data-ttu-id="4e436-123">Код для этой и других вспомогательных функций также указан в разделе [общего назначения функции](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4e436-123">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
//  Copyright (C) Microsoft.  All rights reserved.
//  Declare and initialize variables. This includes creating a 
//  pointer to the message content. In real situations, 
//  the message content will usually exist somewhere and a pointer
//  to it will get passed to the application. 

BYTE* pbContent = (BYTE*) "A razzle-dazzle hashed message \n"
       "Hashing is better than trashing. \n";    // The message
DWORD cbContent = strlen((char *)pbContent)+1;  // Size of message
                                                // including the  
                                                // final NULL.
HCRYPTPROV hCryptProv;                          // CSP handle
DWORD HashAlgSize;
CRYPT_ALGORITHM_IDENTIFIER HashAlgorithm;
CMSG_HASHED_ENCODE_INFO HashedEncodeInfo;
DWORD cbEncodedBlob;
BYTE *pbEncodedBlob;
HCRYPTMSG hMsg;
HCRYPTMSG hDupMsg;
//-------------------------------------------------------------------
//  Variables to be used in decoding.
DWORD cbData = sizeof(DWORD);
DWORD dwMsgType;
DWORD cbDecoded;
BYTE  *pbDecoded;

//-------------------------------------------------------------------
//  Begin processing.

printf("Begin processing. \n");
printf("The message to be hashed and encoded is: \n");
printf("%s\n",pbContent);    // Display original message.
printf("The starting message length is %d\n",cbContent);

//-------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(
               &hCryptProv,     // Address for the handle. 
               NULL,            // Use the current user's logon name.
               NULL,            // Use the default provider.
               PROV_RSA_FULL,   // Provider type.
               0))              // Zero allows access to
                                // private keys.
{
    printf("A CSP context has been acquired. \n");
}
else
{
    MyHandleError("CryptAcquireContext failed.");
}
//-------------------------------------------------------------------
// The function succeeded; hCryptProv is the CSP handle.

//-------------------------------------------------------------------
// Initialize the algorithm identifier structure.

HashAlgSize = sizeof(HashAlgorithm);
memset(&HashAlgorithm, 0, HashAlgSize);   // Initialize to zero.
HashAlgorithm.pszObjId = szOID_RSA_MD5;   // Then set the 
                                          //   necessary member.

//-------------------------------------------------------------------
// Initialize the CMSG_HASHED_ENCODE_INFO structure.

memset(&HashedEncodeInfo, 0, sizeof(CMSG_HASHED_ENCODE_INFO));
HashedEncodeInfo.cbSize = sizeof(CMSG_HASHED_ENCODE_INFO);
HashedEncodeInfo.hCryptProv = hCryptProv;
HashedEncodeInfo.HashAlgorithm = HashAlgorithm;
HashedEncodeInfo.pvHashAuxInfo = NULL;

//-------------------------------------------------------------------
// Get the size of the encoded message BLOB.

if(cbEncodedBlob = CryptMsgCalculateEncodedLength(
                     MY_ENCODING_TYPE,     // Message encoding type
                     0,                    // Flags
                     CMSG_HASHED,          // Message type
                     &HashedEncodeInfo,    // Pointer to structure
                     NULL,                 // Inner content object ID
                     cbContent))           // Size of content
{
    printf("The length to be allocated is %d bytes.\n",
        cbEncodedBlob);
}
else
{
    MyHandleError("Getting cbEncodedBlob length failed");
}
//-------------------------------------------------------------------
// Allocate memory for the encoded BLOB.
if(pbEncodedBlob = (BYTE *) malloc(cbEncodedBlob))
{
    printf("%d bytes of memory have been allocated.\n",
        cbEncodedBlob);
}
else
{
    MyHandleError("Malloc operation failed.");
}
//-------------------------------------------------------------------
// Open a message to encode.

if(hMsg = CryptMsgOpenToEncode(
            MY_ENCODING_TYPE,        // Encoding type
            0,                       // Flags
            CMSG_HASHED,             // Message type
            &HashedEncodeInfo,       // Pointer to structure
            NULL,                    // Inner content object ID
            NULL))                   // Stream information (not used)
{
    printf("The message to encode has been opened. \n");
}
else
{
    MyHandleError("OpenToEncode failed");
}
//-------------------------------------------------------------------
// Update the message with the data.

if(CryptMsgUpdate(
            hMsg,          // Handle to the message
            pbContent,     // Pointer to the content
            cbContent,     // Size of the content
            TRUE))         // Last call
{
    printf("Data has been added to the message to encode. \n");
}
else
{
    MyHandleError("MsgUpdate failed");
}
//-------------------------------------------------------------------
// Create a duplicate of the message.

if(hDupMsg = CryptMsgDuplicate(hMsg))
{
     printf("The message has been duplicated.\n");
}
else
{
     MyHandleError("Duplication of the message failed.");
}

//-------------------------------------------------------------------
// Get the resulting message from the duplicate of the message.

if(CryptMsgGetParam(
               hDupMsg,                  // Handle to the message
               CMSG_CONTENT_PARAM,       // Parameter type
               0,                        // Index
               pbEncodedBlob,            // Pointer to the BLOB
               &cbEncodedBlob))          // Size of the BLOB
{
     printf("Message encoded successfully. \n");
}
else    
{
    MyHandleError("MsgGetParam failed");
}
//-------------------------------------------------------------------
// Close both messages to prepare for decoding.

CryptMsgClose(hMsg);
CryptMsgClose(hDupMsg);

// The following code decodes the hashed message.
// Usually, this would be in a separate program and the encoded,
// hashed data would be input from a file, from an email message, 
// or from some other source.
//
// The variables used in this code have already been
// declared and initialized.

//-------------------------------------------------------------------
// Open the  message for decoding.

if(hMsg = CryptMsgOpenToDecode(
            MY_ENCODING_TYPE,       // Encoding type
            0,                      // Flags
            0,                      // Message type 
                                    // (get from message)
            hCryptProv,             // Cryptographic provider
            NULL,                   // Recipient information
            NULL))                  // Stream information
{
     printf("The message has been opened for decoding. \n");
}
else
{
     MyHandleError("OpenToDecode failed");
}
//-------------------------------------------------------------------
// Update the message with the encoded BLOB. 

if(CryptMsgUpdate(
            hMsg,             // Handle to the message
            pbEncodedBlob,    // Pointer to the encoded BLOB
            cbEncodedBlob,    // Size of the encoded BLOB
            TRUE))            // Last call
{
     printf("The encoded data is added to the message "
         "to decode. \n");
}
else
{
    MyHandleError("Decode MsgUpdate failed");
}
//-------------------------------------------------------------------
// Get the message type.

if(CryptMsgGetParam(
       hMsg,               // Handle to the message
       CMSG_TYPE_PARAM,    // Parameter type
       0,                  // Index
       &dwMsgType,         // Address for returned information
       &cbData))           // Size of the returned information
{
    printf("The message type has been obtained. \n");
}
else
{
    MyHandleError("Decode CMSG_TYPE_PARAM failed");
}
//-------------------------------------------------------------------
// Some applications may need to use a switch statement here
// and process the message differently, depending on the
// message type.

if(dwMsgType == CMSG_HASHED)
{
     printf("The message is a hashed message. Proceed. \n");
}
else
{
    MyHandleError("Wrong message type");
}
//-------------------------------------------------------------------
// Get the size of the content.

if(CryptMsgGetParam(
               hMsg,                   // Handle to the message
               CMSG_CONTENT_PARAM,     // Parameter type
               0,                      // Index
               NULL,                   // Address for returned 
                                       // information
               &cbDecoded))            // Size of the returned 
                                       // information
{
    printf("The length %d of the message obtained. \n", cbDecoded);
}
else
{
    MyHandleError("Decode CMSG_CONTENT_PARAM failed");
}
//-------------------------------------------------------------------
// Allocate memory.

if(pbDecoded = (BYTE *) malloc(cbDecoded))
{
     printf("Memory for the decoded message has been allocated.\n");
}
else
{
    MyHandleError("Decoding memory allocation failed");
}
//-------------------------------------------------------------------
// Copy the decoded message into the buffer just allocated.

if(CryptMsgGetParam(
            hMsg,                    // Handle to the message
            CMSG_CONTENT_PARAM,      // Parameter type
            0,                       // Index
            pbDecoded,               // Address for returned 
                                     // information
            &cbDecoded))             // Size of the returned 
                                     // information
{
    printf("Message decoded successfully \n");
    printf("The decoded message is \n%s\n", (LPSTR)pbDecoded);
}
else
{
    MyHandleError("Decoding CMSG_CONTENT_PARAM #2 failed");
}
//-------------------------------------------------------------------
// Verify the hash.

if(CryptMsgControl(
              hMsg,                        // Handle to the message
              0,                           // Flags
              CMSG_CTRL_VERIFY_HASH,       // Control type
              NULL))                       // Pointer not used
{
    printf("Verification of hash succeeded. \n");
    printf("The data has not been tampered with.\n");
}
else
{
     printf("Verification of hash failed. Something changed "
         "this message .\n");
}

printf("Test program completed without error. \n");

//-------------------------------------------------------------------
// Clean up

if(pbEncodedBlob)
    free(pbEncodedBlob);
if(pbDecoded)
    free(pbDecoded);

CryptMsgClose(hMsg); 

// Release the CSP.

if(hCryptProv) 
   CryptReleaseContext(hCryptProv,0);
} // End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the standard  
//  error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // End of MyHandleError
```



 

 
