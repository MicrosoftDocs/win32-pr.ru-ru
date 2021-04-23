---
description: В следующем примере выводится список сертификатов в хранилище системных сертификатов, в котором отображается имя субъекта каждого сертификата, и он позволяет пользователю выбрать удаление сертификатов из хранилища.
ms.assetid: 52a0287b-7d2a-483e-8bbc-43621c4b7103
title: Пример программы на языке C. Удаление сертификатов из хранилища сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29f55d27bf2a85d82e4ab96e51fe5368c9de935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909399"
---
# <a name="example-c-program-deleting-certificates-from-a-certificate-store"></a><span data-ttu-id="9fb46-103">Пример программы на языке C. Удаление сертификатов из хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="9fb46-103">Example C Program: Deleting Certificates from a Certificate Store</span></span>

<span data-ttu-id="9fb46-104">В следующем примере выводится список сертификатов в [*хранилище системных сертификатов*](../secgloss/c-gly.md), в котором отображается имя субъекта каждого сертификата, и он позволяет пользователю выбрать удаление сертификатов из хранилища.</span><span class="sxs-lookup"><span data-stu-id="9fb46-104">The following example lists the certificates in a system [*certificate store*](../secgloss/c-gly.md), displaying the name of the subject of each certificate, and it allows the user to choose to delete any certificates from the store.</span></span> <span data-ttu-id="9fb46-105">Пример получает имя хранилища сертификатов от пользователя и, таким образом, может использоваться для хранения содержимого любого системного хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="9fb46-105">The example gets the name of the certificate store from the user and thus can be used to maintain the contents of any system certificate store.</span></span>

