---
description: Список всех сертификатов в системном хранилище сертификатов, имя субъекта и все свойства контекста сертификата для каждого из этих сертификатов.
ms.assetid: 4b5361f5-79b1-4b05-a133-1a394da7d6ee
title: Пример программы на языке C. Вывод списка сертификатов в хранилище
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504fe54bea81663957274844c4896b53a25217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911275"
---
# <a name="example-c-program-listing-the-certificates-in-a-store"></a><span data-ttu-id="398d4-103">Пример программы на языке C. Вывод списка сертификатов в хранилище</span><span class="sxs-lookup"><span data-stu-id="398d4-103">Example C Program: Listing the Certificates in a Store</span></span>

<span data-ttu-id="398d4-104">В следующем примере кода выводится список всех сертификатов в системном [*хранилище сертификатов*](../secgloss/c-gly.md) , имя субъекта и все свойства [*контекста сертификата*](../secgloss/c-gly.md) каждого из этих сертификатов.</span><span class="sxs-lookup"><span data-stu-id="398d4-104">The following example code lists all of the certificates in a system [*certificate store*](../secgloss/c-gly.md) and the name of the subject and all of the [*certificate context*](../secgloss/c-gly.md) properties of each of those certificates.</span></span> <span data-ttu-id="398d4-105">Пример получает имя хранилища сертификатов от пользователя и, таким образом, может использоваться для получения списка содержимого любого системного хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="398d4-105">The example gets the name of the certificate store from the user and thus can be used to list the contents of any system certificate store.</span></span> <span data-ttu-id="398d4-106">Кроме того, в этом примере показано использование двух новых функций пользовательского интерфейса, в которых отображается сертификат, а другой — пользовательский интерфейс, позволяющий пользователю выбрать сертификат из списка сертификатов в хранилище.</span><span class="sxs-lookup"><span data-stu-id="398d4-106">In addition, this example shows the use of two new UI functions, one that displays a certificate and the other, UI that allows the user to select a certificate from a list of the certificates in a store.</span></span>

