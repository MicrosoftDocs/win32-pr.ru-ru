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
# <a name="polling-for-the-status-of-the-job"></a>Опрос состояния задания

По умолчанию приложение должно опрашивать изменения в состоянии задания. Чтобы записать изменения в состоянии задания, вызовите метод [**использованием метода ibackgroundcopyjob:: with State**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) . Чтобы захватить изменения в количестве передаваемых байтов и файлов, вызовите метод [**использованием метода ibackgroundcopyjob:: Progress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) . Чтобы получить сведения о ходе выполнения задания отправки и ответа, вызовите метод [**IBackgroundCopyJob2:: жетреплипрогресс**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) . Пример, в котором используются сведения о ходе выполнения, см. [в разделе Определение хода выполнения задания](determining-the-progress-of-a-job.md).

Перечисление [**\_ \_ состояния задания BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) определяет состояния задания, а структура [**\_ \_ хода выполнения задания BG**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) содержит сведения о количестве переданных байтов и файлов.

Для использования опроса необходимо создать механизм для инициирования опроса. Например, создайте таймер или используйте кнопку "Обновить" в пользовательском интерфейсе. Однако может быть проще зарегистрироваться для получения уведомлений о событиях и получать события при изменении состояния или хода выполнения. Дополнительные сведения об уведомлении о событии см. в разделе [Регистрация обратного вызова com](registering-a-com-callback.md).

В следующем примере для опроса состояния задания используется таймер. В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым.


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



 

 




