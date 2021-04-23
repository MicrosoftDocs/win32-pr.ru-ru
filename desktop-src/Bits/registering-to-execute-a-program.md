---
title: Регистрация для выполнения программы
description: Вы можете зарегистрироваться, чтобы служба BITS выполняла программу на основе переданных заданий и событий ошибок, но не событий изменения задания. Служба BITS выполняет программу в контексте пользователя.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- БИТЫ уведомлений о событиях, Командная строка
- Регистрация для получения битов уведомлений командной строки
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7831a959a73112b21bdf3e0fbc2b7d3dd4f6a447
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792259"
---
# <a name="registering-to-execute-a-program"></a><span data-ttu-id="5b5c8-106">Регистрация для выполнения программы</span><span class="sxs-lookup"><span data-stu-id="5b5c8-106">Registering to Execute a Program</span></span>

<span data-ttu-id="5b5c8-107">Вы можете зарегистрироваться, чтобы служба BITS выполняла программу на основе переданных заданий и событий ошибок, но не событий изменения задания.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-107">You can register to have BITS execute a program based on job transferred and error events, but not job modified events.</span></span> <span data-ttu-id="5b5c8-108">Служба BITS выполняет программу в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-108">BITS executes the program in the user's context.</span></span>

<span data-ttu-id="5b5c8-109">**Регистрация для выполнения программы**</span><span class="sxs-lookup"><span data-stu-id="5b5c8-109">**To register to execute a program**</span></span>

1.  <span data-ttu-id="5b5c8-110">Вызовите метод **использованием метода ibackgroundcopyjob:: QueryInterface** , чтобы получить указатель интерфейса [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="5b5c8-110">Call the **IBackgroundCopyJob::QueryInterface** method to retrieve an [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface pointer.</span></span> <span data-ttu-id="5b5c8-111">Укажите \_ \_ Ууидоф (IBackgroundCopyJob2) в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-111">Specify \_\_uuidof(IBackgroundCopyJob2) as the interface identifier.</span></span>
2.  <span data-ttu-id="5b5c8-112">Вызовите метод [**IBackgroundCopyJob2:: сетнотификмдлине**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) , чтобы указать программу для выполнения, и любые аргументы, необходимые для программы, например идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-112">Call the [**IBackgroundCopyJob2::SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) method to specify the program to execute and any arguments required by the program, such as the job identifier.</span></span>

3.  <span data-ttu-id="5b5c8-113">Вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) , чтобы указать время выполнения командной строки.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-113">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to specify when the command line executes.</span></span>

    <span data-ttu-id="5b5c8-114">Можно указать только \_ передаваемые задания с уведомлением BG \_ \_ и \_ \_ \_ Флаги события ошибки задания BG notify.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-114">You can only specify the BG\_NOTIFY\_JOB\_TRANSFERRED and BG\_NOTIFY\_JOB\_ERROR event flags.</span></span> <span data-ttu-id="5b5c8-115">\_ \_ Флаг изменения уведомления для задания BG \_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-115">The BG\_NOTIFY\_JOB\_MODIFICATION flag is ignored.</span></span>

<span data-ttu-id="5b5c8-116">Обратите внимание, что служба BITS не будет выполнять программу, если вы также [зарегистрировались для получения обратных вызовов COM](registering-a-com-callback.md) , а указатель интерфейса обратного вызова является допустимым, или метод уведомления, который вызывается BITS, возвращает код успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-116">Note that BITS will not execute the program if you also [registered to receive COM callbacks](registering-a-com-callback.md) and the callback interface pointer is valid or the notification method that BITS calls returns a success code.</span></span> <span data-ttu-id="5b5c8-117">Однако если метод уведомления возвращает код ошибки, например е \_ Failed, то BITS выполнит командную строку.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-117">However, if the notification method returns a failure code, such as E\_FAIL, BITS will execute the command line.</span></span>

<span data-ttu-id="5b5c8-118">Служба BITS вызывает функцию [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) для запуска программы.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-118">BITS calls the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function to launch the program.</span></span> <span data-ttu-id="5b5c8-119">Если указать строку параметра, первый параметр должен быть именем программы.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-119">If you specify a parameter string, the first parameter must be the program name.</span></span>

<span data-ttu-id="5b5c8-120">В следующем примере показано, как выполнить регистрацию для выполнения программы при возникновении события, переданного при передаче задания.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-120">The following example shows how to register to execute a program when the job-transferred event occurs.</span></span> <span data-ttu-id="5b5c8-121">В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-121">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
#define MAX_PARAMETER_LEN 4000

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szJobId[48];
const WCHAR *pProgram = L"c:\\PATHHERE\\PROGRAMNAMEHERE.exe";
WCHAR szParameters[MAX_PARAMETER_LEN+1];
GUID JobId;
int rc;

hr = pJob->GetId(&JobId);
if (SUCCEEDED(hr))
{
  rc = StringFromGUID2(JobId, szJobId, ARRAYSIZE(szJobId));
  if (rc)
  {
    StringCchPrintf(szParameters, MAX_PARAMETER_LEN+1, L"%s %s", pProgram, szJobId);
    pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
    hr = pJob2->SetNotifyCmdLine(pProgram, szParameters);
    if (SUCCEEDED(hr))
    {
      hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED);
    }
    pJob2->Release();
    if (FAILED(hr))
    {
      //Handle error - unable to register for command line notification.
    }
  }
}
```



<span data-ttu-id="5b5c8-122">Когда состояние задания \_ \_ передается в состояние задания BG \_ , BITS выполняет программу, указанную в ппрограм.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-122">When the state of the job becomes BG\_JOB\_STATE\_TRANSFERRED, BITS executes the program specified in pProgram.</span></span> <span data-ttu-id="5b5c8-123">Следующий пример представляет собой простую реализацию программы, которая принимает идентификатор задания в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-123">The following example is a simple implementation of a program that takes a job identifier as an argument.</span></span> <span data-ttu-id="5b5c8-124">Программа предполагает, что ей передано правильное количество аргументов.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-124">The program assumes the correct number of arguments are passed to it.</span></span>


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <strsafe.h>

int wmain(int argc, wchar_t *argv[])
{
 HRESULT hr;
 IBackgroundCopyManager *pManager = NULL;
 IBackgroundCopyJob *pJob = NULL;
 GUID JobId;
 LPWSTR pDisplayName = NULL;
 LPCWSTR pSuccessString = L" completed successfully.";
 LPWSTR pMessage;

 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
  NULL, CLSCTX_LOCAL_SERVER,
  __uuidof(IBackgroundCopyManager), (void**)&pManager);

 if (pManager)
 {
  hr = CLSIDFromString(argv[1], &JobId);
  if (SUCCEEDED(hr))
  {
   hr = pManager->GetJob(JobId, &pJob);
   if (SUCCEEDED(hr))
   {
    hr = pJob->GetDisplayName(&pDisplayName);
    if (SUCCEEDED(hr))
    {
     int messageLen = wcslen(pDisplayName) + wcslen(pSuccessString) + 1;
     pMessage = (WCHAR*)malloc(messageLen * sizeof(WCHAR));
     if (pMessage)
     {
      StringCchPrintf(pMessage, messageLen,
       L"%s%s", pDisplayName, pSuccessString);
      MessageBox(HWND_DESKTOP, pMessage, L"MyProgram - Transferred", MB_OK);
      free(pMessage);
     }
     else
     {
      hr = E_OUTOFMEMORY;
     }
     CoTaskMemFree(pDisplayName);
    }
    pJob->Release();
   }
  }
  pManager->Release();
 }

 CoUninitialize();
 return(hr);
}
```



 

 