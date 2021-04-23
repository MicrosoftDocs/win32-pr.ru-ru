---
description: В следующем примере показана сериализация контекста сертификата и его свойств в форму, которая может быть сохранена в файле, отправлена с сообщением электронной почты или иным образом передана другому пользователю.
ms.assetid: cda7fa68-debe-40e6-8c4a-536dacccc2d1
title: Пример программы на языке C. Сериализация сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efee0269a587e659605d375472f6e0ba16673d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081132"
---
# <a name="example-c-program-serializing-certificates"></a><span data-ttu-id="36db1-103">Пример программы на языке C. Сериализация сертификатов</span><span class="sxs-lookup"><span data-stu-id="36db1-103">Example C Program: Serializing Certificates</span></span>

<span data-ttu-id="36db1-104">В следующем примере показана сериализация [*контекста сертификата*](../secgloss/c-gly.md) и его свойств в форму, которая может быть сохранена в файле, отправлена с сообщением электронной почты или иным образом передана другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="36db1-104">The following example demonstrates serializing a [*certificate context*](../secgloss/c-gly.md) and its properties into a form that can be stored in a file, sent with an email message, or otherwise transmitted to another user.</span></span> <span data-ttu-id="36db1-105">В примере также показано, как сериализованный сертификат можно изменить обратно в сертификат и добавить в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="36db1-105">The example also shows how the serialized certificate can be changed back into a certificate and added to a certificate store.</span></span> <span data-ttu-id="36db1-106">Этот же процесс также работает с списками [*отзыва сертификатов*](../secgloss/c-gly.md) и списков [*CTL*](../secgloss/c-gly.md) с помощью [**цертсериализекрлсторилемент**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) и [**цертсериализектлсторилемент**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement).</span><span class="sxs-lookup"><span data-stu-id="36db1-106">The same process works also with [*CRLs*](../secgloss/c-gly.md) and [*CTLs*](../secgloss/c-gly.md) using [**CertSerializeCRLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) and [**CertSerializeCTLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement).</span></span>

