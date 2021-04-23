---
description: Базовый поставщик использовал только 40-разрядные симметричные ключи.
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: Новая функция длины ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6842bfc1f4e68f115d804a55d628ffa51f0c68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272256"
---
# <a name="new-key-length-functionality"></a><span data-ttu-id="790a8-103">Новая функция длины ключей</span><span class="sxs-lookup"><span data-stu-id="790a8-103">New Key-length Functionality</span></span>

<span data-ttu-id="790a8-104">Базовый поставщик использовал только 40-разрядные [*симметричные ключи*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="790a8-104">The Base Provider used only 40-bit [*symmetric keys*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="790a8-105">Добавление более длинных ключей в расширенном поставщике и факт того, что импортируемые ключи могут иметь произвольную длину, требуют запроса длины для определенного ключа.</span><span class="sxs-lookup"><span data-stu-id="790a8-105">The addition of longer keys in the Enhanced Provider, and the fact that imported keys can be of arbitrary length requires a method of querying the length for a specific key.</span></span> <span data-ttu-id="790a8-106">Чтобы определить фактическую длину ключа в битах, пользователь может вызвать [**криптжеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) с помощью \_ значения параметра кэйлен.</span><span class="sxs-lookup"><span data-stu-id="790a8-106">To find the actual length of a key in bits, a user can call [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) with the KP\_KEYLEN parameter value.</span></span> <span data-ttu-id="790a8-107">Длина ключа возвращается в **DWORD** , на который указывает параметр *pbData* .</span><span class="sxs-lookup"><span data-stu-id="790a8-107">The length of the key is returned in the **DWORD** pointed to by the *pbData* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="790a8-108">Для защиты от [*криптаналисис*](../secgloss/c-gly.md) атак с пошаговым выполнением приложения должны проверить недостаточность [*длины ключей*](../secgloss/k-gly.md) и уведомить пользователя о том, что он встречается.</span><span class="sxs-lookup"><span data-stu-id="790a8-108">To protect against stepping-down [*cryptanalysis*](../secgloss/c-gly.md) attacks, applications must check for insufficient [*key lengths*](../secgloss/k-gly.md) and notify the user when one is encountered.</span></span>

 

<span data-ttu-id="790a8-109">В следующем примере показано, как запросить длину ключа.</span><span class="sxs-lookup"><span data-stu-id="790a8-109">The following example shows how to query the length of a key.</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <Wincrypt.h>
#include <stdio.h>
void main()
{
    HCRYPTPROV hProv = NULL;
    HCRYPTKEY hKey = NULL;

    DWORD dwKeyLength;
    DWORD dwLen = sizeof(DWORD);
    // Copyright (C) Microsoft.  All rights reserved.
    // Acquire a cryptographic context.
    if (!CryptAcquireContext(&hProv,
                              NULL,
                              NULL,
                              PROV_RSA_FULL,
                              CRYPT_VERIFYCONTEXT))
    {
        printf("CryptAcquireContext failed.\n");
        goto Cleanup;
    }

    // Generate a key.
    if (!CryptGenKey(
                hProv,    
                CALG_RC2,    
                0,    
                &hKey))
    {
        printf("CryptGenKey failed.\n");
        goto Cleanup;
    }

    // Query the key length.
    if (!CryptGetKeyParam(
            hKey,    
            KP_KEYLEN,    
            (BYTE*)&dwKeyLength,
            &dwLen,    
            0))
    {
        printf("CryptGetKeyParam failed.\n");
        goto Cleanup;
    }
    else
    {
        printf("The key is %d bits long. \n", dwKeyLength);
    } 

Cleanup:

    if (hKey)
        CryptDestroyKey(hKey);

    if (hProv)
        CryptReleaseContext(hProv, 0);
}
```



 

 
