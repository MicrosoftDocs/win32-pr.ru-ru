---
title: Пример добавления вспомогательного маркера в задание передачи BITS
description: Вы можете настроить задание передачи фоновая интеллектуальная служба передачи (BITS) с дополнительным маркером безопасности. Задание передачи BITS использует этот вспомогательный токен для проверки подлинности и доступа к ресурсам.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4adab6ca8cebeeca9b9883e89db28205dfdab1ea43e05c01fd119c14c26d374
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528824"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a>Пример. Добавление вспомогательного маркера в задание передачи BITS

Вы можете настроить задание передачи фоновая интеллектуальная служба передачи (BITS) с дополнительным маркером безопасности. Задание передачи BITS использует этот вспомогательный токен для проверки подлинности и доступа к ресурсам.

Дополнительные сведения см. в разделе [вспомогательные токены для заданий передачи BITS](helper-tokens-for-bits-transfer-jobs.md).

Следующая процедура создает задание передачи BITS в контексте локального пользователя, получает учетные данные второго пользователя, создает вспомогательный маркер с этими учетными данными, а затем задает вспомогательный токен для задания передачи BITS.

В этом примере используется заголовок и реализация, определенные в [примере: общие классы](common-classes.md).

**Добавление вспомогательного маркера в задание передачи BITS**

