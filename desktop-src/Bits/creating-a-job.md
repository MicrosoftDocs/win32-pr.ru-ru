---
title: Создание задания
description: Чтобы создать задание перемещения, вызовите метод Ибаккграундкопиманажер CreateJob.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- БИТЫ задания передачи
- БИТЫ заданий передачи, создание
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8dddb2427fde43014a31e81f72711ca74e69de34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486661"
---
# <a name="creating-a-job"></a><span data-ttu-id="ebed7-105">Создание задания</span><span class="sxs-lookup"><span data-stu-id="ebed7-105">Creating a Job</span></span>

<span data-ttu-id="ebed7-106">Чтобы создать задание перемещения, вызовите метод [**ибаккграундкопиманажер:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="ebed7-106">To create a transfer job, call the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span> <span data-ttu-id="ebed7-107">После создания задания службы BITS [добавляют файлы в задание](adding-files-to-a-job.md) и [изменяют свойства задания](setting-and-retrieving-the-properties-of-a-job.md) в соответствии с вашими приложениями.</span><span class="sxs-lookup"><span data-stu-id="ebed7-107">After BITS creates the job, [add files to the job](adding-files-to-a-job.md) and [modify the job's properties](setting-and-retrieving-the-properties-of-a-job.md) as appropriate for your application.</span></span> <span data-ttu-id="ebed7-108">Чтобы активировать задание в очереди, вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .</span><span class="sxs-lookup"><span data-stu-id="ebed7-108">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method.</span></span>

<span data-ttu-id="ebed7-109">Метод [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) создает идентификатор GUID, который однозначно идентифицирует задание.</span><span class="sxs-lookup"><span data-stu-id="ebed7-109">The [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method creates a GUID that uniquely identifies the job.</span></span> <span data-ttu-id="ebed7-110">Идентификатор GUID используется для [получения задания из очереди на перемещение](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="ebed7-110">You use the GUID to [retrieve the job from the transfer queue](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span> <span data-ttu-id="ebed7-111">Отображаемое имя, которое вы задаете при создании задания, не является уникальным; более одного задания могут использовать одно и то же имя.</span><span class="sxs-lookup"><span data-stu-id="ebed7-111">The display name that you provide when you create the job is not unique; more than one job can use the same name.</span></span>

<span data-ttu-id="ebed7-112">BITS ограничивает количество заданий в очереди до 300 заданий и число заданий, которые пользователь может создать в 60.</span><span class="sxs-lookup"><span data-stu-id="ebed7-112">BITS limits the number of jobs in the queue to 300 jobs and the number of jobs that a user can create to 60 job.</span></span> <span data-ttu-id="ebed7-113">Эти ограничения не применяются к администраторам и службам.</span><span class="sxs-lookup"><span data-stu-id="ebed7-113">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="ebed7-114">Сведения об изменении этих ограничений по умолчанию см. в разделе [групповые политики](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ebed7-114">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="ebed7-115">В следующем примере показано, как создать задание загрузки.</span><span class="sxs-lookup"><span data-stu-id="ebed7-115">The following example shows how to create a download job.</span></span> <span data-ttu-id="ebed7-116">В примере предполагается, что \_ переменная g пбкм является допустимым указателем интерфейса [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="ebed7-116">The example assumes the g\_pbcm variable is a valid [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="ebed7-117">Дополнительные сведения о создании указателя на интерфейс **ибаккграундкопиманажер** см. в разделе [Подключение к службе BITS](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="ebed7-117">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


```C++
HRESULT hr;
GUID JobId;
IBackgroundCopyJob* pJob = NULL;

//To create an upload job, replace BG_JOB_TYPE_DOWNLOAD with 
//BG_JOB_TYPE_UPLOAD or BG_JOB_TYPE_UPLOAD_REPLY.
hr = g_pbcm->CreateJob(L"MyJobName", BG_JOB_TYPE_DOWNLOAD, &JobId, &pJob);
if (SUCCEEDED(hr))
{
  //Save the JobId for later reference. 
  //Modify the job's property values.
  //Add files to the job.
  //Activate (resume) the job in the transfer queue.
}
```



<span data-ttu-id="ebed7-118">Чтобы получить последний интерфейс [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , вызовите метод **использованием метода ibackgroundcopyjob:: QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="ebed7-118">To get the latest [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface, call the **IBackgroundCopyJob::QueryInterface** method.</span></span> <span data-ttu-id="ebed7-119">В следующем примере показано, как получить интерфейс [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .</span><span class="sxs-lookup"><span data-stu-id="ebed7-119">The following example shows how to get the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface.</span></span>


```C++
  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJob5* pJob5 = NULL;

  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob5), (void**)&pJob5);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }
```



 

 




