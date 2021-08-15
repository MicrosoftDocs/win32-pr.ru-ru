---
title: Пример создания ключа сеанса
description: Пример создания ключа сеанса
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- Windows Пакет SDK для формата мультимедиа, ключи сеанса
- Windows Пакет SDK для формата мультимедиа, ключи содержимого
- Windows Пакет SDK для формата мультимедиа, пример кода
- Windows Пакет SDK для формата мультимедиа, примеры кода
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
ms.openlocfilehash: cef4a9c673b0aef24e010bff0f9a84beaf6321a81fe4ac8a8a9935c126983eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964143"
---
# <a name="create-session-key-example"></a>Пример создания ключа сеанса

Ключ сеанса используется для защиты ключа содержимого. Следующий код демонстрирует создание ключа сеанса, но оставляет сведения о создании случайных ключей.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Примеры импорта DRM**](drm-import-examples.md)
</dt> </dl>

 

 