<span data-ttu-id="398d4-107">В этом примере кода показаны следующие задачи и функции [*CryptoAPI*](../secgloss/c-gly.md) :</span><span class="sxs-lookup"><span data-stu-id="398d4-107">This example code illustrates the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="398d4-108">Открытие системного хранилища с помощью [**цертопенсистемсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).</span><span class="sxs-lookup"><span data-stu-id="398d4-108">Opening a system store using [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).</span></span>
-   <span data-ttu-id="398d4-109">В цикле перечислите все сертификаты в открытом хранилище с помощью [**цертенумцертификатесинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).</span><span class="sxs-lookup"><span data-stu-id="398d4-109">In a loop, enumerating all of the certificates in the open store using [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).</span></span>
-   <span data-ttu-id="398d4-110">Отображение сертификата с помощью [**криптуидлгвиевконтекст**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext).</span><span class="sxs-lookup"><span data-stu-id="398d4-110">Displaying a certificate using [**CryptUIDlgViewContext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext).</span></span>
-   <span data-ttu-id="398d4-111">Получение имени субъекта сертификата с помощью [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="398d4-111">Getting the name of the certificate's subject using [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>
-   <span data-ttu-id="398d4-112">В цикле с помощью [**цертенумцертификатеконтекстпропертиес**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) можно получить идентификаторы свойств всех свойств, связанных с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="398d4-112">In a loop, using [**CertEnumCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) to get the property identifiers of all of the properties associated with the certificate.</span></span>
-   <span data-ttu-id="398d4-113">Использование [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) для получения каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="398d4-113">Using [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) to get each of the properties.</span></span>
-   <span data-ttu-id="398d4-114">Отображение списка сертификатов в хранилище и предоставление пользователю возможности выбора одного из них с помощью [**криптуидлгселектцертификатефромсторе**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore).</span><span class="sxs-lookup"><span data-stu-id="398d4-114">Displaying a list of certificates in a store and allowing a user to select one of them using [**CryptUIDlgSelectCertificateFromStore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore).</span></span>
-   <span data-ttu-id="398d4-115">Закрытие хранилища сертификатов с помощью [**цертклосесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).</span><span class="sxs-lookup"><span data-stu-id="398d4-115">Closing the certificate store using [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).</span></span>

<span data-ttu-id="398d4-116">В этом примере используется функция [**михандлиррор**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="398d4-116">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="398d4-117">Код для этой функции включен в пример.</span><span class="sxs-lookup"><span data-stu-id="398d4-117">Code for this function is included with the sample.</span></span>

<span data-ttu-id="398d4-118">Код для этой и других вспомогательных функций также указан в разделе [общего назначения функции](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="398d4-118">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>

<span data-ttu-id="398d4-119">В следующем примере показано перечисление и отображение сертификатов в хранилище.</span><span class="sxs-lookup"><span data-stu-id="398d4-119">The following example shows enumerating and displaying the certificates in a store.</span></span> <span data-ttu-id="398d4-120">Чтобы скомпилировать этот пример, необходимо настроить компилятор для использования многобайтовой кодировки.</span><span class="sxs-lookup"><span data-stu-id="398d4-120">To compile this example, you must configure your compiler to use a multiple-byte character set.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <wincrypt.h>
#include <cryptuiapi.h>

#include <tchar.h>

#pragma comment (lib, "crypt32.lib")
#pragma comment (lib, "cryptui.lib")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// This program lists all of the certificates in a system certificate
// store and all of the property identifier numbers of those 
// certificates. It also demonstrates the use of two
// UI functions. One, CryptUIDlgSelectCertificateFromStore, 
// displays the certificates in a store
// and allows the user to select one of them, 
// The other, CryptUIDlgViewContext,
// displays the contents of a single certificate.

//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE       hCertStore;        
PCCERT_CONTEXT   pCertContext=NULL;      
char pszNameString[256];
char pszStoreName[256];
void*            pvData;
DWORD            cbData;
DWORD            dwPropId = 0; 
            // Zero must be used on the first
            // call to the function. After that,
            // the last returned property identifier is passed.

//-------------------------------------------------------------------
//  Begin processing and Get the name of the system certificate store 
//  to be enumerated. Output here is to stderr so that the program  
//  can be run from the command line and stdout can be redirected  
//  to a file.

fprintf(stderr,"Please enter the store name:");
gets_s(pszStoreName, sizeof(pszStoreName));
fprintf(stderr,"The store name is %s.\n",pszStoreName);

//-------------------------------------------------------------------
// Open a system certificate store.

if ( hCertStore = CertOpenSystemStore(
     NULL,
     pszStoreName))
{
     fprintf(stderr,"The %s store has been opened. \n", 
          pszStoreName);
}
else
{
// If the store was not opened, exit to an error routine.
     MyHandleError("The store was not opened.");
}

//-------------------------------------------------------------------
// Use CertEnumCertificatesInStore to get the certificates 
// from the open store. pCertContext must be reset to
// NULL to retrieve the first certificate in the store.
 
// pCertContext = NULL;

while(pCertContext= CertEnumCertificatesInStore(
     hCertStore,
     pCertContext))
{
//-------------------------------------------------------------------
// A certificate was retrieved. Continue.
//-------------------------------------------------------------------
//  Display the certificate.

if ( CryptUIDlgViewContext(
  CERT_STORE_CERTIFICATE_CONTEXT,
  pCertContext,
  NULL,
  NULL,
  0,
  NULL))
{
//     printf("OK\n");
}
else
{
    MyHandleError("UI failed.");
}

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
   fprintf(stderr,"CertGetName failed. \n");

//-------------------------------------------------------------------
// Loop to find all of the property identifiers for the specified  
// certificate. The loop continues until 
// CertEnumCertificateContextProperties returns zero.

while(dwPropId = CertEnumCertificateContextProperties(
       pCertContext, // The context whose properties are to be listed.
       dwPropId))    // Number of the last property found.  
                     // This must be zero to find the first 
                     // property identifier.
{
//-------------------------------------------------------------------
// When the loop is executed, a property identifier has been found.
// Print the property number.

   printf("Property # %d found->", dwPropId);

//-------------------------------------------------------------------
// Indicate the kind of property found.

   switch(dwPropId)
   {
     case CERT_FRIENDLY_NAME_PROP_ID:
     {
       printf("Display name: ");
       break;
     }
     case CERT_SIGNATURE_HASH_PROP_ID:
     {
       printf("Signature hash identifier ");
       break;
     }
     case CERT_KEY_PROV_HANDLE_PROP_ID:
     {
       printf("KEY PROVE HANDLE");
       break;
     }
     case CERT_KEY_PROV_INFO_PROP_ID:
     {
       printf("KEY PROV INFO PROP ID ");
       break;
     }
     case CERT_SHA1_HASH_PROP_ID:
     {
        printf("SHA1 HASH identifier");
        break;
     }
     case CERT_MD5_HASH_PROP_ID:
     {
        printf("md5 hash identifier ");
        break;
     }
     case CERT_KEY_CONTEXT_PROP_ID:
     {
        printf("KEY CONTEXT PROP identifier");
        break;
     }
     case CERT_KEY_SPEC_PROP_ID:
     {
        printf("KEY SPEC PROP identifier");
        break;
      }
      case CERT_ENHKEY_USAGE_PROP_ID:
      {
        printf("ENHKEY USAGE PROP identifier");
        break;
      }
      case CERT_NEXT_UPDATE_LOCATION_PROP_ID:
      {
        printf("NEXT UPDATE LOCATION PROP identifier");
        break;
      }
      case CERT_PVK_FILE_PROP_ID:
      {
         printf("PVK FILE PROP identifier ");
         break;
      }
      case CERT_DESCRIPTION_PROP_ID:
      {
        printf("DESCRIPTION PROP identifier ");
        break;
      }
      case CERT_ACCESS_STATE_PROP_ID:
      {
        printf("ACCESS STATE PROP identifier ");
        break;
      }
      case CERT_SMART_CARD_DATA_PROP_ID:
      {
         printf("SMART_CARD DATA PROP identifier ");
         break;
      }
      case CERT_EFS_PROP_ID:
      {
        printf("EFS PROP identifier ");
        break;
      }
      case CERT_FORTEZZA_DATA_PROP_ID:
      {
        printf("FORTEZZA DATA PROP identifier ");
        break;
      }
      case CERT_ARCHIVED_PROP_ID:
      {
        printf("ARCHIVED PROP identifier ");
        break;
      }
      case CERT_KEY_IDENTIFIER_PROP_ID:
      {
        printf("KEY IDENTIFIER PROP identifier ");
        break;
      }
      case CERT_AUTO_ENROLL_PROP_ID:
      {
        printf("AUTO ENROLL identifier. ");
        break;
      }
   } // End switch.

//-------------------------------------------------------------------
// Retrieve information on the property by first getting the 
// property size. 
// For more information, see CertGetCertificateContextProperty.

   if(CertGetCertificateContextProperty(
         pCertContext, 
         dwPropId , 
         NULL, 
         &cbData))
    {
    //  Continue.
    }
    else
    {  
    // If the first call to the function failed,
    // exit to an error routine.
        MyHandleError("Call #1 to GetCertContextProperty failed.");
    }
//-------------------------------------------------------------------
// The call succeeded. Use the size to allocate memory 
// for the property.
   
   if(pvData = (void*)malloc(cbData))
   {
   // Memory is allocated. Continue.
   }
   else
   {
   // If memory allocation failed, exit to an error routine.
      MyHandleError("Memory allocation failed.");
   }
   //----------------------------------------------------------------
   // Allocation succeeded. Retrieve the property data.
   
   if(CertGetCertificateContextProperty(
      pCertContext,
      dwPropId,
      pvData, 
      &cbData))
    {
    // The data has been retrieved. Continue.
    }
    else
    {
    // If an error occurred in the second call, 
    // exit to an error routine.
      MyHandleError("Call #2 failed.");
    }
    //---------------------------------------------------------------
    // Show the results.

   printf("The Property Content is %d \n", pvData);
     
   //----------------------------------------------------------------
   // Free the certificate context property memory.
    
   free(pvData);
  }  // End inner while.
} // End outer while.

//-------------------------------------------------------------------
// Select a new certificate by using the user interface.

if(!(pCertContext = CryptUIDlgSelectCertificateFromStore(
  hCertStore,
  NULL,
  NULL,
  NULL,
  CRYPTUI_SELECT_LOCATION_COLUMN,
  0,
  NULL)))
{
    MyHandleError("Select UI failed." );
}


//-------------------------------------------------------------------
// Clean up.

CertFreeCertificateContext(pCertContext);
CertCloseStore(hCertStore,0);
printf("The function completed successfully. \n");
} // End of main.


void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.
```



 

 
