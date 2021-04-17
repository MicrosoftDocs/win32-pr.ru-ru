---
description: Создает и хэширует ключ сеанса, который можно использовать для шифрования сообщения, текста или файла.
ms.assetid: 15d4a05d-5888-4532-91fd-6cd94afe0b99
title: Пример программы на языке C. Создание и хэширование ключа сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbfb1dae0f331a80a2b2c473f0446cf2a1623dda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684349"
---
# <a name="example-c-program-creating-and-hashing-a-session-key"></a>Пример программы на языке C. Создание и хэширование ключа сеанса

В следующем примере создается и [*хэшируется*](../secgloss/h-gly.md) [*ключ сеанса*](../secgloss/s-gly.md) , который можно использовать для шифрования сообщения, текста или файла.

В этом примере также показано использование следующих функций CryptoAPI:

-   [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) получить [*поставщик служб шифрования*](../secgloss/c-gly.md).
-   [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) создать пустой хэш-объект.
-   [**Криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) для создания случайного [*ключа сеанса*](../secgloss/s-gly.md).
-   [**Крипсашсессионкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) для хэширования созданного ключа сеанса.
-   [**Криптдестройхаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) , чтобы уничтожить хэш.
-   [**Криптдестройкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) для уничтожения созданного ключа.
-   [**Криптрелеасеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) , чтобы освободить CSP.

В этом примере используется функция [**михандлиррор**](myhandleerror.md). Код для этой функции включен в пример. Код для этой и других вспомогательных функций также указан в разделе [общего назначения функции](general-purpose-functions.md).


```C++
//  Copyright (C) Microsoft. All rights reserved.
//  
//  CreateAndHashSessionKey.cpp : Defines the entry point for the 
//  application.
//

#include <stdafx.h>

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(LPTSTR psz);

void main()
{
    HCRYPTPROV hCryptProv;
    HCRYPTHASH hHash;
    HCRYPTKEY hKey;

    //---------------------------------------------------------------
    // Acquire a cryptographic provider context handle.
    if(CryptAcquireContext(
        &hCryptProv, 
        NULL, 
        NULL, 
        PROV_RSA_FULL, 
        0)) 
    {
        printf("CryptAcquireContext complete. \n");
    }
    else
    {
        MyHandleError("Acquisition of context failed.");
    }

    //---------------------------------------------------------------
    // Create a hash object.
    if(CryptCreateHash(
        hCryptProv, 
        CALG_MD5, 
        0, 
        0, 
        &hHash)) 
    {
        printf("An empty hash object has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptBeginHash!\n");
    }

    //---------------------------------------------------------------
    // Create a random session key.
    if(CryptGenKey(
        hCryptProv, 
        CALG_RC2, 
        CRYPT_EXPORTABLE, 
        &hKey)) 
    {
        printf("A random session key has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptGenKey!\n");
    }

    //---------------------------------------------------------------
    // Compute the cryptographic hash on the key object.
    if(CryptHashSessionKey(
        hHash, 
        hKey, 
        0))
    {
        printf("The session key has been hashed. \n");
    }
    else
    {
        MyHandleError("Error during CryptHashSessionKey!\n");
    }

    /*
    Use the hash of the key object. For instance, additional data 
    could be hashed and sent in a message to several recipients. The 
    recipients will be able to verify who the message originator is 
    if the key used is also exported to them.
    */

    //---------------------------------------------------------------
    // Clean up.

    // Destroy the hash object.

    if(hHash)
    {
        if(!(CryptDestroyHash(hHash)))
        {
            MyHandleError("Error during CryptDestroyHash");
        }
    }

    // Destroy the session key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError("Error during CryptDestroyKey");
        }
    }

    // Release the provider.
    if(hCryptProv)
    {
        if(!(CryptReleaseContext(hCryptProv,0)))
        {
            MyHandleError("Error during CryptReleaseContext");
        }
    }
} // End main.

//  Define function MyHandleError.
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

```



 

 
