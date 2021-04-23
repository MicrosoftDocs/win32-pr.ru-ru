---
description: Используется для проверки того, что сообщение не было изменено во время передачи.
ms.assetid: a4bb67fb-8217-4e76-b1bf-461ccd39f58a
title: Пример программы на языке C. Создание HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a18da226c9e88d535b34fe9c319a042132749e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544215"
---
# <a name="example-c-program-creating-an-hmac"></a><span data-ttu-id="2e3b8-103">Пример программы на языке C. Создание HMAC</span><span class="sxs-lookup"><span data-stu-id="2e3b8-103">Example C Program: Creating an HMAC</span></span>

<span data-ttu-id="2e3b8-104">Хэшированная контрольная сумма проверки подлинности сообщений (HMAC) обычно используется для проверки того, что сообщение не было изменено во время передачи.</span><span class="sxs-lookup"><span data-stu-id="2e3b8-104">A hashed message authentication checksum (HMAC) is typically used to verify that a message has not been changed during transit.</span></span> <span data-ttu-id="2e3b8-105">Обе стороны к сообщению должны иметь общий секретный ключ.</span><span class="sxs-lookup"><span data-stu-id="2e3b8-105">Both parties to the message must have a shared secret key.</span></span> <span data-ttu-id="2e3b8-106">Отправитель объединяет ключ и сообщение в строку, создает дайджест строки с помощью алгоритма, такого как SHA-1 или MD5, и передает сообщение и дайджест.</span><span class="sxs-lookup"><span data-stu-id="2e3b8-106">The sender combines the key and the message into a string, creates a digest of the string by using an algorithm such as SHA-1 or MD5, and transmits the message and the digest.</span></span> <span data-ttu-id="2e3b8-107">Получатель объединяет общий ключ с сообщением, применяет соответствующий алгоритм и сравнивает дайджест, полученный с передачей отправителя.</span><span class="sxs-lookup"><span data-stu-id="2e3b8-107">The receiver combines the shared key with the message, applies the appropriate algorithm, and compares the digest thus obtained with that transmitted by the sender.</span></span> <span data-ttu-id="2e3b8-108">Если дайджесты одинаковы, сообщение не было изменено.</span><span class="sxs-lookup"><span data-stu-id="2e3b8-108">If the digests are exactly the same, the message was not tampered with.</span></span>

