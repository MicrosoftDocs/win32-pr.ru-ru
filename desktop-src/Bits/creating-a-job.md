---
title: Создание задания
description: Чтобы создать задание перемещения, вызовите метод Ибаккграундкопиманажер CreateJob.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- БИТЫ задания передачи
- БИТЫ заданий передачи, создание
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0241d855d60178e87f28820f14b39e497f200fe5770933f293257e62b2d1b601
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528893"
---
# <a name="creating-a-job"></a>Создание задания

Чтобы создать задание перемещения, вызовите метод [**ибаккграундкопиманажер:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) . После создания задания службы BITS [добавляют файлы в задание](adding-files-to-a-job.md) и [изменяют свойства задания](setting-and-retrieving-the-properties-of-a-job.md) в соответствии с вашими приложениями. Чтобы активировать задание в очереди, вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .

Метод [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) создает идентификатор GUID, который однозначно идентифицирует задание. Идентификатор GUID используется для [получения задания из очереди на перемещение](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob). Отображаемое имя, которое вы задаете при создании задания, не является уникальным; более одного задания могут использовать одно и то же имя.

BITS ограничивает количество заданий в очереди до 300 заданий и число заданий, которые пользователь может создать в 60. Эти ограничения не применяются к администраторам и службам. Сведения об изменении этих ограничений по умолчанию см. в разделе [групповые политики](group-policies.md).

В следующем примере показано, как создать задание загрузки. В примере предполагается, что \_ переменная g пбкм является допустимым указателем интерфейса [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) . Дополнительные сведения о создании указателя на интерфейс **ибаккграундкопиманажер** см. в разделе [Подключение к службе BITS](connecting-to-the-bits-service.md).


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



Чтобы получить последний интерфейс [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , вызовите метод **использованием метода ibackgroundcopyjob:: QueryInterface** . В следующем примере показано, как получить интерфейс [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .


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



 

 




