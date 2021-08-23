---
description: В следующем примере показана концепция хранилища коллекций, временное хранилище сертификатов, которое фактически включает в себя содержимое нескольких хранилищ сертификатов.
ms.assetid: 5349222f-ad68-477c-8712-fde16e68f600
title: 'Пример программы на языке C: операции с хранилищем сертификатов коллекции и одного уровня'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52074b58cb96b37b17808cfa8de17e2cd4af3082cf58c7c4312b46eb8eca0e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873874"
---
# <a name="example-c-program-collection-and-sibling-certificate-store-operations"></a>Пример программы на языке C: операции с хранилищем сертификатов коллекции и одного уровня

В следующем примере показана концепция хранилища коллекций, временное [*хранилище сертификатов*](../secgloss/c-gly.md) , которое фактически включает в себя содержимое нескольких хранилищ сертификатов. В коллекцию можно добавить одно или несколько магазинов, которые могут обращаться к содержимому любого из магазинов в коллекции с помощью одного вызова функции.

В этом примере показаны следующие задачи и функции [*CryptoAPI*](../secgloss/c-gly.md) :

-   Открытие и закрытие хранилища коллекций, хранилища памяти и системного хранилища с помощью [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) и [**цертклосесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).
-   Добавление одноуровневого хранилища в хранилище коллекции с помощью [**цертаддсторетоколлектион**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).
-   Поиск сертификатов и ссылок на сертификаты в магазинах, которые соответствуют некоторым критериям с помощью [**цертфиндцертификатеинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).
-   Добавление полученного сертификата в хранилище в памяти с помощью [**цертаддцертификатеконтексттосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore).
-   Добавление ссылки на сертификат в хранилище с помощью [**цертаддцертификателинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore).
-   Сохранение хранилища в памяти в файл на диске.
-   Открытие и закрытие хранилища сертификатов на основе файлов.
-   Удаление одноуровневого хранилища из коллекции с помощью [**цертремовесторефромколлектион**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection).

В этом примере используется функция [**михандлиррор**](myhandleerror.md). Код для этой функции включен в пример. Код для этой и других вспомогательных функций также указан в разделе [общего назначения функции](general-purpose-functions.md).

В этом примере используется функция **креатемидакл** , определенная в разделе [Создание DACL](../secbp/creating-a-dacl.md) , чтобы обеспечить создание открытого файла с соответствующим списком DACL.

В следующем примере показано открытие хранилища коллекции, создание нового хранилища сертификатов в памяти и Добавление нового хранилища в качестве одноуровневого хранилища в хранилище коллекции. Затем программа открывает системное хранилище и получает сертификат. Этот сертификат добавляется в хранилище памяти. Второй сертификат извлекается из системного хранилища, а в хранилище памяти добавляется ссылка на этот сертификат. Затем сертификат и ссылка извлекаются из хранилища коллекции, где показаны сертификаты и ссылки в хранилище с общим родителем, которые можно получить из хранилища коллекций. Память сохраняется на диске. Затем хранилище памяти удаляется из коллекции. Ссылка, добавленная в хранилище памяти, по-прежнему может быть найдена в хранилище памяти, но больше не может быть найдена в хранилище коллекции. Все магазины и файлы закрыты, хранилище файлов открывается повторно и выполняется поиск по ссылке на сертификат. Успешное выполнение этой программы зависит от доступного хранилища. Это хранилище должно содержать сертификат с темой "вставить сертификат \_ \_ субъекта \_ Name1" и второй сертификат с темой "вставить \_ сертификат \_ субъекта \_ 2". Имена субъектов следует изменить на имена субъектов сертификата, известных в хранилище My.


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define  MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

HCERTSTORE  hCollectionStore;           // Collection store 
                                        // handle
HCERTSTORE  hSystemStore;               // System store handle
HCERTSTORE  hMemoryStore;               // Memory store handle
PCCERT_CONTEXT  pDesiredCert = NULL;    // Set to NULL for the first 
                                        // call to
                                        // CertFindCertificateInStore
HANDLE hStoreFileHandle ;               // Output file handle
LPWSTR pszFileName = L"TestStor.sto";    // Output file name
SECURITY_ATTRIBUTES sa;                 // for DACL
LPWSTR pswzFirstCert = L"Insert_cert_subject_name1";
                                        // Subject of the first 
                                        // certificate
LPWSTR pswzSecondCert = L"Insert_cert_subject_name2";    
                                        // Subject of the second
                                        // certificate

//-------------------------------------------------------------------
// Open a collection certificate store.

if(hCollectionStore = CertOpenStore(
      CERT_STORE_PROV_COLLECTION, // Collection store
      0,                          // Encoding type 
                                  // Not used with a collection store
      NULL,                       // Use the default provider
      0,                          // No flags
      NULL))                      // Not needed
{
   printf("Opened a collection store. \n");
}
else
{
   MyHandleError( "Error opening the collection store.");
}
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
     L"MY"))                 // System store name
{
   printf("Opened the My system store. \n");
}
else
{
   MyHandleError( "Could not open the My system store.");
}
//-------------------------------------------------------------------
// Get a certificate that has the string
// "Insert_cert_subject_name1" in its subject. 
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hSystemStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzFirstCert,               // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S certificate was found. \n",pswzFirstCert);
}
else
{
   MyHandleError("Could not find the desired certificate.");
}
//-------------------------------------------------------------------
// pDesiredCert is a pointer to a certificate with a subject that 
// includes the string passed as parameter five to the function.