<span data-ttu-id="36db1-107">В этом примере показаны следующие задачи и функции CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="36db1-107">This example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="36db1-108">Открытие хранилища сертификатов системы с помощью [**цертопенсистемсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).</span><span class="sxs-lookup"><span data-stu-id="36db1-108">Opening a system certificate store using [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).</span></span>
-   <span data-ttu-id="36db1-109">Открытие хранилища сертификатов с помощью [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="36db1-109">Opening a certificate store using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
-   <span data-ttu-id="36db1-110">Получение сертификата из хранилища с помощью [**цертенумцертификатесинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).</span><span class="sxs-lookup"><span data-stu-id="36db1-110">Retrieving a certificate from a store using [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).</span></span>
-   <span data-ttu-id="36db1-111">Получение имени субъекта сертификата с помощью [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="36db1-111">Getting the name of the certificate's subject using [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>
-   <span data-ttu-id="36db1-112">Создание сериализованной формы [*контекста сертификата*](../secgloss/c-gly.md) и его свойств с помощью [**цертсериализецертификатесторилемент**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement).</span><span class="sxs-lookup"><span data-stu-id="36db1-112">Creating a serialized form of a [*certificate context*](../secgloss/c-gly.md) and its properties using [**CertSerializeCertificateStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement).</span></span>
-   <span data-ttu-id="36db1-113">Создание нового сертификата из сериализованной строки и добавление его в хранилище сертификатов с помощью [**цертаддсериализеделементтосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore).</span><span class="sxs-lookup"><span data-stu-id="36db1-113">Creating a new certificate from a serialized string and adding it into a certificate store using [**CertAddSerializedElementToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore).</span></span>
-   <span data-ttu-id="36db1-114">Использование [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore) для создания нового сертификата из закодированной части существующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="36db1-114">Using [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore) to create a new certificate from the encoded portion of an existing certificate.</span></span>
-   <span data-ttu-id="36db1-115">Использование [**цертклосесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) для закрытия хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="36db1-115">Using [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) to close a certificate store.</span></span>


```C++
//------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Example that uses CertSerializeCertificateStoreElement to
// serialize the data from a certificate, 
// and CertAddSerializedElementToStore to add that data as a new
// certificate to a store.
// CertAddEncodeCertificateToStore is also demonstrated.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE         hSystemStore;
HCERTSTORE         hFileStore;
PCCERT_CONTEXT     pCertContext = NULL;
char               pszNameString[256]; 
BYTE*              pbElement;
DWORD              cbElement;

//-------------------------------------------------------------------
// Open a system certificate store.

if(hSystemStore = CertOpenSystemStore(
    0,
    "CA"))
{
  printf("The CA system store is open. Continue.\n");
}
else
{
  MyHandleError("The first system store did not open.");
}
//-------------------------------------------------------------------
// Open a second store.
// In order to work, a file-based certificate store named 
// teststor.sto must be available in the working directory.

if(hFileStore = CertOpenStore(
   CERT_STORE_PROV_FILENAME,
   MY_ENCODING_TYPE,
   NULL,
   0,
   L"testStor.sto" ))
{
     printf("The file store is open. Continue.\n");
}
else
{
     MyHandleError("The file store did not open.");
}
//-------------------------------------------------------------------
// Retrieve the first certificate from the Root store.
// CertFindCertificateInStore could be used here to find
// a certificate with a specific property.

if(pCertContext=CertEnumCertificatesInStore(
    hSystemStore,
    pCertContext))
{
printf("A certificate is available. Continue.\n");
}
else
{
     MyHandleError("No certificate available. "
         "The store may be empty.");
}
//-------------------------------------------------------------------
//  Find and print the name of the subject of the certificate 
//  just retrieved.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
     printf("Certificate for %s has been retrieved.\n",
         pszNameString);
}
else
{
     printf("CertGetName failed. \n");
}
//-------------------------------------------------------------------
// Find out how much memory to allocate for the serialized element.

if(CertSerializeCertificateStoreElement(
    pCertContext,      // The existing certificate.
    0,                 // Accept default for dwFlags, 
    NULL,              // NULL for the first function call.
    &cbElement))       // Address where the length of the 
                       // serialized element will be placed.
{
     printf("The length of the serialized string is %d.\n",
         cbElement);
}
else
{
     MyHandleError("Finding the length of the serialized "
         "element failed.");
}
//-------------------------------------------------------------------
// Allocate memory for the serialized element.

if(pbElement = (BYTE*)malloc(cbElement))
{
     printf("Memory has been allocated. Continue.\n");
}
else
{
     MyHandleError("The allocation of memory failed.");
}
//-------------------------------------------------------------------
// Create the serialized element from a certificate context.

if(CertSerializeCertificateStoreElement(
    pCertContext,        // The certificate context source for the 
                         // serialized element.
    0,                   // dwFlags. Accept the default.
    pbElement,           // A pointer to where the new element will
                         // be stored.
    &cbElement))         // The length of the serialized element,
{
     printf("The encoded element has been serialized. \n");
}
else
{
     MyHandleError("The element could not be serialized.");
}
//-------------------------------------------------------------------
//  pbElement could be written to a file or be sent by email
//  to another user. 
//  The following process uses the serialized 
//  pbElement and its length, cbElement, to 
//  add a new certificate to a store.

if(CertAddSerializedElementToStore(
    hFileStore,          // Store where certificate is to be added.
    pbElement,           // The serialized element for another
                         // certificate. 
    cbElement,           // The length of pbElement.  
    CERT_STORE_ADD_REPLACE_EXISTING,
                         // Flag to indicate what to do if a matching
                         // certificate is already in the store.
    0,                   // dwFlags. Accept the default.
    CERT_STORE_CERTIFICATE_CONTEXT_FLAG, 
    NULL,
    NULL
    ))
{
     printf("The new certificate is added to the second store.\n");
}
else
{
     MyHandleError("The new element was not added to a store.");
}
//-------------------------------------------------------------------
//  Next, another certificate will be retrieved from the system store
//  and its encoded part, pCertContext->pbCertEncoded, will be
//  used to create a new certificate to be added to the file store.

if(pCertContext=CertEnumCertificatesInStore(
    hSystemStore,
    pCertContext))
{
printf("Another certificate is available. Continue.\n");
}
else
{
     MyHandleError("No certificate is available. "
         "The store may be empty.");
}

//-------------------------------------------------------------------
//  Find and print the name of the subject of the certificate 
//  just retrieved.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
     printf("Certificate for %s has been retrieved.\n",
         pszNameString);
}
else
{
     printf("CertGetName failed. \n");
}
//-------------------------------------------------------------------
//  Create a new certificate from the encoded portion of pCertContext
//  and add it to the file-based store.

if(CertAddEncodedCertificateToStore(
     hFileStore,
     MY_ENCODING_TYPE,
     pCertContext->pbCertEncoded,
     pCertContext->cbCertEncoded,
     CERT_STORE_ADD_USE_EXISTING,
     NULL))
{
     printf("Another certificate is added to the file store.\n");
}
else
{
     MyHandleError("The new certificate was not added to the "
         "file store.");
}
//-------------------------------------------------------------------
// Free memory.

free(pbElement);
CertCloseStore(hSystemStore,0);
CertCloseStore(hFileStore,0); 
printf("The program ran without error to the end.\n");

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



 

 
