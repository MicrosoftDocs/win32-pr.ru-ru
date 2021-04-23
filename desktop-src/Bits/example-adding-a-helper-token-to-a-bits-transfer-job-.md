---
title: Пример добавления вспомогательного маркера в задание передачи BITS
description: Вы можете настроить задание передачи фоновая интеллектуальная служба передачи (BITS) с дополнительным маркером безопасности. Задание передачи BITS использует этот вспомогательный токен для проверки подлинности и доступа к ресурсам.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab12fe93ae54d91d02bef5e59e99d267571413e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070552"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a><span data-ttu-id="7479d-104">Пример. Добавление вспомогательного маркера в задание передачи BITS</span><span class="sxs-lookup"><span data-stu-id="7479d-104">Example: Adding a Helper Token to a BITS Transfer Job</span></span>

<span data-ttu-id="7479d-105">Вы можете настроить задание передачи фоновая интеллектуальная служба передачи (BITS) с дополнительным маркером безопасности.</span><span class="sxs-lookup"><span data-stu-id="7479d-105">You can configure a Background Intelligent Transfer Service (BITS) transfer job with an additional security token.</span></span> <span data-ttu-id="7479d-106">Задание передачи BITS использует этот вспомогательный токен для проверки подлинности и доступа к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="7479d-106">The BITS transfer job uses this helper token for authentication and to access resources.</span></span>