<span data-ttu-id="9fb46-106">В этом примере показаны следующие задачи и функции [*CryptoAPI*](../secgloss/c-gly.md) :</span><span class="sxs-lookup"><span data-stu-id="9fb46-106">This example illustrates the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="9fb46-107">Открытие хранилища сертификатов системы с помощью [**цертопенсистемсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).</span><span class="sxs-lookup"><span data-stu-id="9fb46-107">Opening a system certificate store using [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).</span></span>
-   <span data-ttu-id="9fb46-108">Перечисление сертификатов в хранилище сертификатов с помощью [**цертенумцертификатесинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).</span><span class="sxs-lookup"><span data-stu-id="9fb46-108">Listing the certificates in a certificate store using [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).</span></span>
-   <span data-ttu-id="9fb46-109">Получение имени субъекта сертификата с помощью [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="9fb46-109">Getting the name of the subject of a certificate using [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>
-   <span data-ttu-id="9fb46-110">Сравнение имени субъекта сертификата с именем издателя сертификата с помощью [**церткомпарецертификатенаме**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename).</span><span class="sxs-lookup"><span data-stu-id="9fb46-110">Comparing the name of the subject of the certificate with the name of the issuer of the certificate using [**CertCompareCertificateName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename).</span></span>
-   <span data-ttu-id="9fb46-111">Проверка того, соответствует ли открытый ключ текущего сертификата открытому ключу предыдущего сертификата с помощью [**церткомпарепубликкэйинфо**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo).</span><span class="sxs-lookup"><span data-stu-id="9fb46-111">Checking to determine whether the public key of the current certificate matches the public key of a previous certificate using [**CertComparePublicKeyInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo).</span></span>
-   <span data-ttu-id="9fb46-112">Дублирование указателя на [*контекст сертификата*](../secgloss/c-gly.md) с помощью [**цертдупликатецертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext).</span><span class="sxs-lookup"><span data-stu-id="9fb46-112">Duplicating a pointer to a [*certificate context*](../secgloss/c-gly.md) using [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext).</span></span>
-   <span data-ttu-id="9fb46-113">Сравнение членов [**сертификата \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) каждого сертификата с помощью [**церткомпарецертификате**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate).</span><span class="sxs-lookup"><span data-stu-id="9fb46-113">Comparing the [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) members of each certificate using [**CertCompareCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate).</span></span>
-   <span data-ttu-id="9fb46-114">Удаление сертификата из хранилища с помощью [**цертделетецертификатефромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore).</span><span class="sxs-lookup"><span data-stu-id="9fb46-114">Deleting a certificate from a store using [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore).</span></span>
-   <span data-ttu-id="9fb46-115">Закрытие хранилища сертификатов с помощью [**цертклосесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).</span><span class="sxs-lookup"><span data-stu-id="9fb46-115">Closing a certificate store using [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).</span></span>

<span data-ttu-id="9fb46-116">Этот пример получает имя системного хранилища сертификатов от пользователя, открывает хранилище и проходит по сертификатам в этом хранилище.</span><span class="sxs-lookup"><span data-stu-id="9fb46-116">This example gets the name of a system certificate store from the user, opens that store, and goes through the certificates in that store.</span></span> <span data-ttu-id="9fb46-117">Для каждого сертификата отображается имя субъекта сертификата, и пользователю предоставляется возможность удалить этот сертификат.</span><span class="sxs-lookup"><span data-stu-id="9fb46-117">For each certificate, the name of the certificate's subject is displayed and the user is given an option to delete that certificate.</span></span>


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
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

HANDLE          hStoreHandle;
PCCERT_CONTEXT  pCertContext=NULL;   
PCCERT_CONTEXT  pDupCertContext; 
PCERT_PUBLIC_KEY_INFO pOldPubKey = NULL;
PCERT_PUBLIC_KEY_INFO pNewPubKey; 
char pszStoreName[256];
char pszNameString[256];
char fResponse ='n';  
char x;

//-------------------------------------------------------------------
// Get the name of the certificate store to open. 
printf("This program maintains the contents of a certificate\n");
printf("store by allowing you to delete any excess certificates\n");
printf("from a store. \n\n");
printf("Please enter the name of the system store to maintain:");
fgets(pszStoreName, 255, stdin);
if (pszStoreName[strlen(pszStoreName) - 1] =='\n')
   pszStoreName[strlen(pszStoreName) - 1] = '\0';
printf("Certificates will be deleted from "
       "the %s store.\n",pszStoreName);

//-------------------------------------------------------------------
// Open a system certificate store.

if ( hStoreHandle = CertOpenSystemStore(
     NULL,     
     pszStoreName))
{
     printf("The %s store has been opened. \n", pszStoreName);
}
else
{
     MyHandleError("The store was not opened.");
}
//-------------------------------------------------------------------
// Find the certificates in the system store. 

while(pCertContext= CertEnumCertificatesInStore(
    hStoreHandle,
    pCertContext)) // on the first call to the function,
                   //  this parameter is NULL
                   // on all subsequent
                   //  calls, it is the last pointer returned by 
                   //  the function
{
//-------------------------------------------------------------------
// Get and display the name of the subject of the certificate.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
   printf("\nCertificate for %s \n",pszNameString);
}
else
{
   MyHandleError("CertGetName failed.");
}
//-------------------------------------------------------------------
// Check to determine whether the issuer 
// and the subject are the same.

if(CertCompareCertificateName(
   MY_ENCODING_TYPE,
   &(pCertContext->pCertInfo->Issuer),
   &(pCertContext->pCertInfo->Subject)))
{
     printf("The certificate subject and issuer are the same.\n");
}
else
{
     printf("The certificate subject and issuer "
         "are not the same.\n");
}
//--------------------------------------------------------------------
// Determine whether this certificate's public key matches 
// the public key of the last certificate.

pNewPubKey = &(pCertContext->pCertInfo->SubjectPublicKeyInfo);
if(pOldPubKey)
   if(CertComparePublicKeyInfo(
       MY_ENCODING_TYPE,
       pOldPubKey,
       pNewPubKey))
   {
       printf("The public keys are the same.\n");
   }
   else
   {
       printf("This certificate has a different public key.\n");
   }
//-------------------------------------------------------------------
// Reset the old key.

pOldPubKey = pNewPubKey;

//-------------------------------------------------------------------
// Determine whether this certificate is to be deleted. 

printf("Would you like to delete this certificate? (y/n) ");
fResponse = getchar();
if(fResponse == 'y')
{
   //----------------------------------------------------------------
   // Create a duplicate pointer to the certificate to be 
   // deleted. In this way, the original pointer is not freed 
   // when the certificate is deleted from the store 
   // and the enumeration of the certificates in the store can
   // continue. If the original pointer is used, after the 
   // certificate is deleted, the enumeration loop stops.

   if(pDupCertContext = CertDuplicateCertificateContext(
      pCertContext))
   {
       printf("A duplicate pointer was created. Continue. \n");
   }
   else
   {
        MyHandleError("Duplication of the certificate "
            "pointer failed.");
   }

//-------------------------------------------------------------------
// Compare the pCertInfo members of the two certificates 
// to determine whether they are identical.

if(CertCompareCertificate(
      X509_ASN_ENCODING,
      pDupCertContext->pCertInfo, 
      pCertContext->pCertInfo))
{
     printf("The two certificates are identical. \n");
}
else
{
     printf("The two certificates are not identical. \n");
}
//-------------------------------------------------------------------
// Delete the certificate.
   if(CertDeleteCertificateFromStore(
     pDupCertContext))   
   {
       printf("The certificate has been deleted. Continue. \n");
   }
   else
   {
      printf("The deletion of the certificate failed.\n");
   }
} // end if

//-------------------------------------------------------------------
// Clear the input buffer.

x = getchar();

} // end while

//-------------------------------------------------------------------
// Clean up.

CertCloseStore(
   hStoreHandle,
   0);
printf("The program ran to completion successfully. \n");
} // end main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
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



 

 
