---
title: Контроль загрузки BITS через дорогостоящее подключение
description: Блокировать загрузку с дорогостоящим подключением, например с помощью перемещаемой связи сотовой сети.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- Загрузка BITS, как
- скачивает биты, избегая дорогостоящих
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 6326838f08f1879929d9a6be67ef94c4aa035e00
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "103890100"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a><span data-ttu-id="4f864-105">Контроль загрузки BITS через дорогостоящее подключение</span><span class="sxs-lookup"><span data-stu-id="4f864-105">Control a BITS download over an expensive connection</span></span>

<span data-ttu-id="4f864-106">В этом разделе показано, как заблокировать загрузку задания BITS через дорогостоящее подключение, например в роуминге сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="4f864-106">This topic shows how to block a BITS job from downloading over an expensive connection such as a roaming cellular link.</span></span> <span data-ttu-id="4f864-107">BITS — это асинхронный API, при котором приложение создает задание, добавляет URL-адреса в это задание и вызывает функцию [**возобновления**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) объекта задания.</span><span class="sxs-lookup"><span data-stu-id="4f864-107">BITS is an asynchronous API where the application creates a job, adds URLs to that job, and calls the job object's [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) function.</span></span> <span data-ttu-id="4f864-108">С этого момента служба BITS выбирает время загрузки задания на основе таких факторов, как приоритет задания и политика передачи.</span><span class="sxs-lookup"><span data-stu-id="4f864-108">From that point, BITS chooses when the job downloads based on factors such as job priority and the transfer policy.</span></span> <span data-ttu-id="4f864-109">После завершения загрузки задания служба BITS уведомляет приложение о том, что URL-адрес был скачан (если приложение зарегистрировано для уведомления о завершении).</span><span class="sxs-lookup"><span data-stu-id="4f864-109">After the job has finished downloading, BITS notifies the application that the URL has been downloaded (if the application has registered for completion notification).</span></span> <span data-ttu-id="4f864-110">В течение времени существования задания, если изменяется сеть конечного пользователя (например, если пользователь находится в командировке и в настоящее время накладывается роуминг), служба BITS приостанавливает задание до тех пор, пока не будет оптимальным условием сети.</span><span class="sxs-lookup"><span data-stu-id="4f864-110">During the job's lifetime, if the end user's network changes—such as if the user is traveling and is currently incurring roaming fees—then BITS will suspend the job until network conditions are optimal.</span></span> <span data-ttu-id="4f864-111">В следующих пошаговых инструкциях показано, как создать задание и указать соответствующие параметры политики пересылки.</span><span class="sxs-lookup"><span data-stu-id="4f864-111">The following step-by-step instructions show how to create the job and specify the appropriate transfer policy settings.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4f864-112">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="4f864-112">Prerequisites</span></span>

-   <span data-ttu-id="4f864-113">Microsoft Visual Studio;</span><span class="sxs-lookup"><span data-stu-id="4f864-113">Microsoft Visual Studio</span></span>

## <a name="instructions"></a><span data-ttu-id="4f864-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="4f864-114">Instructions</span></span>

### <a name="step-1-include-the-required-bits-header-files"></a><span data-ttu-id="4f864-115">Шаг 1. Включение необходимых файлов заголовков BITS</span><span class="sxs-lookup"><span data-stu-id="4f864-115">Step 1: Include the required BITS header files</span></span>

<span data-ttu-id="4f864-116">Вставьте следующие директивы заголовка в начало исходного файла.</span><span class="sxs-lookup"><span data-stu-id="4f864-116">Insert the following header directives at the top of the source file.</span></span>


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a><span data-ttu-id="4f864-117">Шаг 2. Инициализация COM</span><span class="sxs-lookup"><span data-stu-id="4f864-117">Step 2: Initialize COM</span></span>

<span data-ttu-id="4f864-118">Перед созданием экземпляра интерфейса [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) (используемого для создания задания BITS) необходимо инициализировать COM, задать com-потоковую модель и указать уровень олицетворения как минимум на \_ уровне IMP на языке RPC C \_ \_ \_ impersonate.</span><span class="sxs-lookup"><span data-stu-id="4f864-118">Before instantiating the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface (used to create a BITS job), you must initialize COM, set the COM threading model, and specify an impersonation level of at least RPC\_C\_IMP\_LEVEL\_IMPERSONATE.</span></span>


```C++
// Initialize COM and specify the COM threading model.
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
 // Specify an impersonation level of at least RPC_C_IMP_LEVEL_IMPERSONATE.
 hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                           RPC_C_AUTHN_LEVEL_CONNECT,
                           RPC_C_IMP_LEVEL_IMPERSONATE,
                           NULL, EOAC_NONE, 0);
 if (SUCCEEDED(hr))
 {
  ...
```



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a><span data-ttu-id="4f864-119">Шаг 3. Создание экземпляра интерфейса Ибаккграундкопиманажер</span><span class="sxs-lookup"><span data-stu-id="4f864-119">Step 3: Instantiate the IBackgroundCopyManager interface</span></span>

<span data-ttu-id="4f864-120">Используйте интерфейс [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) для создания заданий перемещения, получения объекта перечислителя, содержащего задания в очереди, и извлечения отдельных заданий из очереди.</span><span class="sxs-lookup"><span data-stu-id="4f864-120">Use the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to create transfer jobs, retrieve an enumerator object that contains the jobs in the queue, and retrieve individual jobs from the queue.</span></span>


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a><span data-ttu-id="4f864-121">Шаг 4. Создание задания BITS</span><span class="sxs-lookup"><span data-stu-id="4f864-121">Step 4: Create the BITS job</span></span>

