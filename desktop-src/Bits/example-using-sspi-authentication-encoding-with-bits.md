---
title: Пример использования кодирования аутентификации SSPI с BITS
description: Вы можете использовать методы проверки подлинности (SSPI) и фоновая интеллектуальная служба передачи (BITS) для получения учетных данных от пользователя, кодирования учетных данных и установки закодированных учетных данных для задания передачи BITS.
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b86248c4782789010a817755d9bc27b3e5373b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793771"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a><span data-ttu-id="3b653-103">Пример. Использование кодирования проверки подлинности SSPI с BITS</span><span class="sxs-lookup"><span data-stu-id="3b653-103">Example: Using SSPI Authentication Encoding with BITS</span></span>

<span data-ttu-id="3b653-104">Вы можете использовать методы проверки подлинности (SSPI) и фоновая интеллектуальная служба передачи (BITS) для получения учетных данных от пользователя, кодирования учетных данных и установки закодированных учетных данных для задания передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="3b653-104">You can use Security Support Provider Interface (SSPI) Authentication and Background Intelligent Transfer Service (BITS) methods to get the credentials from a user, encode the credentials, and set the encoded credentials on a BITS transfer job.</span></span> <span data-ttu-id="3b653-105">Для преобразования структуры учетных данных в строки, которые можно передать в задание передачи BITS, требуется кодирование.</span><span class="sxs-lookup"><span data-stu-id="3b653-105">Encoding is required to convert credentials structure into strings that can be passed to a BITS transfer job.</span></span>

<span data-ttu-id="3b653-106">Дополнительные сведения о проверке подлинности и методах SSPI см. в разделе [SSPI](../secauthn/sspi.md).</span><span class="sxs-lookup"><span data-stu-id="3b653-106">For more information about SSPI authentication and methods, see [SSPI](../secauthn/sspi.md).</span></span>

<span data-ttu-id="3b653-107">Следующая процедура запрашивает учетные данные пользователя с помощью пакета безопасности Negotiate.</span><span class="sxs-lookup"><span data-stu-id="3b653-107">The following procedure prompts for credentials from the user by using the Negotiate security package.</span></span> <span data-ttu-id="3b653-108">Программа создает структуру идентификации проверки подлинности и заполняет структуру закодированными строками, представляющими имя пользователя, домен и пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="3b653-108">The program creates an authentication identity structure and populates the structure with the encoded strings that represent the user name, domain, and password of the user.</span></span> <span data-ttu-id="3b653-109">Затем программа создает задание скачивания BITS и задает закодированное имя пользователя и пароль в качестве учетных данных для задания.</span><span class="sxs-lookup"><span data-stu-id="3b653-109">Then the program creates a BITS download job and sets the encoded user name and password as the credentials for the job.</span></span> <span data-ttu-id="3b653-110">Программа освобождает структуру удостоверений проверки подлинности после того, как она больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="3b653-110">The program frees the authentication identity structure after it is no longer needed.</span></span>