//-------------------------------------------------------------------
// Add the certificate from the My store to the memory store.

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
   MyHandleError("Could not add the certificate to the "
       "memory store.");
}

//-------------------------------------------------------------------
//  Add the memory store as a sibling to the collection store. 
//  All certificates in the memory store will now be available in
//  the collection store. Any new certificates added to the memory 
//  store will also be available in the collection store.

if(CertAddStoreToCollection(
   hCollectionStore,
   hMemoryStore,
   CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG,// New certificates can be
                                       // added to the sibling store
   1))                                 // The sibling store's 
                                       // priority
                                       // because this store has 
                                       // the highest priority, 
                                       // certificates added to
                                       // the collection store will
                                       // actually be stored in this
                                       // store
{
     printf("The memory store is added to the collection store.\n");
}
else
{
     MyHandleError("The memory store was not added "
         "to the collection.");
}
//-------------------------------------------------------------------
//  Find a different certificate in the My store, and add, to the 
//  memory store, a link to that certificate.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hSystemStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzSecondCert,              // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S certificate was found. \n",pswzSecondCert);
}
else
{
   MyHandleError("Could not find the second certificate.");
}
//-------------------------------------------------------------------
// Add a link to a second certificate from the My store to the new 
// memory store.

if(CertAddCertificateLinkToStore(
      hMemoryStore,                // store handle
      pDesiredCert,                // pointer to a certificate
      CERT_STORE_ADD_USE_EXISTING,
      NULL))
{
   printf("%S link added to the memory store. \n",pswzSecondCert);
}
else
{
   MyHandleError("Could not add the certificate link to the "
       "memory store.");
}

//-------------------------------------------------------------------
// Find the first certificate in the memory store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,                // Store handle
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzFirstCert,               // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S certificate was found in the "
      "memory store. \n",pswzFirstCert);
}
else
{
   printf("The %S certificate was not in the "
       "memory store.\n", pswzFirstCert);
}

//-------------------------------------------------------------------
//  Find that same certificate in the collection store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hCollectionStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzFirstCert,               // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S certificate was found in the "
      "collection store. \n", pswzFirstCert);
}
else
{
  printf("The %S certificate was not in the "
      "memory collection.\n", pswzFirstCert);
}

//-------------------------------------------------------------------
//  Find the certificate link in the memory store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hCollectionStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // Mo dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzSecondCert,              // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S link was found in the "
      "collection store. \n", pswzSecondCert);
}
else
{
   printf("The %S certificate link was not in the "
       "memory store.\n", pswzSecondCert);
}

//-------------------------------------------------------------------
// Create a file to save the new store and certificate into.

// Create a DACL for the file.
sa.nLength = sizeof(SECURITY_ATTRIBUTES);
sa.bInheritHandle = FALSE;  

// Call function to set the DACL. The DACL
// is set in the SECURITY_ATTRIBUTES 
// lpSecurityDescriptor member.
// if CreateMyDACL(&sa) fails, call MyHandleError("CreateMyDACL failed.")

if(hStoreFileHandle = CreateFile(
      pszFileName,             // File path
      GENERIC_WRITE,           // Access mode
      0,                       // Share mode
      &sa,                     // Security 
      CREATE_ALWAYS,           // How to create the file
      FILE_ATTRIBUTE_NORMAL,   // File attributes
      NULL))                   // File template
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
      hMemoryStore,            // Store handle
      0,                       // Encoding type not needed here
      CERT_STORE_SAVE_AS_STORE,
      CERT_STORE_SAVE_TO_FILE,
      hStoreFileHandle,        // The handle of an open disk file
      0))                      // dwFlags--no flags are needed here
{
   printf("Saved the memory store to disk. \n");
}
else
{
   MyHandleError("Could not save the memory store to disk.");
}
//-------------------------------------------------------------------
//  Remove the sibling store from the collection.
//  CertRemoveStoreFromCollection returns void.

printf("\nRemoving the memory store from the collection.\n");
CertRemoveStoreFromCollection(
    hCollectionStore,
    hMemoryStore);

//-------------------------------------------------------------------
//   Find the link in the memory store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzSecondCert,              // Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S link is still in the "
      "memory store. \n", pswzSecondCert);
}
else
{
   printf("The certificate link was not in the "
       "memory store.\n");
}
//-------------------------------------------------------------------
//  Try to find certificate link in the collection store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hCollectionStore,
      MY_ENCODING_TYPE,            
      0, 
      CERT_FIND_SUBJECT_STR,    
      pswzSecondCert,
      NULL))       
{
  printf("The %S link was found in the "
      "collection store. \n", pswzSecondCert);
}
else
{
   printf("Removing the store from the collection worked.\n");
   printf("The %S link is not in the "
       "collection store.\n",pswzSecondCert);
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
//  Find the certificate link in the reopened file store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            
      0,                          
      CERT_FIND_SUBJECT_STR,      
      pswzSecondCert,              
      NULL))                       
{
  printf("The %S certificate link was found in the "
      "file store. \n",pswzSecondCert);
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

printf("All of the stores and files are closed. \n");

} // End of main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function, to print an error message to the standard error 
// (stderr) file and exit the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // End of MyHandleError
```



 

 
