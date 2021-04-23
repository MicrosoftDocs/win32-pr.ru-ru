---
description: 'API шифрования: следующее поколение (CNG) предоставляет функции, которые запрашивают, добавляют, удаляют и назначают приоритеты комплектов шифров, поддерживаемых поставщиком. Изменения, внесенные с помощью этих функций, вступают в силу немедленно и не нуждаются в перезапуске активного сервера.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Определение приоритетов для комплектов шифров SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f885c4d51006233be252a02c7cc3bebd26a4e6c3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273335"
---
# <a name="prioritizing-schannel-cipher-suites"></a><span data-ttu-id="c1f08-104">Определение приоритетов для комплектов шифров SChannel</span><span class="sxs-lookup"><span data-stu-id="c1f08-104">Prioritizing Schannel Cipher Suites</span></span>

<span data-ttu-id="c1f08-105">[API шифрования: следующее поколение](../seccng/cng-portal.md) (CNG) предоставляет функции, которые запрашивают, добавляют, удаляют и назначают приоритеты комплектов шифров, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="c1f08-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) provides functions that query, add, remove, and prioritize the cipher suites that a provider supports.</span></span> <span data-ttu-id="c1f08-106">Изменения, внесенные с помощью этих функций, вступают в силу немедленно и не нуждаются в перезапуске активного сервера.</span><span class="sxs-lookup"><span data-stu-id="c1f08-106">Changes made by using these functions take effect immediately and do not require restarting an active server.</span></span>

> [!Note]
> <span data-ttu-id="c1f08-107">Список комплектов шифров также можно изменить, настроив параметры групповой политики **порядок набора шифров SSL** с помощью оснастки "Групповая политика объект" в консоли управления (MMC).</span><span class="sxs-lookup"><span data-stu-id="c1f08-107">You can also modify the list of cipher suites by configuring the **SSL Cipher Suite Order** group policy settings using the Group Policy Object snap-in in Microsoft Management Console.</span></span>
> 
> <span data-ttu-id="c1f08-108">**Настройка параметра групповой политики " **порядок набора шифров SSL** "**</span><span class="sxs-lookup"><span data-stu-id="c1f08-108">**To configure the **SSL Cipher Suite Order** group policy setting**</span></span>
> 
> 1.  <span data-ttu-id="c1f08-109">В командной строке введите **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="c1f08-109">At a command prompt, enter **gpedit.msc**.</span></span> <span data-ttu-id="c1f08-110">Появится **Редактор объектов групповой политики** .</span><span class="sxs-lookup"><span data-stu-id="c1f08-110">The **Group Policy Object Editor** appears.</span></span>
> 2.  <span data-ttu-id="c1f08-111">Разверните узел **Конфигурация компьютера**, **Административные шаблоны**, **сеть**, а затем щелкните **Параметры конфигурации SSL**.</span><span class="sxs-lookup"><span data-stu-id="c1f08-111">Expand **Computer Configuration**, **Administrative Templates**, **Network**, and then click **SSL Configuration Settings**.</span></span>
> 3.  <span data-ttu-id="c1f08-112">В разделе **Параметры конфигурации SSL** щелкните параметр **порядок набора шифров SSL** .</span><span class="sxs-lookup"><span data-stu-id="c1f08-112">Under **SSL Configuration Settings**, click the **SSL Cipher Suite Order** setting.</span></span>
> 4.  <span data-ttu-id="c1f08-113">В области **порядок набора шифров SSL** прокрутите до нижней части области.</span><span class="sxs-lookup"><span data-stu-id="c1f08-113">In the **SSL Cipher Suite Order** pane, scroll to the bottom of the pane.</span></span>
> 5.  <span data-ttu-id="c1f08-114">Следуйте инструкциям, **чтобы изменить этот параметр**.</span><span class="sxs-lookup"><span data-stu-id="c1f08-114">Follow the instructions labeled **How to modify this setting**.</span></span>
> 
> <span data-ttu-id="c1f08-115">Чтобы изменения вступили в силу, необходимо перезагрузить компьютер после изменения этого параметра.</span><span class="sxs-lookup"><span data-stu-id="c1f08-115">It is necessary to restart the computer after modifying this setting for the changes to take effect.</span></span>

 

