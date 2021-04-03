---
title: Параметры задачи в примере кода C/C++
description: В этом примере удаляются все параметры командной строки, связанные с известной задачей. В этом примере предполагается, что задача и тестовая задача уже существуют на локальном компьютере.
ms.assetid: cd71379a-7eb2-4966-a28b-5b7d31d60c16
keywords:
- Задание свойств задачи планировщик задач, параметры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509776aa87d414cb1cb4c590c2be2c0ea3912269
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774882"
---
# <a name="cc-code-example-setting-task-parameters"></a><span data-ttu-id="989fb-105">Пример кода C/C++: Задание параметров задачи</span><span class="sxs-lookup"><span data-stu-id="989fb-105">C/C++ Code Example: Setting Task Parameters</span></span>

<span data-ttu-id="989fb-106">В этом примере удаляются все параметры командной строки, связанные с известной задачей.</span><span class="sxs-lookup"><span data-stu-id="989fb-106">This example clears all command-line parameters associated with a known task.</span></span> <span data-ttu-id="989fb-107">В этом примере предполагается, что задача и тестовая задача уже существуют на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="989fb-107">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
  ITaskScheduler *pITS;
  
  hr = CoInitialize(NULL);
  if (SUCCEEDED(hr))
  {
    hr = CoCreateInstance(CLSID_CTaskScheduler,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_ITaskScheduler,
                          (void **) &pITS);
    if (FAILED(hr))
    {
      CoUninitialize();
      return 1;
    }
  }
  else
  {
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::Activate to get the Task object.
  ///////////////////////////////////////////////////////////////////
  ITask *pITask;
  LPCWSTR lpcwszTaskName;
  lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                     (IUnknown**) &pITask);
  
  // Release the ITaskScheduler interface.
  pITS->Release();  
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::SetParameters to L"" to clear the parameters for
  // Test Task.
  ///////////////////////////////////////////////////////////////////
  LPCWSTR pwszParameters = L"";
  
  hr = pITask->SetParameters(pwszParameters);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetParameters: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call IPersistFile::Save to save the modified task to disk.
  ///////////////////////////////////////////////////////////////////
  IPersistFile *pIPersistFile;
  
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  
  // Release the ITask interface.
  pITask->Release();  
  
  hr = pIPersistFile->Save(NULL,
                           TRUE);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling IPersistFile::Save: ");
    wprintf(L"error = 0x%x\n",hr);
    pIPersistFile->Release();
    CoUninitialize();
    return 1;
  }

  // Release the IPersistFile interface.
  pIPersistFile->Release();
  
  wprintf(L"Cleared the parameters of TestTask.\n");
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="989fb-108">См. также</span><span class="sxs-lookup"><span data-stu-id="989fb-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="989fb-109">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="989fb-109">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




