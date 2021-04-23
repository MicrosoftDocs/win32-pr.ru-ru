---
title: Опрос состояния задания
description: По умолчанию приложение должно опрашивать изменения в состоянии задания.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- БИТЫ заданий передачи, опрос
- опрос для битов состояния задания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df7fcde49d7359ff8cfa38326eba1e1e0bfeac5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887767"
---
# <a name="polling-for-the-status-of-the-job"></a><span data-ttu-id="7ef5f-105">Опрос состояния задания</span><span class="sxs-lookup"><span data-stu-id="7ef5f-105">Polling for the Status of the Job</span></span>

<span data-ttu-id="7ef5f-106">По умолчанию приложение должно опрашивать изменения в состоянии задания.</span><span class="sxs-lookup"><span data-stu-id="7ef5f-106">By default, an application must poll for changes in the status of a job.</span></span> <span data-ttu-id="7ef5f-107">Чтобы записать изменения в состоянии задания, вызовите метод [**использованием метода ibackgroundcopyjob:: with State**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) .</span><span class="sxs-lookup"><span data-stu-id="7ef5f-107">To capture changes in the job's state, call the [**IBackgroundCopyJob::GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) method.</span></span> <span data-ttu-id="7ef5f-108">Чтобы захватить изменения в количестве передаваемых байтов и файлов, вызовите метод [**использованием метода ibackgroundcopyjob:: Progress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) .</span><span class="sxs-lookup"><span data-stu-id="7ef5f-108">To capture changes in the number of bytes and files transferred, call the [**IBackgroundCopyJob::GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) method.</span></span> <span data-ttu-id="7ef5f-109">Чтобы получить сведения о ходе выполнения задания отправки и ответа, вызовите метод [**IBackgroundCopyJob2:: жетреплипрогресс**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) .</span><span class="sxs-lookup"><span data-stu-id="7ef5f-109">To retrieve progress information on the reply portion of an upload-reply job, call the [**IBackgroundCopyJob2::GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) method.</span></span> <span data-ttu-id="7ef5f-110">Пример, в котором используются сведения о ходе выполнения, см. [в разделе Определение хода выполнения задания](determining-the-progress-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="7ef5f-110">For an example that uses the progress information, see [Determining the Progress of a Job](determining-the-progress-of-a-job.md).</span></span>

<span data-ttu-id="7ef5f-111">Перечисление [**\_ \_ состояния задания BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) определяет состояния задания, а структура [**\_ \_ хода выполнения задания BG**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) содержит сведения о количестве переданных байтов и файлов.</span><span class="sxs-lookup"><span data-stu-id="7ef5f-111">The [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration defines the states of a job, and the [**BG\_JOB\_PROGRESS**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) structure contains information on the number of bytes and files transferred.</span></span>

<span data-ttu-id="7ef5f-112">Для использования опроса необходимо создать механизм для инициирования опроса.</span><span class="sxs-lookup"><span data-stu-id="7ef5f-112">To use polling, you need to create a mechanism to initiate polling.</span></span> <span data-ttu-id="7ef5f-113">Например, создайте таймер или используйте кнопку "Обновить" в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="7ef5f-113">For example, create a timer or use an "Update" button on the user interface.</span></span> <span data-ttu-id="7ef5f-114">Однако может быть проще зарегистрироваться для получения уведомлений о событиях и получать события при изменении состояния или хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7ef5f-114">However, it might be easier to register for event notification and receive events when the state or progress changes.</span></span> <span data-ttu-id="7ef5f-115">Дополнительные сведения об уведомлении о событии см. в разделе [Регистрация обратного вызова com](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="7ef5f-115">For information on event notification, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="7ef5f-116">В следующем примере для опроса состояния задания используется таймер.</span><span class="sxs-lookup"><span data-stu-id="7ef5f-116">The following example uses a timer to poll for the state of a job.</span></span> <span data-ttu-id="7ef5f-117">В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым.</span><span class="sxs-lookup"><span data-stu-id="7ef5f-117">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_JOB_STATE State;
HANDLE hTimer = NULL;
LARGE_INTEGER liDueTime;
//IBackgroundCopyError* pError = NULL;
//BG_JOB_PROGRESS Progress;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

liDueTime.QuadPart = -10000000;  //Poll every 1 second
hTimer = CreateWaitableTimer(NULL, FALSE, L"MyTimer");
SetWaitableTimer(hTimer, &liDueTime, 1000, NULL, NULL, 0);

do
{
  WaitForSingleObject(hTimer, INFINITE);

  //Use JobStates[State] to set the window text in a user interface.
  hr = pJob->GetState(&State);
  if (FAILED(hr))
  {
    //Handle error
  }

  if (BG_JOB_STATE_TRANSFERRED == State)
    //Call pJob->Complete(); to acknowledge that the transfer is complete
    //and make the file available to the client.
  else if (BG_JOB_STATE_ERROR == State || BG_JOB_STATE_TRANSIENT_ERROR == State)
    //Call pJob->GetError(&pError); to retrieve an IBackgroundCopyError interface 
    //pointer which you use to determine the cause of the error.
  else if (BG_JOB_STATE_TRANSFERRING == State)
    //Call pJob->GetProgress(&Progress); to determine the number of bytes 
    //and files transferred.
} while (BG_JOB_STATE_TRANSFERRED != State && 
         BG_JOB_STATE_ERROR != State &&
         BG_JOB_STATE_TRANSIENT_ERROR != State);
CancelWaitableTimer(hTimer);
CloseHandle(hTimer);
```



 

 




