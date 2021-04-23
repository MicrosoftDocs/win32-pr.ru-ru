---
title: Пример создания ключа сеанса
description: Пример создания ключа сеанса
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- Windows Media Format SDK, сеансовые ключи
- Windows Media Format SDK, ключи содержимого
- Windows Media Format SDK, пример кода
- Windows Media Format SDK, примеры кода
- Управление цифровыми правами (DRM), сеансовые ключи
- DRM (Управление цифровыми правами), сеансовые ключи
- Управление цифровыми правами (DRM), ключи содержимого
- DRM (Управление цифровыми правами), ключи содержимого
- Управление цифровыми правами (DRM), пример кода
- DRM (Управление цифровыми правами), пример кода
- Управление цифровыми правами (DRM), примеры кода
- DRM (Управление цифровыми правами), примеры кода
- Расширенные API клиента DRM, ключи сеанса
- Расширенные API клиента, ключи сеанса
- Расширенные API клиента DRM, ключи содержимого
- Расширенные API клиента, ключи содержимого
- Расширенные API клиента DRM, пример кода
- Расширенные API клиента, пример кода
- Расширенные API клиента DRM, примеры кода
- Расширенные API клиента, примеры кода
- ключи сеанса
- ключи содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b757f5d67df0aea1dd70ee45ad2d1b0732040be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068595"
---
# <a name="create-session-key-example"></a><span data-ttu-id="0a903-125">Пример создания ключа сеанса</span><span class="sxs-lookup"><span data-stu-id="0a903-125">Create Session Key Example</span></span>

<span data-ttu-id="0a903-126">Ключ сеанса используется для защиты ключа содержимого.</span><span class="sxs-lookup"><span data-stu-id="0a903-126">The session key is used to protect the content key.</span></span> <span data-ttu-id="0a903-127">Следующий код демонстрирует создание ключа сеанса, но оставляет сведения о создании случайных ключей.</span><span class="sxs-lookup"><span data-stu-id="0a903-127">The following code demonstrates how to create a session key, but leaves out the details of random key generation.</span></span>


```C++
HRESULT CreateSessionKey( WMDRM_IMPORT_SESSION_KEY **ppSessionKey, DWORD *pcbSessionKey )
{
    // TODO: Set this value to the desired number of bytes for the session key data. 
    const DWORD SESSION_KEY_DATA_SIZE = 20; 

    HRESULT hr = S_OK;
    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;

    if( NULL == ppSessionKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }
    
    // Compute the size of the session key structure plus the session key.
    DWORD cbSessionKey = sizeof( WMDRM_IMPORT_SESSION_KEY ) + SESSION_KEY_DATA_SIZE;

    // Allocate memory for the session key.
    pSessionKey = (WMDRM_IMPORT_SESSION_KEY *)new BYTE[ cbSessionKey ];
    if( NULL == pSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    ZeroMemory( pSessionKey, cbSessionKey );

    // Set the key type and the key size.
    pSessionKey->dwKeyType = WMDRM_KEYTYPE_RC4;
    pSessionKey->cbKey = SESSION_KEY_DATA_SIZE;
    
    // Set the key to a random value. Note that the random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in shipping code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pSessionKey->rgbKey;
    for (size_t i = 0; i < SESSION_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }
    
    // If all has been successful set the parameters.
    *ppSessionKey = pSessionKey;
    pSessionKey = NULL;
    *pcbSessionKey = cbSessionKey;

EXIT:
    
    SAFE_ARRAY_DELETE( pSessionKey );
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0a903-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0a903-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a903-129">**Примеры импорта DRM**</span><span class="sxs-lookup"><span data-stu-id="0a903-129">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