<span data-ttu-id="2e3b8-109">В этом примере демонстрируются следующие задачи и функции CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="2e3b8-109">This example demonstrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="2e3b8-110">Получение маркера для [*поставщика служб шифрования*](../secgloss/c-gly.md) путем вызова [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span><span class="sxs-lookup"><span data-stu-id="2e3b8-110">Acquiring a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) by calling [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="2e3b8-111">Получение симметричного ключа из строки с байтами путем вызова [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash), [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)и [**криптдеривекэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span><span class="sxs-lookup"><span data-stu-id="2e3b8-111">Deriving a symmetric key from a byte string by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash), [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata), and [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span></span>
-   <span data-ttu-id="2e3b8-112">Использование симметричного ключа для создания хэш-объекта HMAC путем вызова [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) и [**криптсесашпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span><span class="sxs-lookup"><span data-stu-id="2e3b8-112">Using the symmetric key to create an HMAC hash object by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) and [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span></span>
-   <span data-ttu-id="2e3b8-113">Хэширование сообщения путем вызова [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).</span><span class="sxs-lookup"><span data-stu-id="2e3b8-113">Hashing a message by calling [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).</span></span>
-   <span data-ttu-id="2e3b8-114">Получение хэша путем вызова [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam).</span><span class="sxs-lookup"><span data-stu-id="2e3b8-114">Retrieving the hash by calling [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam).</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <wincrypt.h>

int main()
{
//--------------------------------------------------------------------
// Declare variables.
//
// hProv:           Handle to a cryptographic service provider (CSP). 
//                  This example retrieves the default provider for  
//                  the PROV_RSA_FULL provider type.  
// hHash:           Handle to the hash object needed to create a hash.
// hKey:            Handle to a symmetric key. This example creates a 
//                  key for the RC4 algorithm.
// hHmacHash:       Handle to an HMAC hash.
// pbHash:          Pointer to the hash.
// dwDataLen:       Length, in bytes, of the hash.
// Data1:           Password string used to create a symmetric key.
// Data2:           Message string to be hashed.
// HmacInfo:        Instance of an HMAC_INFO structure that contains 
//                  information about the HMAC hash.
// 
HCRYPTPROV  hProv       = NULL;
HCRYPTHASH  hHash       = NULL;
HCRYPTKEY   hKey        = NULL;
HCRYPTHASH  hHmacHash   = NULL;
PBYTE       pbHash      = NULL;
DWORD       dwDataLen   = 0;
BYTE        Data1[]     = {0x70,0x61,0x73,0x73,0x77,0x6F,0x72,0x64};
BYTE        Data2[]     = {0x6D,0x65,0x73,0x73,0x61,0x67,0x65};
HMAC_INFO   HmacInfo;

//--------------------------------------------------------------------
// Zero the HMAC_INFO structure and use the SHA1 algorithm for
// hashing.

ZeroMemory(&HmacInfo, sizeof(HmacInfo));
HmacInfo.HashAlgid = CALG_SHA1;

//--------------------------------------------------------------------
// Acquire a handle to the default RSA cryptographic service provider.

if (!CryptAcquireContext(
    &hProv,                   // handle of the CSP
    NULL,                     // key container name
    NULL,                     // CSP name
    PROV_RSA_FULL,            // provider type
    CRYPT_VERIFYCONTEXT))     // no key access is requested
{
   printf(" Error in AcquireContext 0x%08x \n",
          GetLastError());
   goto ErrorExit;
}

//--------------------------------------------------------------------
// Derive a symmetric key from a hash object by performing the
// following steps:
//    1. Call CryptCreateHash to retrieve a handle to a hash object.
//    2. Call CryptHashData to add a text string (password) to the 
//       hash object.
//    3. Call CryptDeriveKey to create the symmetric key from the
//       hashed password derived in step 2.
// You will use the key later to create an HMAC hash object. 

if (!CryptCreateHash(
    hProv,                    // handle of the CSP
    CALG_SHA1,                // hash algorithm to use
    0,                        // hash key
    0,                        // reserved
    &hHash))                  // address of hash object handle
{
   printf("Error in CryptCreateHash 0x%08x \n",
          GetLastError());
   goto ErrorExit;
}

if (!CryptHashData(
    hHash,                    // handle of the hash object
    Data1,                    // password to hash
    sizeof(Data1),            // number of bytes of data to add
    0))                       // flags
{
   printf("Error in CryptHashData 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

if (!CryptDeriveKey(
    hProv,                    // handle of the CSP
    CALG_RC4,                 // algorithm ID
    hHash,                    // handle to the hash object
    0,                        // flags
    &hKey))                   // address of the key handle
{
   printf("Error in CryptDeriveKey 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

//--------------------------------------------------------------------
// Create an HMAC by performing the following steps:
//    1. Call CryptCreateHash to create a hash object and retrieve 
//       a handle to it.
//    2. Call CryptSetHashParam to set the instance of the HMAC_INFO 
//       structure into the hash object.
//    3. Call CryptHashData to compute a hash of the message.
//    4. Call CryptGetHashParam to retrieve the size, in bytes, of
//       the hash.
//    5. Call malloc to allocate memory for the hash.
//    6. Call CryptGetHashParam again to retrieve the HMAC hash.

if (!CryptCreateHash(
    hProv,                    // handle of the CSP.
    CALG_HMAC,                // HMAC hash algorithm ID
    hKey,                     // key for the hash (see above)
    0,                        // reserved
    &hHmacHash))              // address of the hash handle
{
   printf("Error in CryptCreateHash 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

if (!CryptSetHashParam(
    hHmacHash,                // handle of the HMAC hash object
    HP_HMAC_INFO,             // setting an HMAC_INFO object
    (BYTE*)&HmacInfo,         // the HMAC_INFO object
    0))                       // reserved
{
   printf("Error in CryptSetHashParam 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

if (!CryptHashData(
    hHmacHash,                // handle of the HMAC hash object
    Data2,                    // message to hash
    sizeof(Data2),            // number of bytes of data to add
    0))                       // flags
{
   printf("Error in CryptHashData 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

//--------------------------------------------------------------------
// Call CryptGetHashParam twice. Call it the first time to retrieve
// the size, in bytes, of the hash. Allocate memory. Then call 
// CryptGetHashParam again to retrieve the hash value.

if (!CryptGetHashParam(
    hHmacHash,                // handle of the HMAC hash object
    HP_HASHVAL,               // query on the hash value
    NULL,                     // filled on second call
    &dwDataLen,               // length, in bytes, of the hash
    0))
{
   printf("Error in CryptGetHashParam 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

pbHash = (BYTE*)malloc(dwDataLen);
if(NULL == pbHash) 
{
   printf("unable to allocate memory\n");
   goto ErrorExit;
}
    
if (!CryptGetHashParam(
    hHmacHash,                 // handle of the HMAC hash object
    HP_HASHVAL,                // query on the hash value
    pbHash,                    // pointer to the HMAC hash value
    &dwDataLen,                // length, in bytes, of the hash
    0))
{
   printf("Error in CryptGetHashParam 0x%08x \n", GetLastError());
   goto ErrorExit;
}

// Print the hash to the console.

printf("The hash is:  ");
for(DWORD i = 0 ; i < dwDataLen ; i++) 
{
   printf("%2.2x ",pbHash[i]);
}
printf("\n");

// Free resources.
ErrorExit:
    if(hHmacHash)
        CryptDestroyHash(hHmacHash);
    if(hKey)
        CryptDestroyKey(hKey);
    if(hHash)
        CryptDestroyHash(hHash);    
    if(hProv)
        CryptReleaseContext(hProv, 0);
    if(pbHash)
        free(pbHash);
    return 0;
}

```



 

 
