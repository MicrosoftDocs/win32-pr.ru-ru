---
description: Предоставляет функции для перечисления и получения сведений о зарегистрированных поставщиках.
ms.assetid: 5b07060e-0c66-4bf2-b697-05231cb38375
title: Использование средств настройки шифрования CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd700b52810f43381722a315bec12216acd7b683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662401"
---
# <a name="using-the-cryptography-configuration-features-of-cng"></a><span data-ttu-id="46a42-103">Использование средств настройки шифрования CNG</span><span class="sxs-lookup"><span data-stu-id="46a42-103">Using the Cryptography Configuration Features of CNG</span></span>

<span data-ttu-id="46a42-104">API-интерфейс CNG предоставляет функции для перечисления и получения сведений о зарегистрированных поставщиках.</span><span class="sxs-lookup"><span data-stu-id="46a42-104">The CNG API provides functions to enumerate and obtain information about registered providers.</span></span>

-   [<span data-ttu-id="46a42-105">Перечисление поставщиков</span><span class="sxs-lookup"><span data-stu-id="46a42-105">Enumerating Providers</span></span>](#enumerating-providers)
-   [<span data-ttu-id="46a42-106">Получение сведений о регистрации поставщика</span><span class="sxs-lookup"><span data-stu-id="46a42-106">Getting Provider Registration Information</span></span>](#getting-provider-registration-information)

## <a name="enumerating-providers"></a><span data-ttu-id="46a42-107">Перечисление поставщиков</span><span class="sxs-lookup"><span data-stu-id="46a42-107">Enumerating Providers</span></span>

<span data-ttu-id="46a42-108">Для перечисления зарегистрированных поставщиков используется функция [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) .</span><span class="sxs-lookup"><span data-stu-id="46a42-108">You use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to enumerate the registered providers.</span></span> <span data-ttu-id="46a42-109">Функцию **бкриптенумрегистередпровидерс** можно вызвать одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="46a42-109">The **BCryptEnumRegisteredProviders** function can be called in one of two ways:</span></span>

1.  <span data-ttu-id="46a42-110">Первый заключается в том, чтобы функция [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) выделила память.</span><span class="sxs-lookup"><span data-stu-id="46a42-110">The first is to have the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function allocate the memory.</span></span> <span data-ttu-id="46a42-111">Это достигается путем передачи адреса **пустого** указателя для параметра *ппбуффер* .</span><span class="sxs-lookup"><span data-stu-id="46a42-111">This is accomplished by passing the address of a **NULL** pointer for the *ppBuffer* parameter.</span></span> <span data-ttu-id="46a42-112">Этот код выделит память, необходимую для [**структуры \_ поставщиков шифрования**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) и связанных строк.</span><span class="sxs-lookup"><span data-stu-id="46a42-112">This code will allocate the memory required for the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and the associated strings.</span></span> <span data-ttu-id="46a42-113">Когда функция **бкриптенумрегистередпровидерс** используется таким образом, необходимо освободить память, когда она больше не нужна, передав *ппбуффер* функции [**бкриптфрибуффер**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .</span><span class="sxs-lookup"><span data-stu-id="46a42-113">When the **BCryptEnumRegisteredProviders** function is used in this manner, you must free the memory when it is no longer needed by passing *ppBuffer* to the [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) function.</span></span>

    <span data-ttu-id="46a42-114">В следующем примере показано, как использовать функцию [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="46a42-114">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate the buffer for you.</span></span>

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

    

2.  <span data-ttu-id="46a42-115">Второй способ заключается в выделении требуемой памяти самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="46a42-115">The second method is to allocate the required memory yourself.</span></span> <span data-ttu-id="46a42-116">Это достигается путем вызова функции [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) со **значением NULL** для параметра *ппбуффер* .</span><span class="sxs-lookup"><span data-stu-id="46a42-116">This is accomplished by calling the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function with **NULL** for the *ppBuffer* parameter.</span></span> <span data-ttu-id="46a42-117">Функция **бкриптенумрегистередпровидерс** будет помещаться в значение, на которое указывает параметр *пкббуффер* , необходимый размер в байтах структуры [**\_ поставщиков шифрования**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) и всех строк.</span><span class="sxs-lookup"><span data-stu-id="46a42-117">The **BCryptEnumRegisteredProviders** function will place in the value pointed to by the *pcbBuffer* parameter, the required size, in bytes, of the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and all strings.</span></span> <span data-ttu-id="46a42-118">Затем необходимо выделить требуемую память и передать адрес указателя буфера для параметра *ппбуффер* во втором вызове функции **бкриптенумрегистередпровидерс** .</span><span class="sxs-lookup"><span data-stu-id="46a42-118">You then allocate the required memory and pass the address of this buffer pointer for the *ppBuffer* parameter in a second call to the **BCryptEnumRegisteredProviders** function.</span></span>

    <span data-ttu-id="46a42-119">В следующем примере показано, как использовать функцию [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) для выделения и использования собственного буфера.</span><span class="sxs-lookup"><span data-stu-id="46a42-119">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate and use your own buffer.</span></span>

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

    

## <a name="getting-provider-registration-information"></a><span data-ttu-id="46a42-120">Получение сведений о регистрации поставщика</span><span class="sxs-lookup"><span data-stu-id="46a42-120">Getting Provider Registration Information</span></span>

<span data-ttu-id="46a42-121">Функция [**бкрипткуерипровидеррегистратион**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) используется для получения дополнительных сведений о поставщике, относящихся к регистрации.</span><span class="sxs-lookup"><span data-stu-id="46a42-121">The [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function is used to obtain additional, registration-specific information about a provider.</span></span> <span data-ttu-id="46a42-122">Эта функция принимает имя поставщика, для которого требуется получить сведения, требуемый режим поставщика (режим ядра, режим пользователя или оба) и идентификатор интерфейса поставщика для получения сведений о регистрации.</span><span class="sxs-lookup"><span data-stu-id="46a42-122">This function takes the name of the provider that you want to obtain information for, the desired provider mode (kernel mode, user mode, or both), and the identifier of the provider interface to retrieve the registration information for.</span></span> <span data-ttu-id="46a42-123">Например, чтобы получить сведения о регистрации в пользовательском режиме для интерфейса шифра поставщика Microsoft-примитивного поставщика, необходимо выполнить вызов, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="46a42-123">For example, to obtain the user mode registration information for the cipher interface for the "Microsoft Primitive Provider" provider, you would make a call similar to the following.</span></span>


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



<span data-ttu-id="46a42-124">Как и функция [**бкриптенумрегистередпровидерс**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , функция [**бкрипткуерипровидеррегистратион**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) может либо выделить память для вас, либо выделить память самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="46a42-124">Like the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function, the [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function can either allocate memory for you or you can allocate the memory yourself.</span></span> <span data-ttu-id="46a42-125">Этот процесс одинаков для двух функций.</span><span class="sxs-lookup"><span data-stu-id="46a42-125">The process is the same for the two functions.</span></span>

 

 



