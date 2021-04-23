---
title: Пример импорта управления цифровыми правами
description: Пример импорта управления цифровыми правами
ms.assetid: 46a64305-9aac-47df-992d-6aea8ecb54bf
keywords:
- Windows Media Format SDK, импорт DRM
- Windows Media Format SDK, импорт
- Windows Media Format SDK, пример кода
- Windows Media Format SDK, примеры кода
- Управление цифровыми правами (DRM), импорт
- DRM (Управление цифровыми правами), импорт
- Управление цифровыми правами (DRM), инициализация импорта
- DRM (Управление цифровыми правами), инициализация импорта
- Управление цифровыми правами (DRM), пример кода
- DRM (Управление цифровыми правами), пример кода
- Управление цифровыми правами (DRM), примеры кода
- DRM (Управление цифровыми правами), примеры кода
- Расширенные API клиента DRM, инициализация импорта
- Расширенные API клиента, инициализация импорта
- Расширенные API клиента DRM, импорт
- Расширенные API клиента, импорт
- Расширенные API клиента DRM, пример кода
- Расширенные API клиента, пример кода
- Расширенные API клиента DRM, примеры кода
- Расширенные API клиента, примеры кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450eeaa128c17d0d64511dd028cda3ce1c4f28c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258959"
---
# <a name="initialize-drm-import-example"></a><span data-ttu-id="12da9-123">Пример импорта управления цифровыми правами</span><span class="sxs-lookup"><span data-stu-id="12da9-123">Initialize DRM Import Example</span></span>

<span data-ttu-id="12da9-124">В следующем примере кода показано, как инициализировать объект модуля записи DRM для импорта DRM:</span><span class="sxs-lookup"><span data-stu-id="12da9-124">The following code example illustrates how to initialize a DRM writer object for DRM Import:</span></span>


```C++
HRESULT InitializeImport( IWMDRMWriter3 *pDRMWriter )
{
    // Set this value to the desired number of bytes in an encrypted 
    //  session key.
    const int MODULUS_SIZE = 32;

    HRESULT hr = S_OK;
    WMDRM_IMPORT_INIT_STRUCT ImportInit;

    BYTE *pbEncryptedSessionKey = NULL;
    DWORD cbEncryptedSessionKey = 0;

    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;
    DWORD cbSessionKey = 0;

    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;
    DWORD cbContentKey = 0;
        
    // Allocate memory for the encrypted session key.
    pbEncryptedSessionKey = new BYTE[ MODULUS_SIZE ];
    if( NULL == pbEncryptedSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    cbEncryptedSessionKey = MODULUS_SIZE;

    hr = CreateSessionKey( &pSessionKey, &cbSessionKey );
    if( FAILED( hr ) ) goto EXIT;

    if( cbSessionKey > MODULUS_SIZE )
    if( FAILED( hr ) ) goto EXIT;

    hr = CreateContentKey( &pContentKey, &cbContentKey );
    if( FAILED( hr ) ) goto EXIT;

    // TODO: Encrypt the content key with the session Key.    
    // TODO: Encrypt the session key with the machine certificate public key.   

    ImportInit.dwVersion = 0;
    ImportInit.pbEncryptedSessionKeyMessage = pbEncryptedSessionKey;
    ImportInit.cbEncryptedSessionKeyMessage = cbEncryptedSessionKey;
    ImportInit.pbEncryptedKeyMessage = (BYTE*)pContentKey;
    ImportInit.cbEncryptedKeyMessage = cbContentKey;

    hr = pDRMWriter->SetProtectStreamSamples( &ImportInit );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_ARRAY_DELETE( pContentKey );
    SAFE_ARRAY_DELETE( pSessionKey );

    return( hr );
}
```



## <a name="related-topics"></a><span data-ttu-id="12da9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="12da9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12da9-126">**Пример создания ключа содержимого**</span><span class="sxs-lookup"><span data-stu-id="12da9-126">**Create Content Key Example**</span></span>](create-content-key-example.md)
</dt> <dt>

[<span data-ttu-id="12da9-127">**Пример создания ключа сеанса**</span><span class="sxs-lookup"><span data-stu-id="12da9-127">**Create Session Key Example**</span></span>](create-session-key-example.md)
</dt> <dt>

[<span data-ttu-id="12da9-128">**Примеры импорта DRM**</span><span class="sxs-lookup"><span data-stu-id="12da9-128">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




