---
title: Пример создания ключа содержимого
description: Пример создания ключа содержимого
ms.assetid: 8e75bac3-d1fb-4a72-8088-fe5ff0899ac2
keywords:
- Windows Media Format SDK, ключи содержимого
- Windows Media Format SDK, пример кода
- Windows Media Format SDK, примеры кода
- Управление цифровыми правами (DRM), ключи содержимого
- DRM (Управление цифровыми правами), ключи содержимого
- Управление цифровыми правами (DRM), пример кода
- DRM (Управление цифровыми правами), пример кода
- Управление цифровыми правами (DRM), примеры кода
- DRM (Управление цифровыми правами), примеры кода
- Расширенные API клиента DRM, ключи содержимого
- Расширенные API клиента, ключи содержимого
- Расширенные API клиента DRM, пример кода
- Расширенные API клиента, пример кода
- Расширенные API клиента DRM, примеры кода
- Расширенные API клиента, примеры кода
- ключи содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881dfd0d318d7d699b44ca9c3f77f22f9acfc689
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068596"
---
# <a name="create-content-key-example"></a><span data-ttu-id="35c2d-119">Пример создания ключа содержимого</span><span class="sxs-lookup"><span data-stu-id="35c2d-119">Create Content Key Example</span></span>

<span data-ttu-id="35c2d-120">Ключ содержимого используется для шифрования образцов мультимедиа для импорта Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="35c2d-120">The content key is used to encrypt media samples for Windows Media DRM Import.</span></span> <span data-ttu-id="35c2d-121">В следующем примере кода показано, как создать и инициализировать структуру ключа содержимого.</span><span class="sxs-lookup"><span data-stu-id="35c2d-121">The following code example demonstrates how to create and initialize a content key structure.</span></span>


```C++
HRESULT CreateContentKey( WMDRM_IMPORT_CONTENT_KEY **ppContentKey, DWORD *pcbContentKey)
{
    // TODO: Set this value to the desired number of bytes for the content key data. 
    const DWORD IV_DATA_SIZE = 16;
    HRESULT hr = S_OK;
    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;

    // The content key.
    const BYTE rgbContentKey[] = {
        0x67, 0x39, 0x83, 0xb9,
        0x52, 0xa8, 0xe3
    };        
    const DWORD CONTENT_KEY_DATA_SIZE = sizeof(rgbContentKey);

    // Compute the total size of the content key structure
    DWORD cbContentKey = sizeof( WMDRM_IMPORT_CONTENT_KEY ) +
      IV_DATA_SIZE + CONTENT_KEY_DATA_SIZE;

    // Make sure we have a valid 
    if( NULL == ppContentKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }

    // Allocate the content key, locally first
    pContentKey = (WMDRM_IMPORT_CONTENT_KEY *)new BYTE[ cbContentKey ];
    
    // Check the allocation was successful 
    if( NULL == pContentKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }

    // Ininitalize the key
    ZeroMemory( pContentKey, cbContentKey );
    pContentKey->dwVersion = 0;
    pContentKey->cbStructSize = cbContentKey;

    // Set the initialization vector key type 
    pContentKey->dwIVKeyType = WMDRM_KEYTYPE_RC4;
    pContentKey->cbIVKey = IV_DATA_SIZE;
    
    // Generate a random initialization vector. Note that this random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in commercial strength code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pContentKey->rgbKeyData;
    for (size_t i = 0; i < IV_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }   
    
    // Set the content key type.
    pContentKey->dwContentKeyType = WMDRM_KEYTYPE_COCKTAIL;
    pContentKey->cbContentKey = CONTENT_KEY_DATA_SIZE;

    // Fill out the content key. 
    for (size_t i = 0; i < CONTENT_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = rgbContentKey[i]; 
    }   
    

    // If all has been successful, set the parameters
    *ppContentKey = pContentKey;
    pContentKey = NULL;
    *pcbContentKey = cbContentKey;

EXIT:
    SAFE_ARRAY_DELETE( pContentKey );
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="35c2d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="35c2d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35c2d-123">**Примеры импорта DRM**</span><span class="sxs-lookup"><span data-stu-id="35c2d-123">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




