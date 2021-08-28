---
description: 'API шифрования: следующее поколение (CNG) предоставляет функции, которые запрашивают, добавляют, удаляют и назначают приоритеты комплектов шифров, поддерживаемых поставщиком. Изменения, внесенные с помощью этих функций, вступают в силу немедленно и не нуждаются в перезапуске активного сервера.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Определение приоритетов для комплектов шифров SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4436d2f72ebaa1f8d551d935ea9f16d2c03cd7c75fc7d40a73f1a27c7406ad6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920773"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Определение приоритетов для комплектов шифров SChannel

[API шифрования: следующее поколение](../seccng/cng-portal.md) (CNG) предоставляет функции, которые запрашивают, добавляют, удаляют и назначают приоритеты комплектов шифров, поддерживаемых поставщиком. Изменения, внесенные с помощью этих функций, вступают в силу немедленно и не нуждаются в перезапуске активного сервера.

> [!Note]
> Список комплектов шифров также можно изменить, настроив параметры групповой политики **порядок набора шифров SSL** с помощью оснастки "Групповая политика объект" в консоли управления (MMC).
> 
> **Настройка параметра групповой политики " **порядок набора шифров SSL** "**
> 
> 1.  В командной строке введите **gpedit. msc**. Появится **Редактор объектов групповой политики** .
> 2.  разверните узел **конфигурация компьютера**, **административные шаблоны**, **сеть**, а затем щелкните **конфигурация SSL Параметры**.
> 3.  в разделе **конфигурация ssl Параметры** выберите параметр **порядок набора шифров ssl** .
> 4.  В области **порядок набора шифров SSL** прокрутите до нижней части области.
> 5.  Следуйте инструкциям, **чтобы изменить этот параметр**.
> 
> Чтобы изменения вступили в силу, необходимо перезагрузить компьютер после изменения этого параметра.

 

Список комплектов шифров ограничен 1023 символами.

Чтобы установить приоритет для комплектов шифров SChannel, см. следующие примеры.

-   [Список поддерживаемых комплектов шифров](#listing-supported-cipher-suites)
-   [Добавление, удаление и назначение приоритетов комплектам шифров](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Список поддерживаемых комплектов шифров

Вызовите функцию [**бкриптенумконтекстфунктионс**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) , чтобы получить список комплектов шифров, поддерживаемых поставщиком в порядке приоритета.

В следующем примере показано, как использовать функцию [**бкриптенумконтекстфунктионс**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) для перечисления поддерживаемых комплектов шифров.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{

   HRESULT Status = ERROR_SUCCESS;
   DWORD   cbBuffer = 0;
   PCRYPT_CONTEXT_FUNCTIONS pBuffer = NULL;

    Status = BCryptEnumContextFunctions(
        CRYPT_LOCAL,
        L"SSL",
        NCRYPT_SCHANNEL_INTERFACE,
        &cbBuffer,
        &pBuffer);
    if(FAILED(Status))
    {
        printf_s("\n**** Error 0x%x returned by BCryptEnumContextFunctions\n", Status);
        goto Cleanup;
    }
                
    if(pBuffer == NULL)
    {
        printf_s("\n**** Error pBuffer returned from BCryptEnumContextFunctions is null");
        goto Cleanup;
    }

    printf_s("\n\n Listing Cipher Suites ");
    for(UINT index = 0; index < pBuffer->cFunctions; ++index)
    {
        printf_s("\n%S", pBuffer->rgpszFunctions[index]);
    }

Cleanup:
    if (pBuffer != NULL)
    {
        BCryptFreeBuffer(pBuffer);
    }
}


```



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>Добавление, удаление и назначение приоритетов комплектам шифров

Вызовите функции [**бкриптаддконтекстфунктион**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) и [**бкриптремовеконтекстфунктион**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) , чтобы добавлять и удалять комплекты шифров из списка поддерживаемых комплектов шифров.

При добавлении комплекта шифров установите значение параметра *двпоситион* функции [**бкриптаддконтекстфунктион**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) , чтобы оно применяет **\_ приоритет \_** , чтобы добавить его в верхнюю часть списка с приоритетом или присвоить **\_ приоритетному \_ нижнему** краю, чтобы добавить его в нижнюю часть списка.

Чтобы определить приоритет списка комплектов шифров, удалите все комплекты шифров из списка, а затем добавьте комплекты шифров в список в нужном порядке.

В следующем примере показано, как добавить набор шифров в верхнюю часть списка с приоритетами для поставщика Microsoft SChannel по умолчанию.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
    LPWSTR wszCipher = (L"RSA_EXPORT1024_DES_CBC_SHA");
       
    Status = BCryptAddContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher,
                CRYPT_PRIORITY_TOP);
}


```



В следующем примере показано, как удалить комплект шифров из списка приоритетов для поставщика Microsoft SChannel по умолчанию.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
      LPWSTR wszCipher = (L"TLS_RSA_WITH_RC4_128_SHA");
       
    Status = BCryptRemoveContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher);
}


```



 

 
