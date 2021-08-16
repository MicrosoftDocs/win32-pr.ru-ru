---
description: Предоставляет функции для перечисления и получения сведений о зарегистрированных поставщиках.
ms.assetid: 5b07060e-0c66-4bf2-b697-05231cb38375
title: Использование средств настройки шифрования CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa1845d7c1df7afb95b93446b1e86b3838aed7e0ef51bb0e53b6f7a83f3515b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905403"
---
# <a name="using-the-cryptography-configuration-features-of-cng"></a>Использование средств настройки шифрования CNG

API-интерфейс CNG предоставляет функции для перечисления и получения сведений о зарегистрированных поставщиках.

-   [Перечисление поставщиков](#enumerating-providers)
-   [Получение сведений о регистрации поставщика](#getting-provider-registration-information)

## <a name="enumerating-providers"></a>Перечисление поставщиков

Для перечисления зарегистрированных поставщиков используется функция [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) . Функцию **бкриптенумрегистередпровидерс** можно вызвать одним из двух способов:

1.  Первый заключается в том, чтобы функция [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) выделила память. Это достигается путем передачи адреса **пустого** указателя для параметра *ппбуффер* . Этот код выделит память, необходимую для [**структуры \_ поставщиков шифрования**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) и связанных строк. Когда функция **бкриптенумрегистередпровидерс** используется таким образом, необходимо освободить память, когда она больше не нужна, передав *ппбуффер* функции [**бкриптфрибуффер**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .

    В следующем примере показано, как использовать функцию [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) для выделения буфера.

    ```C++
    #include <windows.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders1()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;
        PCRYPT_PROVIDERS pBuffer = NULL;

        /*
        Get the providers, letting the BCryptEnumRegisteredProviders 
        function allocate the memory.
        */
        status = BCryptEnumRegisteredProviders(&cbBuffer, &pBuffer);

        if (NT_SUCCESS(status))
        {
            if (pBuffer != NULL)
            {
                // Enumerate the providers.
                for (ULONG i = 0; i < pBuffer->cProviders; i++)
                {
                    printf("%S\n", pBuffer->rgpszProviders[i]);
                }
            }
        }
        else
        {
            printf("BCryptEnumRegisteredProviders failed with error " 
                "code 0x%08x\n", status);
        }

        if (NULL != pBuffer)
        {
            /*
            Free the memory allocated by the 
            BCryptEnumRegisteredProviders function.
            */
            BCryptFreeBuffer(pBuffer);
        }
    }
    
    ```

    

2.  Второй способ заключается в выделении требуемой памяти самостоятельно. Это достигается путем вызова функции [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) со **значением NULL** для параметра *ппбуффер* . Функция **бкриптенумрегистередпровидерс** будет помещаться в значение, на которое указывает параметр *пкббуффер* , необходимый размер в байтах структуры [**\_ поставщиков шифрования**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) и всех строк. Затем необходимо выделить требуемую память и передать адрес указателя буфера для параметра *ппбуффер* во втором вызове функции **бкриптенумрегистередпровидерс** .

    В следующем примере показано, как использовать функцию [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) для выделения и использования собственного буфера.

    ```C++
    #include <windows.h>
    #include <stdio.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders2()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;

        // Get the required size of the buffer.
        status = BCryptEnumRegisteredProviders(&cbBuffer, NULL);

        if (STATUS_BUFFER_TOO_SMALL == status)
        {
            // Allocate the buffer.
            PCRYPT_PROVIDERS pBuffer = 
                (PCRYPT_PROVIDERS)LocalAlloc(LPTR, cbBuffer);
            if (NULL != pBuffer)
            {
                // Get the providers in the buffer that was allocated.
                status = BCryptEnumRegisteredProviders(
                    &cbBuffer, 
                    &pBuffer);
                if (NT_SUCCESS(status))
                {
                    for (ULONG i = 0; i < pBuffer->cProviders; i++)
                    {
                        // Enumerate the providers.
                        printf("%S\n", pBuffer->rgpszProviders[i]);
                    }
                }

                // Free the memory that was allocated.
                LocalFree(pBuffer);
            }
        }
    }
    
    ```

    

## <a name="getting-provider-registration-information"></a>Получение сведений о регистрации поставщика

Функция [**бкрипткуерипровидеррегистратион**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) используется для получения дополнительных сведений о поставщике, относящихся к регистрации. Эта функция принимает имя поставщика, для которого требуется получить сведения, требуемый режим поставщика (режим ядра, режим пользователя или оба) и идентификатор интерфейса поставщика для получения сведений о регистрации. Например, чтобы получить сведения о регистрации в пользовательском режиме для интерфейса шифра поставщика Microsoft-примитивного поставщика, необходимо выполнить вызов, аналогичный приведенному ниже.


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



Как и функция [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , функция [**бкрипткуерипровидеррегистратион**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) может либо выделить память для вас, либо выделить память самостоятельно. Этот процесс одинаков для двух функций.

 

 



