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
ms.openlocfilehash: 293bf2449f12b43b018ed2f5f8c8e27d64f0f2a6e5f47dad95e4efdcc29a23b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010909"
---
# <a name="enumerating-jobs-in-the-transfer-queue"></a>Перечисление заданий в очереди на перемещение

Чтобы перечислить задания из очереди на перемещение, вызовите метод [**ибаккграундкопиманажер:: енумжобс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . Метод возвращает указатель интерфейса [**иенумбаккграундкопижобс**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) , который используется для перечисления заданий в очереди.

Чтобы получить задания пользователя, присвойте первому параметру метода [**енумжобс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) значение 0. Чтобы получить все задания в очереди, установите первый параметр метода **енумжобс** в значение \_ задания BG \_ Перечисление \_ всех \_ пользователей. Только пользователи с правами администратора могут получать все задания в очереди на перемещение.

Обратите внимание, что перечисленный список является моментальным снимком заданий в очереди пересылки во время вызова метода [**енумжобс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . Однако значения свойств этих заданий соответствуют текущим значениям задания.

Если вы хотите получить отдельные задания перемещения, вызовите метод [**ибаккграундкопиманажер:: жетжоб**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .

Сведения о перечислении файлов в задании см. [в разделе Перечисление файлов в задании](enumerating-files-in-a-job.md).

В следующем примере показано, как перечислить задания в очереди передачи. Переменная g \_ ксферманажер в примере является указателем интерфейса [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) . Дополнительные сведения о создании указателя на интерфейс **ибаккграундкопиманажер** см. в разделе [Подключение к службе BITS](connecting-to-the-bits-service.md).


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



 

 




