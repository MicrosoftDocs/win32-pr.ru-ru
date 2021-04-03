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
# <a name="example-using-sspi-authentication-encoding-with-bits"></a>Пример. Использование кодирования проверки подлинности SSPI с BITS

Вы можете использовать методы проверки подлинности (SSPI) и фоновая интеллектуальная служба передачи (BITS) для получения учетных данных от пользователя, кодирования учетных данных и установки закодированных учетных данных для задания передачи BITS. Для преобразования структуры учетных данных в строки, которые можно передать в задание передачи BITS, требуется кодирование.

Дополнительные сведения о проверке подлинности и методах SSPI см. в разделе [SSPI](../secauthn/sspi.md).

Следующая процедура запрашивает учетные данные пользователя с помощью пакета безопасности Negotiate. Программа создает структуру идентификации проверки подлинности и заполняет структуру закодированными строками, представляющими имя пользователя, домен и пароль пользователя. Затем программа создает задание скачивания BITS и задает закодированное имя пользователя и пароль в качестве учетных данных для задания. Программа освобождает структуру удостоверений проверки подлинности после того, как она больше не нужна.

В этом примере используется заголовок и реализация, определенные в [примере: общие классы](common-classes.md).

**Использование кодирования проверки подлинности SSPI с заданиями передачи BITS**

1.  Инициализируйте параметры COM, вызвав функцию Ккоинитиализер. Дополнительные сведения о функции Ккоинитиализер см. в разделе [Пример: общие классы](common-classes.md).
2.  Получение указателей для интерфейсов [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) . В этом примере [класс CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) используется для управления указателями на интерфейс COM.
3.  Создайте структуру [ \_ сведений CREDUI](/windows/win32/api/wincred/ns-wincred-credui_infoa) , содержащую сведения о настройке внешнего вида диалогового окна для [функции сспипромптфоркредентиалс](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa). Затем запросите учетные данные пользователя. Дополнительные сведения см. в описании [функции сспипромптфоркредентиалс](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).
4.  Кодирование структуры учетных данных в виде строк, которые можно передать в задание передачи BITS с помощью функции [сспиенкодеаусидентитясстрингс](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) .
5.  Подготовка структуры [**\_ \_ учетных данных для проверки подлинности BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) .
6.  Инициализируйте безопасность процессов COM путем вызова [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Для службы BITS требуется по крайней мере олицетворение уровня IMPERSONATE. Служба BITS завершается с ошибкой **E \_ ACCESSDENIED** , если не задан правильный уровень олицетворения.
7.  Получите исходный указатель на биты, вызвав функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
8.  Создайте задание передачи BITS, вызвав метод [**ибаккграундкопиманажер:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
9.  Получите идентификатор для интерфейса [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) и вызовите метод **использованием метода ibackgroundcopyjob:: QueryInterface** .
10. Заполните [**структуру \_ \_ учетных данных для проверки**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) подлинности с помощью зашифрованных строк имени пользователя и пароля и задайте для схемы проверки подлинности значение Согласование (схема аутентификации **BG \_ \_ \_ Negotiate**).
11. Используйте указатель [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) для выполнения запросов к службе BITS. Эта программа использует метод [**IBackgroundCopyJob2:: сеткредентиалс**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) для задания учетных данных для задания передачи BITS.
12. Добавьте файлы, измените их свойства или возобновите задание передачи BITS.
13. После завершения задания передачи BITS удалите задание из очереди, вызвав [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).
14. Наконец, освободите структуру удостоверений проверки подлинности, вызвав функцию [сспифриаусидентити](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) .

В следующем примере кода показано, как использовать кодирование проверки подлинности SSPI с заданиями передачи BITS.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[SSPI](../secauthn/sspi.md)
</dt> <dt>

[**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Пример. Общие классы](common-classes.md)
</dt> </dl>

 

 