1.  Инициализируйте параметры COM, вызвав функцию Ккоинитиализер. Дополнительные сведения о функции Ккоинитиализер см. в разделе [Пример: общие классы](common-classes.md).
2.  Получает указатель на интерфейс [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) . В этом примере [класс CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) используется для управления указателями на интерфейс COM.
3.  Инициализируйте безопасность процессов COM путем вызова [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Для службы BITS требуется по крайней мере олицетворение уровня IMPERSONATE. Служба BITS завершается с ошибкой E \_ ACCESSDENIED, если не задан правильный уровень олицетворения.
4.  Получите указатель на интерфейс [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) и получите исходный указатель на биты, вызвав функцию [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
5.  Создайте задание передачи BITS, вызвав метод [**ибаккграундкопиманажер:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
6.  Получите указатель на интерфейс обратного вызова Кнотифинтерфаце и вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифинтерфаце**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) , чтобы получать уведомления о событиях, связанных с заданиями. Дополнительные сведения о Кнотифинтерфаце см. в разделе [Пример: общие классы](common-classes.md).
7.  Вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) , чтобы задать типы получаемых уведомлений. В этом примере задаются **\_ задания уведомления BG notify \_ \_** , а также флаги **\_ уведомления о \_ заданиях \_ BG notify** .
8.  Получите указатель на интерфейс [**ибитстокеноптионс**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) , вызвав метод **использованием метода ibackgroundcopyjob:: QueryInterface** с правильным идентификатором интерфейса.
9.  Попытка входа в систему пользователя вспомогательного токена. Создайте маркер олицетворения и вызовите [функцию LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) для заполнения маркера олицетворения. В случае успеха вызовите [функцию имперсонателогжедонусер](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser). Если это не удалось, в примере вызывается [функция RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) для завершения олицетворения вошедшего в систему пользователя, возникает ошибка и закрытый маркер.
10. Вызовите метод [**ибитстокеноптионс:: сеселпертокен**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) для олицетворения маркера вошедшего в систему пользователя. Если этот метод завершается неудачно, в примере вызывается [функция RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) для завершения олицетворения вошедшего в систему пользователя, возникает ошибка и закрытый маркер.
    > [!Note]
    >
    > в поддерживаемых версиях Windows до Windows 10 версии 1607 владелец задания должен иметь учетные данные администратора для вызова метода [**ибитстокеноптионс:: сеселпертокен**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) .
    >
    > начиная с Windows 10 версии 1607, владельцы заданий без прав администратора могут задавать вспомогательные токены без прав администратора в заданиях BITS, которыми они владеют. Владельцы заданий по-прежнему должны иметь учетные данные администратора, чтобы задать вспомогательные маркеры с правами администратора.

     

11. Вызовите метод [**ибитстокеноптионс:: сеселпертокенфлагс**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) , чтобы указать ресурсы для доступа с помощью контекста безопасности вспомогательного токена.
12. После завершения олицетворения в примере вызывается [функция RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) для завершения олицетворения вошедшего в систему пользователя, а маркер закрывается.
13. Добавьте файлы в задание передачи BITS, вызвав [**использованием метода ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).
14. После добавления файла вызовите [**использованием метода ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) , чтобы возобновить задание.
15. Настройте цикл while для ожидания сообщения о выходе из интерфейса обратного вызова во время передачи задания. Цикл while использует функцию [жеттикккаунт](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) для получения числа миллисекунд, прошедших с момента начала передачи задания.
16. После завершения задания передачи BITS удалите задание из очереди, вызвав [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).

В следующем примере кода в задание передачи BITS добавляется вспомогательный маркер.


```C++
#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"


void HelperToken(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &domain, const LPWSTR &username, const LPWSTR &password)
{
// If CoInitializeEx fails, the exception is unhandled and the program terminates   
CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);

CComPtr<IBackgroundCopyJob> pJob; 

    try
    {
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
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void **)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"HelperTokenSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);


        if(FAILED(hr))
        {   
            // Failed to create job.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;    
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to SetNotifyInterface.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to SetNotifyFlags.
            throw MyException(hr, L"SetNotifyFlags");
        }

        //Retrieve the IBitsTokenOptions interface pointer from the BITS transfer job.
        CComPtr<IBitsTokenOptions> pTokenOptions;
        hr = pJob->QueryInterface(__uuidof(IBitsTokenOptions), (void** ) &pTokenOptions);

        if (FAILED(hr))
        {
            // Failed to QueryInterface.
            throw MyException(hr, L"QueryInterface");
        }

        // Log on user of the helper token.
        wprintf(L"Credentials for helper token %s\\%s %s\n", domain, username, password);

        HANDLE hImpersonation = INVALID_HANDLE_VALUE;
        if(LogonUser(username, domain, password, LOGON32_LOGON_INTERACTIVE, LOGON32_PROVIDER_DEFAULT, &hImpersonation))
        {
            // Impersonate the logged-on user.
            if(ImpersonateLoggedOnUser(hImpersonation))
            {
                // Configure the impersonated logged-on user's token as the helper token.
                hr = pTokenOptions->SetHelperToken();        
                if (FAILED(hr))
                {
                    //Failed to set helper token.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperToken");
                }

                hr = pTokenOptions->SetHelperTokenFlags(BG_TOKEN_LOCAL_FILE);
                if (FAILED(hr))
                {
                    //Failed to set helper token flags.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperTokenFlags");
                }

                RevertToSelf();
            }               
            CloseHandle(hImpersonation);
        }

        // Add a file.
        // Replace parameters with variables that contain valid paths.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile,localFile);

        if(FAILED(hr))
        {   
            //Failed to add file to job.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Resume failed.                   
            throw MyException(hr, L"Resume");
        }    
    }
    catch(const std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }
    catch(const MyException &ex)
    {
        wprintf(L"Error 0x%x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack
    DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
    while (dwLimit > GetTickCount())
    {
        MSG msg;

        while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
        { 
            // If it is a quit message, exit.
            if (msg.message == WM_QUIT) 
            {
                return;
            }

            // Otherwise, dispatch the message.
            DispatchMessage(&msg); 
        } // End of PeekMessage while loop
    }

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s ", argv[0]);
        wprintf(L"[remote name] [local name] [helpertoken domain] [helpertoken userrname] [helpertoken password]\n");
        return;
    }

    HelperToken(argv[1],argv[2],argv[3],argv[4],argv[5]);

}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Вспомогательные токены для заданий передачи BITS](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[**ибитстокеноптионс**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[Пример. Общие классы](common-classes.md)
</dt> </dl>

 

 