<span data-ttu-id="4f864-122">Только пользователь, создающий задание или пользователь с правами администратора, может добавлять файлы в задание и изменять свойства задания.</span><span class="sxs-lookup"><span data-stu-id="4f864-122">Only the user who creates the job or a user with administrator privileges can add files to the job and change the job's properties.</span></span>


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a><span data-ttu-id="4f864-123">Шаг 5. Указание параметра политики перемещения для задания</span><span class="sxs-lookup"><span data-stu-id="4f864-123">Step 5: Specify the transfer policy setting for the job</span></span>

<span data-ttu-id="4f864-124">Здесь указывается политика перемещения состояния затрат.</span><span class="sxs-lookup"><span data-stu-id="4f864-124">This is where you specify the cost state transfer policy.</span></span> <span data-ttu-id="4f864-125">Можно установить несколько \_ \_ флагов состояния стоимости BITS, используя побитовое сочетание **или** для достижения нужных результатов.</span><span class="sxs-lookup"><span data-stu-id="4f864-125">You can set several BITS\_COST\_STATE flags by using a bitwise **OR** combination to achieve the desired results.</span></span>


```C++
BITS_JOB_PROPERTY_VALUE propval;
IBackgroundCopyJob5* pBackgroundCopyJob5;

propval.Dword = BITS_COST_STATE_USAGE_BASED
              | BITS_COST_STATE_OVERCAP_THROTTLED
              | BITS_COST_STATE_BELOW_CAP
              | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
              | BITS_COST_STATE_UNRESTRICTED;

hr = pBackgroundCopyJob->QueryInterface(__uuidof(IBackgroundCopyJob5),
                                        reinterpret_cast<void**>(&pBackgroundCopyJob5));
if(SUCCEEDED(hr))
{
 pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);
}
```



## <a name="example"></a><span data-ttu-id="4f864-126">Пример</span><span class="sxs-lookup"><span data-stu-id="4f864-126">Example</span></span>

<span data-ttu-id="4f864-127">В следующем примере кода показано, как задать политику передачи задания BITS таким образом, чтобы обработка задания не выполнялась в то время, когда выполняются определенные условия (например, когда пользователь находится в роуминге или превышено ограничение месячной передачи данных).</span><span class="sxs-lookup"><span data-stu-id="4f864-127">The following code example shows how to set a BITS job's transfer policy so that the processing of the job doesn't occur while certain conditions are met—such as when the user is roaming or has exceeded their monthly data transfer limit.</span></span>


```C++
//*********************************************************
//
//    Copyright (c) Microsoft. All rights reserved.
//    This code is licensed under the Microsoft Public License.
//    THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF
//    ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY
//    IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR
//    PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.
//
//*********************************************************

#define WIN32_LEAN_AND_MEAN             // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <stdio.h> // define wprintf


int main()
{
 HRESULT hr = S_OK;
 GUID guidJob;
 IBackgroundCopyJob5* pBackgroundCopyJob5;  
 IBackgroundCopyJob* pBackgroundCopyJob;
 IBackgroundCopyManager* pQueueMgr;
 BITS_JOB_PROPERTY_VALUE propval;

 // Specify the COM threading model.
 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 if (SUCCEEDED(hr))
 {
  // The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
  hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                            RPC_C_AUTHN_LEVEL_CONNECT,
                            RPC_C_IMP_LEVEL_IMPERSONATE,
                            NULL, EOAC_NONE, 0);

  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(__uuidof(BackgroundCopyManager), 
                         NULL,
                         CLSCTX_LOCAL_SERVER,
                         __uuidof(IBackgroundCopyManager),
                         (void **)&pQueueMgr);

   if (FAILED(hr))
   {
    // Failed to connect to BITS.
    wprintf(L"Failed to connect to BITS with error %x\n",hr);
    goto done;
   }

   // Create a BITS job.
   wprintf(L"Creating Job...\n");

   hr = pQueueMgr->CreateJob(L"TransferPolicy",
                             BG_JOB_TYPE_DOWNLOAD,
                             &guidJob,
                             (IBackgroundCopyJob **)&pBackgroundCopyJob);

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }

   wprintf(L" Job is succesfully created ...\n");

   // Set the Transfer Policy for the job.
   propval.Dword = BITS_COST_STATE_USAGE_BASED 
                 | BITS_COST_STATE_OVERCAP_THROTTLED
                 | BITS_COST_STATE_BELOW_CAP
                 | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
                 | BITS_COST_STATE_UNRESTRICTED;

   hr = pBackgroundCopyJob->QueryInterface(
         __uuidof(IBackgroundCopyJob5),
         reinterpret_cast<void**>(&pBackgroundCopyJob5)
        );

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }
   pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);

   // Get the Transfer Policy for the new job.
   BITS_JOB_PROPERTY_VALUE actual_propval;

   wprintf(L"Getting TransferPolicy Property ...\n");

   hr = pBackgroundCopyJob5->GetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, 
                                         &actual_propval);
   if (FAILED(hr))
   {
    // SetSSLSecurityFlags failed.
    wprintf(L"GetProperty failed with error %x\n",hr);
    goto cancel;
   }

   DWORD job_transferpolicy = actual_propval.Dword;
   wprintf(L"get TransferPolicy Property returned %#x\n", job_transferpolicy);
  }
done:
  CoUninitialize();
 }
 return 1;

cancel:
 pBackgroundCopyJob->Cancel(); 
 pBackgroundCopyJob->Release();
 goto done;
}
```



 

 




