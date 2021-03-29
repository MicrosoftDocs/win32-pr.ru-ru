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
# <a name="registering-to-execute-a-program"></a>Регистрация для выполнения программы

Вы можете зарегистрироваться, чтобы служба BITS выполняла программу на основе переданных заданий и событий ошибок, но не событий изменения задания. Служба BITS выполняет программу в контексте пользователя.

**Регистрация для выполнения программы**

1.  Вызовите метод **использованием метода ibackgroundcopyjob:: QueryInterface** , чтобы получить указатель интерфейса [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) . Укажите \_ \_ Ууидоф (IBackgroundCopyJob2) в качестве идентификатора интерфейса.
2.  Вызовите метод [**IBackgroundCopyJob2:: сетнотификмдлине**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) , чтобы указать программу для выполнения, и любые аргументы, необходимые для программы, например идентификатор задания.

3.  Вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) , чтобы указать время выполнения командной строки.

    Можно указать только \_ передаваемые задания с уведомлением BG \_ \_ и \_ \_ \_ Флаги события ошибки задания BG notify. \_ \_ Флаг изменения уведомления для задания BG \_ игнорируется.

Обратите внимание, что служба BITS не будет выполнять программу, если вы также [зарегистрировались для получения обратных вызовов COM](registering-a-com-callback.md) , а указатель интерфейса обратного вызова является допустимым, или метод уведомления, который вызывается BITS, возвращает код успешного выполнения. Однако если метод уведомления возвращает код ошибки, например е \_ Failed, то BITS выполнит командную строку.

Служба BITS вызывает функцию [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) для запуска программы. Если указать строку параметра, первый параметр должен быть именем программы.

В следующем примере показано, как выполнить регистрацию для выполнения программы при возникновении события, переданного при передаче задания. В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым.


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



Когда состояние задания \_ \_ передается в состояние задания BG \_ , BITS выполняет программу, указанную в ппрограм. Следующий пример представляет собой простую реализацию программы, которая принимает идентификатор задания в качестве аргумента. Программа предполагает, что ей передано правильное количество аргументов.


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



 

 