<span data-ttu-id="7479d-107">Дополнительные сведения см. в разделе [вспомогательные токены для заданий передачи BITS](helper-tokens-for-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="7479d-107">For more information, see [Helper tokens for BITS transfer jobs](helper-tokens-for-bits-transfer-jobs.md).</span></span>

<span data-ttu-id="7479d-108">Следующая процедура создает задание передачи BITS в контексте локального пользователя, получает учетные данные второго пользователя, создает вспомогательный маркер с этими учетными данными, а затем задает вспомогательный токен для задания передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="7479d-108">The following procedure creates a BITS transfer job in the context of the local user, gets credentials of a second user, creates a helper token with these credentials, and then sets the helper token on the BITS transfer job.</span></span>

<span data-ttu-id="7479d-109">В этом примере используется заголовок и реализация, определенные в [примере: общие классы](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7479d-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="7479d-110">**Добавление вспомогательного маркера в задание передачи BITS**</span><span class="sxs-lookup"><span data-stu-id="7479d-110">**To add a helper token to a BITS transfer job**</span></span>

1.  <span data-ttu-id="7479d-111">Инициализируйте параметры COM, вызвав функцию Ккоинитиализер.</span><span class="sxs-lookup"><span data-stu-id="7479d-111">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="7479d-112">Дополнительные сведения о функции Ккоинитиализер см. в разделе [Пример: общие классы](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7479d-112">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="7479d-113">Получает указатель на интерфейс [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) .</span><span class="sxs-lookup"><span data-stu-id="7479d-113">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface.</span></span> <span data-ttu-id="7479d-114">В этом примере [класс CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) используется для управления указателями на интерфейс COM.</span><span class="sxs-lookup"><span data-stu-id="7479d-114">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="7479d-115">Инициализируйте безопасность процессов COM путем вызова [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="7479d-115">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="7479d-116">Для службы BITS требуется по крайней мере олицетворение уровня IMPERSONATE.</span><span class="sxs-lookup"><span data-stu-id="7479d-116">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="7479d-117">Служба BITS завершается с ошибкой E \_ ACCESSDENIED, если не задан правильный уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="7479d-117">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
4.  <span data-ttu-id="7479d-118">Получите указатель на интерфейс [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) и получите исходный указатель на биты, вызвав функцию [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="7479d-118">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
5.  <span data-ttu-id="7479d-119">Создайте задание передачи BITS, вызвав метод [**ибаккграундкопиманажер:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="7479d-119">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
6.  <span data-ttu-id="7479d-120">Получите указатель на интерфейс обратного вызова Кнотифинтерфаце и вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифинтерфаце**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) , чтобы получать уведомления о событиях, связанных с заданиями.</span><span class="sxs-lookup"><span data-stu-id="7479d-120">Get a pointer to the CNotifyInterface callback interface, and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="7479d-121">Дополнительные сведения о Кнотифинтерфаце см. в разделе [Пример: общие классы](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7479d-121">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
7.  <span data-ttu-id="7479d-122">Вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) , чтобы задать типы получаемых уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7479d-122">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="7479d-123">В этом примере задаются **\_ задания уведомления BG notify \_ \_** , а также флаги **\_ уведомления о \_ заданиях \_ BG notify** .</span><span class="sxs-lookup"><span data-stu-id="7479d-123">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
8.  <span data-ttu-id="7479d-124">Получите указатель на интерфейс [**ибитстокеноптионс**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) , вызвав метод **использованием метода ibackgroundcopyjob:: QueryInterface** с правильным идентификатором интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7479d-124">Get a pointer to the [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) interface by calling the **IBackgroundCopyJob::QueryInterface** method with the proper interface identifier.</span></span>
9.  <span data-ttu-id="7479d-125">Попытка входа в систему пользователя вспомогательного токена.</span><span class="sxs-lookup"><span data-stu-id="7479d-125">Attempt to log on the user of the helper token.</span></span> <span data-ttu-id="7479d-126">Создайте маркер олицетворения и вызовите [функцию LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) для заполнения маркера олицетворения.</span><span class="sxs-lookup"><span data-stu-id="7479d-126">Create an impersonation handle, and call the [LogonUser Function]( /windows/win32/api/winbase/nf-winbase-logonusera) to populate the impersonation handle.</span></span> <span data-ttu-id="7479d-127">В случае успеха вызовите [функцию имперсонателогжедонусер](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span><span class="sxs-lookup"><span data-stu-id="7479d-127">If successful, call the [ImpersonateLoggedOnUser Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span></span> <span data-ttu-id="7479d-128">Если это не удалось, в примере вызывается [функция RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) для завершения олицетворения вошедшего в систему пользователя, возникает ошибка и закрытый маркер.</span><span class="sxs-lookup"><span data-stu-id="7479d-128">If unsuccessful, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
10. <span data-ttu-id="7479d-129">Вызовите метод [**ибитстокеноптионс:: сеселпертокен**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) для олицетворения маркера вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="7479d-129">Call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method to impersonate the token of the logged-on user.</span></span> <span data-ttu-id="7479d-130">Если этот метод завершается неудачно, в примере вызывается [функция RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) для завершения олицетворения вошедшего в систему пользователя, возникает ошибка и закрытый маркер.</span><span class="sxs-lookup"><span data-stu-id="7479d-130">If this method fails, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
    > [!Note]
    >
    > <span data-ttu-id="7479d-131">В поддерживаемых версиях Windows до Windows 10 версии 1607 владелец задания должен иметь административные учетные данные для вызова метода [**ибитстокеноптионс:: сеселпертокен**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) .</span><span class="sxs-lookup"><span data-stu-id="7479d-131">In supported versions of Windows before Windows 10, version 1607, the job owner must have administrative credentials to call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method.</span></span>
    >
    > <span data-ttu-id="7479d-132">Начиная с версии 1607, владельцы заданий без прав администратора могут задавать вспомогательные токены без прав администратора в заданиях BITS, которыми они владеют.</span><span class="sxs-lookup"><span data-stu-id="7479d-132">Starting with Windows 10, version 1607, non-administrator job owners can set non-administrator helper tokens on BITS jobs they own.</span></span> <span data-ttu-id="7479d-133">Владельцы заданий по-прежнему должны иметь учетные данные администратора, чтобы задать вспомогательные маркеры с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="7479d-133">Job owners must still have administrative credentials to set helper tokens with administrator privileges.</span></span>

     

11. <span data-ttu-id="7479d-134">Вызовите метод [**ибитстокеноптионс:: сеселпертокенфлагс**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) , чтобы указать ресурсы для доступа с помощью контекста безопасности вспомогательного токена.</span><span class="sxs-lookup"><span data-stu-id="7479d-134">Call the [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) method to specify which resources to access using the helper token's security context.</span></span>
12. <span data-ttu-id="7479d-135">После завершения олицетворения в примере вызывается [функция RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) для завершения олицетворения вошедшего в систему пользователя, а маркер закрывается.</span><span class="sxs-lookup"><span data-stu-id="7479d-135">After the impersonation is complete, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of logged on user, and the handle is closed.</span></span>
13. <span data-ttu-id="7479d-136">Добавьте файлы в задание передачи BITS, вызвав [**использованием метода ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span><span class="sxs-lookup"><span data-stu-id="7479d-136">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span>
14. <span data-ttu-id="7479d-137">После добавления файла вызовите [**использованием метода ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) , чтобы возобновить задание.</span><span class="sxs-lookup"><span data-stu-id="7479d-137">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="7479d-138">Настройте цикл while для ожидания сообщения о выходе из интерфейса обратного вызова во время передачи задания.</span><span class="sxs-lookup"><span data-stu-id="7479d-138">Set up a while loop to wait for the quit message from the callback interface while the job is transferring.</span></span> <span data-ttu-id="7479d-139">Цикл while использует функцию [жеттикккаунт](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) для получения числа миллисекунд, прошедших с момента начала передачи задания.</span><span class="sxs-lookup"><span data-stu-id="7479d-139">The while loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>
16. <span data-ttu-id="7479d-140">После завершения задания передачи BITS удалите задание из очереди, вызвав [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="7479d-140">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="7479d-141">В следующем примере кода в задание передачи BITS добавляется вспомогательный маркер.</span><span class="sxs-lookup"><span data-stu-id="7479d-141">The following code example adds a helper token to a BITS transfer job.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7479d-142">См. также</span><span class="sxs-lookup"><span data-stu-id="7479d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7479d-143">Вспомогательные токены для заданий передачи BITS</span><span class="sxs-lookup"><span data-stu-id="7479d-143">Helper tokens for BITS transfer jobs</span></span>](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[<span data-ttu-id="7479d-144">**ибитстокеноптионс**</span><span class="sxs-lookup"><span data-stu-id="7479d-144">**IBitsTokenOptions**</span></span>](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[<span data-ttu-id="7479d-145">Пример. Общие классы</span><span class="sxs-lookup"><span data-stu-id="7479d-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 