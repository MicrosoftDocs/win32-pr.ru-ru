---
description: 'Пример программы C: операции с хранилищем сертификатов'
ms.assetid: cf87791c-b98c-4dd7-b346-336c4b1a88ca
title: 'Пример программы C: операции с хранилищем сертификатов'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2f20a56fd04eb79b1ebe2359e3c915d9aad60fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663939"
---
# <a name="example-c-program-certificate-store-operations"></a><span data-ttu-id="c2083-103">Пример программы C: операции с хранилищем сертификатов</span><span class="sxs-lookup"><span data-stu-id="c2083-103">Example C Program: Certificate Store Operations</span></span>

<span data-ttu-id="c2083-104">В следующем примере показано несколько общих операций [*хранилища сертификатов*](../secgloss/c-gly.md) , а также следующие задачи и функции [*CryptoAPI*](../secgloss/c-gly.md) :</span><span class="sxs-lookup"><span data-stu-id="c2083-104">The following example demonstrates a number of common [*certificate store*](../secgloss/c-gly.md) operations as well as the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="c2083-105">Открытие и закрытие памяти и системных хранилищ с помощью [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) и [**цертклосесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).</span><span class="sxs-lookup"><span data-stu-id="c2083-105">Opening and closing memory and system stores using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) and [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).</span></span>
-   <span data-ttu-id="c2083-106">Дублирование открытого хранилища с помощью [**цертдупликатесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore).</span><span class="sxs-lookup"><span data-stu-id="c2083-106">Duplicating an open store using [**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore).</span></span>
-   <span data-ttu-id="c2083-107">Поиск в хранит сертификаты, удовлетворяющие некоторым критериям, с помощью [**цертфиндцертификатеинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span><span class="sxs-lookup"><span data-stu-id="c2083-107">Finding in stores certificates that meet some criteria using [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span></span>
-   <span data-ttu-id="c2083-108">Создание нового контекста сертификата из закодированной части существующего сертификата с помощью [**церткреатецертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext).</span><span class="sxs-lookup"><span data-stu-id="c2083-108">Creating a new certificate context from the encoded portion of an existing certificate using [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext).</span></span>
-   <span data-ttu-id="c2083-109">Добавление полученного сертификата в хранилище в памяти с помощью [**цертаддцертификатеконтексттосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore).</span><span class="sxs-lookup"><span data-stu-id="c2083-109">Adding a retrieved certificate to a store in memory using [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore).</span></span>
-   <span data-ttu-id="c2083-110">Добавление ссылки на сертификат в хранилище с помощью [**цертаддцертификателинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore).</span><span class="sxs-lookup"><span data-stu-id="c2083-110">Adding a link to a certificate to a store using [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore).</span></span>
-   <span data-ttu-id="c2083-111">Сохранение хранилища в памяти в файл на диске.</span><span class="sxs-lookup"><span data-stu-id="c2083-111">Saving the store in memory to a file on disk.</span></span>
-   <span data-ttu-id="c2083-112">Открытие и закрытие хранилища сертификатов на основе файлов.</span><span class="sxs-lookup"><span data-stu-id="c2083-112">Opening and closing a file-based certificate store.</span></span>

<span data-ttu-id="c2083-113">В этом примере используется функция [**михандлиррор**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="c2083-113">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="c2083-114">Код для этой функции включен в пример.</span><span class="sxs-lookup"><span data-stu-id="c2083-114">The code for this function is included with the sample.</span></span> <span data-ttu-id="c2083-115">Код для этой и других вспомогательных функций также указан в разделе [общего назначения функции](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c2083-115">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>

<span data-ttu-id="c2083-116">В этом примере используется функция **креатемидакл** , определенная в разделе [Создание DACL](../secbp/creating-a-dacl.md) , чтобы обеспечить создание открытого файла с соответствующим списком DACL.</span><span class="sxs-lookup"><span data-stu-id="c2083-116">This example uses the **CreateMyDACL** function, defined in the [Creating a DACL](../secbp/creating-a-dacl.md) topic, to ensure the open file is created with a proper DACL.</span></span>

<span data-ttu-id="c2083-117">В этом примере в памяти создается хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c2083-117">This example creates a certificate store in memory.</span></span> <span data-ttu-id="c2083-118">Системное хранилище открывается и дублируется.</span><span class="sxs-lookup"><span data-stu-id="c2083-118">A system store is opened and duplicated.</span></span> <span data-ttu-id="c2083-119">Сертификат извлекается из системного хранилища.</span><span class="sxs-lookup"><span data-stu-id="c2083-119">A certificate is retrieved from the system store.</span></span> <span data-ttu-id="c2083-120">Новый сертификат создается из закодированной части полученного сертификата.</span><span class="sxs-lookup"><span data-stu-id="c2083-120">A new certificate is created from the encoded portion of the certificate retrieved.</span></span> <span data-ttu-id="c2083-121">Полученный сертификат добавляется в хранилище памяти.</span><span class="sxs-lookup"><span data-stu-id="c2083-121">The certificate retrieved is added to the memory store.</span></span> <span data-ttu-id="c2083-122">Второй сертификат извлекается из хранилища My Store, а в хранилище памяти добавляется ссылка на этот сертификат.</span><span class="sxs-lookup"><span data-stu-id="c2083-122">A second certificate is retrieved from the My store and a link to that certificate is added to the memory store.</span></span> <span data-ttu-id="c2083-123">Затем сертификат и ссылка извлекаются из хранилища памяти, а память сохраняется на диск.</span><span class="sxs-lookup"><span data-stu-id="c2083-123">The certificate and the link are then retrieved from the memory store and the memory is saved to disk.</span></span> <span data-ttu-id="c2083-124">Все магазины и файлы закрыты.</span><span class="sxs-lookup"><span data-stu-id="c2083-124">All of the stores and files are closed.</span></span> <span data-ttu-id="c2083-125">Затем хранилище файлов открывается повторно и выполняется поиск по ссылке на сертификат.</span><span class="sxs-lookup"><span data-stu-id="c2083-125">Next, the file store is reopened and a search is done for the certificate link.</span></span> <span data-ttu-id="c2083-126">Успешное выполнение этой программы зависит от доступного хранилища.</span><span class="sxs-lookup"><span data-stu-id="c2083-126">The success of this program depends upon a My store being available.</span></span> <span data-ttu-id="c2083-127">Это хранилище должно содержать сертификат с темой "вставить сертификат \_ \_ субъекта \_ Name1" и второй сертификат с темой "вставить \_ сертификат \_ субъекта \_ 2.".</span><span class="sxs-lookup"><span data-stu-id="c2083-127">That store must include a certificate with the subject "Insert\_cert\_subject\_name1," and a second certificate with the subject "Insert\_cert\_subject\_name2."</span></span> <span data-ttu-id="c2083-128">Имена субъектов необходимо изменить на имена субъектов сертификатов, известных в хранилище My.</span><span class="sxs-lookup"><span data-stu-id="c2083-128">The names of the subjects must be changed to the names of certificate subjects known to be in the My store.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//--------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

HCERTSTORE  hSystemStore;              // System store handle
HCERTSTORE  hMemoryStore;              // Memory store handle
HCERTSTORE  hDuplicateStore;           // Handle for a store to be 
                                       // created
                                       // as a duplicate of an open 
                                       // store
PCCERT_CONTEXT  pDesiredCert = NULL;   // Set to NULL for the first 
                                       // call to
                                       // CertFindCertificateInStore
PCCERT_CONTEXT  pCertContext;
HANDLE  hStoreFileHandle ;             // Output file handle
LPWSTR  pszFileName = L"TestStor.sto";  // Output file name
SECURITY_ATTRIBUTES sa;                // For DACL

//-------------------------------------------------------------------
// Open a new certificate store in memory.

if(hMemoryStore = CertOpenStore(
      CERT_STORE_PROV_MEMORY,    // Memory store
      0,                         // Encoding type
                                 // not used with a memory store
      NULL,                      // Use the default provider
      0,                         // No flags
      NULL))                     // Not needed
{
   printf("Opened a memory store. \n");
}
else
{
   MyHandleError( "Error opening a memory store.");
}
//-------------------------------------------------------------------
// Open the My system store using CertOpenStore.

if(hSystemStore = CertOpenStore(
     CERT_STORE_PROV_SYSTEM, // System store will be a 
                             // virtual store
     0,                      // Encoding type not needed 
                             // with this PROV
     NULL,                   // Accept the default HCRYPTPROV
     CERT_SYSTEM_STORE_CURRENT_USER,
                             // Set the system store location in the
                             // registry
     L"MY"))                 // Could have used other predefined 
                             // system stores
                             // including Trust, CA, or Root
{
   printf("Opened the MY system store. \n");
}
else
{
   MyHandleError( "Could not open the MY system store.");
}
//-------------------------------------------------------------------
// Create a duplicate of the My store.

if(hDuplicateStore = CertDuplicateStore(hSystemStore))
{
  printf("The MY store is duplicated.\n");
}
else
{
  printf("Duplication of the MY store failed.\n.");
}

//-------------------------------------------------------------------
// Close the duplicate store. 

if(hDuplicateStore)
    CertCloseStore(
        hDuplicateStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);


//-------------------------------------------------------------------
// Get a certificate that has the string "Insert_cert_subject_name1" 
// in its subject. 

if(pDesiredCert=CertFindCertificateInStore(
      hSystemStore,
      MY_ENCODING_TYPE,             // Use X509_ASN_ENCODING
      0,                            // No dwFlags needed 
      CERT_FIND_SUBJECT_STR,        // Find a certificate with a
                                    // subject that matches the 
                                    // string in the next parameter
      L"Insert_cert_subject_name1", // The Unicode string to be found
                                    // in a certificate's subject
      NULL))                        // NULL for the first call to the
                                    // function 
                                    // In all subsequent
                                    // calls, it is the last pointer
                                    // returned by the function
{
  printf("The desired certificate was found. \n");
}
else
{
   MyHandleError("Could not find the desired certificate.");
}
//-------------------------------------------------------------------
// pDesiredCert is a pointer to a certificate with a subject that 
// includes the string "Insert_cert_subject_name1", the string is 
// passed as parameter #5 to the function.

//------------------------------------------------------------------ 
//  Create a new certificate from the encoded part of
//  an available certificate.

if(pCertContext = CertCreateCertificateContext(
    MY_ENCODING_TYPE  ,            // Encoding type
    pDesiredCert->pbCertEncoded,   // Encoded data from
                                   // the certificate retrieved
    pDesiredCert->cbCertEncoded))  // Length of the encoded data
{
  printf("A new certificate has been created.\n");
}
else
{
  MyHandleError("A new certificate could not be created.");
}

//-------------------------------------------------------------------
// Add the certificate from the My store to the new memory store.

if(CertAddCertificateContextToStore(
      hMemoryStore,                // Store handle
      pDesiredCert,                // Pointer to a certificate
      CERT_STORE_ADD_USE_EXISTING,
      NULL))
{
   printf("Certificate added to the memory store. \n");
}
else
{
   MyHandleError("Could not add the certificate "
       "to the memory store.");
}
//-------------------------------------------------------------------
// Find a different certificate in the My store, and add to it a link
// to the memory store.

//-------------------------------------------------------------------
// Find the certificate context just added to the memory store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);

if(pDesiredCert=CertFindCertificateInStore(
      hSystemStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // no dwFlags needed 
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the 
                                   // string in the next parameter
      L"Insert_cert_subject_name2",// The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL for the first call to the
                                   // function 
                                   // In all subsequent
                                   // calls, it is the last pointer
                                   // returned by the function
{
  printf("The second certificate was found. \n");
}
else
{
   MyHandleError("Could not find the second certificate.");
}
//-------------------------------------------------------------------
// Add a link to the second certificate from the My store to 
// the new memory store.

if(CertAddCertificateLinkToStore(
      hMemoryStore,           // Store handle
      pDesiredCert,           // Pointer to a certificate
      CERT_STORE_ADD_USE_EXISTING,
      NULL))
{
   printf("Certificate link added to the memory store. \n");
}
else
{
   MyHandleError("Could not add the certificate link to the "
       "memory store.");
}
//--------------------------------------------------------------------
// Find the first certificate in the memory store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);

if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed 
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      L"Insert_cert_subject_name1",// The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL for the first call to the
                                   // function
                                   // In all subsequent
                                   // calls, it is the last pointer
                                   // returned by the function
{
  printf("The desired certificate was found in the "
      "memory store. \n");
}
else
{
   printf("Certificate not in the memory store.\n");
}
//-------------------------------------------------------------------
// Find the certificate link in the memory store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);

if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed 
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the 
                                   // string in the next parameter
      L"Insert_cert_subject_name1",// The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL for the first call to the
                                   // function
                                   // In all subsequent
                                   // calls, it is the last pointer
                                   // returned by the function
{
  printf("The certificate link was found in the memory store. \n");
}
else
{
   printf("The certificate link was not in the memory store.\n");
}
//-------------------------------------------------------------------
// Create a file in which to save the new store and certificate.

// Create a DACL for the file.
sa.nLength = sizeof(SECURITY_ATTRIBUTES);
sa.bInheritHandle = FALSE;  

// Call the function to set the DACL. The DACL
// is set in the SECURITY_ATTRIBUTES 
// lpSecurityDescriptor member.
// if !CreateMyDACL(&sa), call MyHandleError("CreateMyDACL failed.");

if(hStoreFileHandle = CreateFile(
      pszFileName,        // File path
      GENERIC_WRITE,      // Access mode
      0,                  // Share mode
      &sa,                // Security 
      CREATE_ALWAYS,      // How to create the file
      FILE_ATTRIBUTE_NORMAL,
                          // File attributes
      NULL))              // Template
{
   printf("Created a new file on disk. \n");
}
else
{
   MyHandleError("Could not create a file on disk.");
}
//-------------------------------------------------------------------
// hStoreFileHandle is the output file handle.
// Save the memory store and its certificate to the output file.

if( CertSaveStore(
      hMemoryStore,        // Store handle
      0,                   // Encoding type not needed here
      CERT_STORE_SAVE_AS_STORE,
      CERT_STORE_SAVE_TO_FILE,
      hStoreFileHandle,    // This is the handle of an open disk file
      0))                  // dwFlags
                           // No flags needed here
{
   printf("Saved the memory store to disk. \n");
}
else
{
   MyHandleError("Could not save the memory store to disk.");
}
//-------------------------------------------------------------------
// Close the stores and the file. Reopen the file store, 
// and check its contents.

if(hMemoryStore)
    CertCloseStore(
        hMemoryStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);

if(hSystemStore)
    CertCloseStore(
        hSystemStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);

if(hStoreFileHandle)
     CloseHandle(hStoreFileHandle);

printf("All of the stores and files are closed. \n");

//-------------------------------------------------------------------
//  Reopen the file store.

if(hMemoryStore = CertOpenStore(
       CERT_STORE_PROV_FILENAME,    // Store provider type
       MY_ENCODING_TYPE,            // If needed, use the usual
                                    // encoding types
       NULL,                        // Use the default HCRYPTPROV
       0,                           // Accept the default for all
                                    // dwFlags
       L"TestStor.sto" ))           // The name of an existing file
                                    // as a Unicode string
{
     printf("The file store has been reopened. \n");
}
else
{
    printf("The file store could not be reopened. \n");
}
//-------------------------------------------------------------------
// Find the certificate link in the reopened file store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);

if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed 
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      L"Insert_cert_subject_name1",// The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL for the first call to the
                                   // function
                                   // In all subsequent
                                   // calls, it is the last pointer
                                   // returned by the function
{
  printf("The certificate link was found in the file store. \n");
}
else
{
   printf("The certificate link was not in the file store.\n");
}
//-------------------------------------------------------------------
// Clean up memory and end.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(hMemoryStore)
    CertCloseStore(
        hMemoryStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);
if(hSystemStore)
    CertCloseStore(
        hSystemStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);
if(hStoreFileHandle)
     CloseHandle(hStoreFileHandle);
printf("All of the stores and files are closed. \n");
return;
} // end main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function, to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end MyHandleError
```



 

 
