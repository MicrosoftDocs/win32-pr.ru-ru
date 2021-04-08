---
title: Пример кода C/C++ Настройка имени приложения
description: В этом примере задается имя приложения, связанного с известной задачей. В этом примере предполагается, что задача \ 0034; задача тестирования \ 0034; уже существует на локальном компьютере, а служба планировщик задач запущена.
ms.assetid: 1d86f945-0f13-4a7f-8123-df7e63a02238
keywords:
- Задание свойств задачи планировщик задач, имя приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc5ce664079217778e08dcd44ef8c646a4c4eaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068069"
---
# <a name="cc-code-example-setting-application-name"></a><span data-ttu-id="a2c2b-105">Пример кода C/C++: Задание имени приложения</span><span class="sxs-lookup"><span data-stu-id="a2c2b-105">C/C++ Code Example: Setting Application Name</span></span>

<span data-ttu-id="a2c2b-106">В этом примере задается имя приложения, связанного с известной задачей.</span><span class="sxs-lookup"><span data-stu-id="a2c2b-106">This example sets the name of the application associated with a known task.</span></span> <span data-ttu-id="a2c2b-107">В этом примере предполагается, что задача "тестовая задача" уже существует на локальном компьютере, а служба планировщик задач запущена.</span><span class="sxs-lookup"><span data-stu-id="a2c2b-107">This example assumes that the task "test task" already exists on the local computer and that the Task Scheduler service is running.</span></span>


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
  // Call ITask::SetApplicationName to specify the Application name
  // for Test Task.
  ///////////////////////////////////////////////////////////////////
  LPCWSTR pwszApplicationName = L"C:\\Windows\\System32\\notepad.exe";
 
  hr = pITask->SetApplicationName(pwszApplicationName);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetApplicationName: ");
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
  
  wprintf(L"Set the application name for Test Task.\n");  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="a2c2b-108">См. также</span><span class="sxs-lookup"><span data-stu-id="a2c2b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2c2b-109">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="a2c2b-109">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




