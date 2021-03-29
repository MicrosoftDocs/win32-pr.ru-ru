---
title: Перечисление заданий в очереди на перемещение
description: Чтобы перечислить задания из очереди на перемещение, вызовите метод Ибаккграундкопиманажер Енумжобс. Метод возвращает указатель интерфейса Иенумбаккграундкопижобс, который используется для перечисления заданий в очереди.
ms.assetid: ebeb1670-dedd-4791-914e-d035d3c22c5a
keywords:
- БИТЫ задания передачи, перечисление
- перечисление заданий в БИТАХ очереди передачи
- БИТЫ очереди передачи, перечисление
- Перечисление битов
- Перечисление битов, заданий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9360043a9265248001dddb785edab3e8aac70abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328555"
---
# <a name="enumerating-jobs-in-the-transfer-queue"></a><span data-ttu-id="e0560-109">Перечисление заданий в очереди на перемещение</span><span class="sxs-lookup"><span data-stu-id="e0560-109">Enumerating Jobs in the Transfer Queue</span></span>

<span data-ttu-id="e0560-110">Чтобы перечислить задания из очереди на перемещение, вызовите метод [**ибаккграундкопиманажер:: енумжобс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="e0560-110">To enumerate jobs from the transfer queue, call the [**IBackgroundCopyManager::EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="e0560-111">Метод возвращает указатель интерфейса [**иенумбаккграундкопижобс**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) , который используется для перечисления заданий в очереди.</span><span class="sxs-lookup"><span data-stu-id="e0560-111">The method returns an [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) interface pointer that you use to enumerate the jobs in the queue.</span></span>

<span data-ttu-id="e0560-112">Чтобы получить задания пользователя, присвойте первому параметру метода [**енумжобс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) значение 0.</span><span class="sxs-lookup"><span data-stu-id="e0560-112">To retrieve the user's jobs, set the first parameter of the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method to 0.</span></span> <span data-ttu-id="e0560-113">Чтобы получить все задания в очереди, установите первый параметр метода **енумжобс** в значение \_ задания BG \_ Перечисление \_ всех \_ пользователей.</span><span class="sxs-lookup"><span data-stu-id="e0560-113">To retrieve all jobs in the queue, set the first parameter of the **EnumJobs** method to BG\_JOB\_ENUM\_ALL\_USERS.</span></span> <span data-ttu-id="e0560-114">Только пользователи с правами администратора могут получать все задания в очереди на перемещение.</span><span class="sxs-lookup"><span data-stu-id="e0560-114">Only users with administrator privileges can retrieve all jobs in the transfer queue.</span></span>

<span data-ttu-id="e0560-115">Обратите внимание, что перечисленный список является моментальным снимком заданий в очереди пересылки во время вызова метода [**енумжобс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="e0560-115">Note that the enumerated list is a snapshot of the jobs in the transfer queue at the time you call the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="e0560-116">Однако значения свойств этих заданий соответствуют текущим значениям задания.</span><span class="sxs-lookup"><span data-stu-id="e0560-116">However, the property values of those jobs reflect the current values of the job.</span></span>

<span data-ttu-id="e0560-117">Если вы хотите получить отдельные задания перемещения, вызовите метод [**ибаккграундкопиманажер:: жетжоб**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .</span><span class="sxs-lookup"><span data-stu-id="e0560-117">If you want to retrieve individual transfer jobs, call the [**IBackgroundCopyManager::GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) method.</span></span>

<span data-ttu-id="e0560-118">Сведения о перечислении файлов в задании см. [в разделе Перечисление файлов в задании](enumerating-files-in-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="e0560-118">To enumerate files in a job, see [Enumerating Files in a Job](enumerating-files-in-a-job.md).</span></span>

<span data-ttu-id="e0560-119">В следующем примере показано, как перечислить задания в очереди передачи.</span><span class="sxs-lookup"><span data-stu-id="e0560-119">The following example shows how to enumerate jobs in the transfer queue.</span></span> <span data-ttu-id="e0560-120">Переменная g \_ ксферманажер в примере является указателем интерфейса [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="e0560-120">The g\_XferManager variable in the example is an [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="e0560-121">Дополнительные сведения о создании указателя на интерфейс **ибаккграундкопиманажер** см. в разделе [Подключение к службе BITS](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="e0560-121">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


```C++
HRESULT hr = 0;
IEnumBackgroundCopyJobs* pJobs = NULL;
IBackgroundCopyJob* pJob = NULL;
ULONG cJobCount = 0;
ULONG idx = 0;

//This example enumerates all jobs in the transfer queue. This call fails if the 
//current user does not have administrator privileges. To enumerate jobs for only 
//the current user, replace BG_JOB_ENUM_ALL_USERS with 0.
hr = g_XferManager->EnumJobs(BG_JOB_ENUM_ALL_USERS, &pJobs);
if (SUCCEEDED(hr))
{
  //Get the count of jobs in the queue. 
  pJobs->GetCount(&cJobCount);

  //Enumerate the jobs in the queue.
  for (idx=0; idx<cJobCount; idx++)
  {
    hr = pJobs->Next(1, &pJob, NULL);
    if (S_OK == hr)
    {
      //Retrieve or set job properties.

      pJob->Release();
      pJob = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pJobs->Release();
  pJobs = NULL;
}
```



 

 