<span data-ttu-id="c1f08-116">Список комплектов шифров ограничен 1023 символами.</span><span class="sxs-lookup"><span data-stu-id="c1f08-116">The list of cipher suites is limited to 1023 characters.</span></span>

<span data-ttu-id="c1f08-117">Чтобы установить приоритет для комплектов шифров SChannel, см. следующие примеры.</span><span class="sxs-lookup"><span data-stu-id="c1f08-117">To prioritize Schannel cipher suites, see the following examples.</span></span>

-   [<span data-ttu-id="c1f08-118">Список поддерживаемых комплектов шифров</span><span class="sxs-lookup"><span data-stu-id="c1f08-118">Listing Supported Cipher Suites</span></span>](#listing-supported-cipher-suites)
-   [<span data-ttu-id="c1f08-119">Добавление, удаление и назначение приоритетов комплектам шифров</span><span class="sxs-lookup"><span data-stu-id="c1f08-119">Adding, Removing, and Prioritizing Cipher Suites</span></span>](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a><span data-ttu-id="c1f08-120">Список поддерживаемых комплектов шифров</span><span class="sxs-lookup"><span data-stu-id="c1f08-120">Listing Supported Cipher Suites</span></span>

<span data-ttu-id="c1f08-121">Вызовите функцию [**бкриптенумконтекстфунктионс**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) , чтобы получить список комплектов шифров, поддерживаемых поставщиком в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="c1f08-121">Call the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list the cipher suites that a provider supports in order of priority.</span></span>

<span data-ttu-id="c1f08-122">В следующем примере показано, как использовать функцию [**бкриптенумконтекстфунктионс**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) для перечисления поддерживаемых комплектов шифров.</span><span class="sxs-lookup"><span data-stu-id="c1f08-122">The following example demonstrates how to use the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list supported cipher suites.</span></span>


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



## <a name="adding-removing-and-prioritizing-cipher-suites"></a><span data-ttu-id="c1f08-123">Добавление, удаление и назначение приоритетов комплектам шифров</span><span class="sxs-lookup"><span data-stu-id="c1f08-123">Adding, Removing, and Prioritizing Cipher Suites</span></span>

<span data-ttu-id="c1f08-124">Вызовите функции [**бкриптаддконтекстфунктион**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) и [**бкриптремовеконтекстфунктион**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) , чтобы добавлять и удалять комплекты шифров из списка поддерживаемых комплектов шифров.</span><span class="sxs-lookup"><span data-stu-id="c1f08-124">Call the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) and [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) functions to add and remove cipher suites from the list of supported cipher suites.</span></span>

<span data-ttu-id="c1f08-125">При добавлении комплекта шифров установите значение параметра *двпоситион* функции [**бкриптаддконтекстфунктион**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) , чтобы оно применяет **\_ приоритет \_** , чтобы добавить его в верхнюю часть списка с приоритетом или присвоить **\_ приоритетному \_ нижнему** краю, чтобы добавить его в нижнюю часть списка.</span><span class="sxs-lookup"><span data-stu-id="c1f08-125">When adding a cipher suite, set the value of the *dwPosition* parameter of the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) function to **CRYPT\_PRIORITY\_TOP** to add it to the top of the prioritized list, or to **CRYPT\_PRIORITY\_BOTTOM** to add it to the bottom of the list.</span></span>

<span data-ttu-id="c1f08-126">Чтобы определить приоритет списка комплектов шифров, удалите все комплекты шифров из списка, а затем добавьте комплекты шифров в список в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="c1f08-126">To prioritize the list of cipher suites, remove all of the cipher suites from the list, and then add cipher suites to the list in the order you want them.</span></span>

<span data-ttu-id="c1f08-127">В следующем примере показано, как добавить набор шифров в верхнюю часть списка с приоритетами для поставщика Microsoft SChannel по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1f08-127">The following example shows how to add a cipher suite to the top of the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



<span data-ttu-id="c1f08-128">В следующем примере показано, как удалить комплект шифров из списка приоритетов для поставщика Microsoft SChannel по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1f08-128">The following example shows how to remove a cipher suite from the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



 

 