<span data-ttu-id="3b653-111">В этом примере используется заголовок и реализация, определенные в [примере: общие классы](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="3b653-111">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="3b653-112">**Использование кодирования проверки подлинности SSPI с заданиями передачи BITS**</span><span class="sxs-lookup"><span data-stu-id="3b653-112">**To use SSPI authentication encoding with BITS transfer jobs**</span></span>

1.  <span data-ttu-id="3b653-113">Инициализируйте параметры COM, вызвав функцию Ккоинитиализер.</span><span class="sxs-lookup"><span data-stu-id="3b653-113">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="3b653-114">Дополнительные сведения о функции Ккоинитиализер см. в разделе [Пример: общие классы](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="3b653-114">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="3b653-115">Получение указателей для интерфейсов [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="3b653-115">Get pointers for the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interfaces.</span></span> <span data-ttu-id="3b653-116">В этом примере [класс CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) используется для управления указателями на интерфейс COM.</span><span class="sxs-lookup"><span data-stu-id="3b653-116">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="3b653-117">Создайте структуру [ \_ сведений CREDUI](/windows/win32/api/wincred/ns-wincred-credui_infoa) , содержащую сведения о настройке внешнего вида диалогового окна для [функции сспипромптфоркредентиалс](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="3b653-117">Create a [CREDUI\_INFO](/windows/win32/api/wincred/ns-wincred-credui_infoa) structure that contains information for customizing the appearance of the dialog box for the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span> <span data-ttu-id="3b653-118">Затем запросите учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="3b653-118">Then prompt for credentials from the user.</span></span> <span data-ttu-id="3b653-119">Дополнительные сведения см. в описании [функции сспипромптфоркредентиалс](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="3b653-119">For more information, see the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span>
4.  <span data-ttu-id="3b653-120">Кодирование структуры учетных данных в виде строк, которые можно передать в задание передачи BITS с помощью функции [сспиенкодеаусидентитясстрингс](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) .</span><span class="sxs-lookup"><span data-stu-id="3b653-120">Encode credential structure as strings that can be passed to a BITS transfer job by using the [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) function.</span></span>
5.  <span data-ttu-id="3b653-121">Подготовка структуры [**\_ \_ учетных данных для проверки подлинности BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) .</span><span class="sxs-lookup"><span data-stu-id="3b653-121">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span>
6.  <span data-ttu-id="3b653-122">Инициализируйте безопасность процессов COM путем вызова [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="3b653-122">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="3b653-123">Для службы BITS требуется по крайней мере олицетворение уровня IMPERSONATE.</span><span class="sxs-lookup"><span data-stu-id="3b653-123">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="3b653-124">Служба BITS завершается с ошибкой **E \_ ACCESSDENIED** , если не задан правильный уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="3b653-124">BITS fails with **E\_ACCESSDENIED** if the correct impersonation level is not set.</span></span>
7.  <span data-ttu-id="3b653-125">Получите исходный указатель на биты, вызвав функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="3b653-125">Obtain the initial locator to BITS by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
8.  <span data-ttu-id="3b653-126">Создайте задание передачи BITS, вызвав метод [**ибаккграундкопиманажер:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="3b653-126">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
9.  <span data-ttu-id="3b653-127">Получите идентификатор для интерфейса [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) и вызовите метод **использованием метода ibackgroundcopyjob:: QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="3b653-127">Get the identifier for the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface, and call the **IBackgroundCopyJob::QueryInterface** method.</span></span>
10. <span data-ttu-id="3b653-128">Заполните [**структуру \_ \_ учетных данных для проверки**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) подлинности с помощью зашифрованных строк имени пользователя и пароля и задайте для схемы проверки подлинности значение Согласование (схема аутентификации **BG \_ \_ \_ Negotiate**).</span><span class="sxs-lookup"><span data-stu-id="3b653-128">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure with the encoded user name and password strings, and set the authentication scheme to Negotiate (**BG\_AUTH\_SCHEME\_NEGOTIATE**).</span></span>
11. <span data-ttu-id="3b653-129">Используйте указатель [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) для выполнения запросов к службе BITS.</span><span class="sxs-lookup"><span data-stu-id="3b653-129">Use the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) pointer to make requests to BITS.</span></span> <span data-ttu-id="3b653-130">Эта программа использует метод [**IBackgroundCopyJob2:: сеткредентиалс**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) для задания учетных данных для задания передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="3b653-130">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
12. <span data-ttu-id="3b653-131">Добавьте файлы, измените их свойства или возобновите задание передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="3b653-131">Add files, modify properties, or resume the BITS transfer job.</span></span>
13. <span data-ttu-id="3b653-132">После завершения задания передачи BITS удалите задание из очереди, вызвав [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="3b653-132">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>
14. <span data-ttu-id="3b653-133">Наконец, освободите структуру удостоверений проверки подлинности, вызвав функцию [сспифриаусидентити](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) .</span><span class="sxs-lookup"><span data-stu-id="3b653-133">Finally, free the authentication identity structure by calling the [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) function.</span></span>

<span data-ttu-id="3b653-134">В следующем примере кода показано, как использовать кодирование проверки подлинности SSPI с заданиями передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="3b653-134">The following code example demonstrates how to use SSPI Authentication Encoding with BITS transfer jobs.</span></span>


```C++
#define SECURITY_WIN32
#define _SEC_WINNT_AUTH_TYPES

#include <windows.h>
#include <ntsecapi.h>
#include <bits.h>
#include <sspi.h>
#include <wincred.h>
#include <iostream>
#include <atlbase.h>
#include "CommonCode.h"

void PromptForCredentials(PWSTR pwTargetName)
{
    HRESULT hr;
    
    // If CoInitializeEx fails, the exception is unhandled and the program terminates
    CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    CComPtr<IBackgroundCopyManager> pQueueMgr;
    CComPtr<IBackgroundCopyJob> pJob;
    CComPtr<IBackgroundCopyJob2> pJob2;

    PSEC_WINNT_AUTH_IDENTITY_OPAQUE pAuthIdentityEx2 = NULL;
    DWORD dwFlags = 0;
    BOOL fSave = FALSE;
    BOOL bReturn = TRUE;

    CREDUI_INFO creduiInfo = { 0 };
    creduiInfo.cbSize = sizeof(creduiInfo);
    // Change the message text and caption to the actual text for your dialog.
    creduiInfo.pszMessageText = pwTargetName;
    creduiInfo.pszCaptionText = L"SSPIPFC title for the dialog box";

    try {
        // Prompt for credentials from user using Negotiate security package.
        DWORD dwRet = SspiPromptForCredentials(
            pwTargetName,
            &creduiInfo,
            0,
            L"Negotiate", 
            NULL,
            &pAuthIdentityEx2,
            &fSave,
            dwFlags
            );

        if (SEC_E_OK != dwRet) 
        {
            // Prompt for credentials failed.
            throw MyException(dwRet, L"SspiPromptForCredentials");
        }

        if (NULL != pAuthIdentityEx2) 
        {
            GUID guidJob;
            BG_AUTH_CREDENTIALS authCreds;

            PCWSTR pwUserName = NULL;
            PCWSTR pwDomainName = NULL;
            PCWSTR pwPassword = NULL;

            // Encode credential structure as strings that can
            // be passed to a BITS job.
            SECURITY_STATUS secStatus = SspiEncodeAuthIdentityAsStrings(
                pAuthIdentityEx2,
                &pwUserName,
                &pwDomainName,
                &pwPassword
                );

            if(SEC_E_OK != secStatus) 
            {
                // Encode authentication identity as strings.
                throw MyException(secStatus, L"SspiEncodeAuthIdentityAsStrings");   
            }

            // Show the encoded user name and domain name.
            wprintf(
                L"User Name: %s\nDomain Name: %s",
                pwUserName,
                pwDomainName
                );

            //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
            HRESULT hr = CoInitializeSecurity(
                NULL,
                -1,
                NULL,
                NULL,
                RPC_C_AUTHN_LEVEL_CONNECT,
                RPC_C_IMP_LEVEL_IMPERSONATE,
                NULL,
                EOAC_DYNAMIC_CLOAKING,
                0
                );
            
            if (FAILED(hr))
            {
                throw MyException(hr, L"CoInitializeSecurity");
            }

            // Connect to BITS.
            hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                CLSCTX_LOCAL_SERVER,
                __uuidof(IBackgroundCopyManager),
                (void**) &pQueueMgr);

            if (FAILED(hr))
            {
                // Failed to connect.
                throw MyException(hr, L"CoCreateInstance");
            }

            // Create a job.
            hr = pQueueMgr->CreateJob(
                L"EncodeSample", 
                BG_JOB_TYPE_DOWNLOAD, 
                &guidJob, 
                &pJob
                );

            if(FAILED(hr))
            {   
                // Failed to create a BITS job.
                throw MyException(hr, L"CreateJob");
            }

            // Get IBackgroundCopyJob2 interface.
            hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
            if (FAILED(hr)) 
            {
                // Failed to get a reference to the IBackgroundCopyJob2 interface.
                throw MyException(hr, L"QueryInterface(IBackgroundCopyJob2)");
            }

            // Create a BITS authentication structure from the encoded strings.
            authCreds.Target = BG_AUTH_TARGET_SERVER;
            authCreds.Scheme = BG_AUTH_SCHEME_NEGOTIATE;
            authCreds.Credentials.Basic.UserName = (LPWSTR)pwUserName;
            authCreds.Credentials.Basic.Password = (LPWSTR)pwPassword;

            // Set the credentials for the job.
            hr = pJob2->SetCredentials(&authCreds);
            if (FAILED(hr)) 
            {
                // Failed to set credentials.
                throw MyException(hr, L"SetCredentials");
            }

            // Modify the job's property values.
            // Add files to the job.
            // Activate (resume) the job in the transfer queue.

            // Remove the job from the transfer queue.
            hr = pJob->Complete();
            if (FAILED(hr)) 
            {
                // Failed to complete the job.
                throw MyException(hr, L"Complete");
            }
        }
    }
    catch(std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }
    catch(MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }

    // Free the auth identity structure.
    if (NULL != pAuthIdentityEx2)
    {
        SspiFreeAuthIdentity(pAuthIdentityEx2);
        pAuthIdentityEx2 = NULL;
    }

    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{
    PromptForCredentials(L"Target");
}
```



## <a name="related-topics"></a><span data-ttu-id="3b653-135">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3b653-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b653-136">SSPI</span><span class="sxs-lookup"><span data-stu-id="3b653-136">SSPI</span></span>](../secauthn/sspi.md)
</dt> <dt>

[<span data-ttu-id="3b653-137">**ибаккграундкопиманажер**</span><span class="sxs-lookup"><span data-stu-id="3b653-137">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="3b653-138">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="3b653-138">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="3b653-139">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="3b653-139">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="3b653-140">Пример. Общие классы</span><span class="sxs-lookup"><span data-stu-id="3b653-140">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 