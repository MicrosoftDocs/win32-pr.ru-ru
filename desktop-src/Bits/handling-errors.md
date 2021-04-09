---
title: Обработка ошибок (бит)
description: Существует два типа ошибок, которые могут быть обработаны в приложении.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- Обработка битов ошибок
- БИТЫ заданий передачи, ошибки
- БИТЫ ошибок
- БИТЫ ошибок, обработка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070939"
---
# <a name="handling-errors-bits"></a><span data-ttu-id="3bad7-107">Обработка ошибок (бит)</span><span class="sxs-lookup"><span data-stu-id="3bad7-107">Handling Errors (BITS)</span></span>

<span data-ttu-id="3bad7-108">Существует два типа ошибок, которые могут быть обработаны в приложении.</span><span class="sxs-lookup"><span data-stu-id="3bad7-108">There are two types of errors to handle in your application.</span></span> <span data-ttu-id="3bad7-109">Первая ошибка является вызовом метода со сбоем.</span><span class="sxs-lookup"><span data-stu-id="3bad7-109">The first error is a failed method call.</span></span> <span data-ttu-id="3bad7-110">Каждый метод возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3bad7-110">Each method returns an **HRESULT** value.</span></span> <span data-ttu-id="3bad7-111">На странице ссылки для каждого метода указаны возвращаемые значения, которые, скорее всего, будут создаваться.</span><span class="sxs-lookup"><span data-stu-id="3bad7-111">The reference page for each method identifies the return values that it is most likely to generate.</span></span> <span data-ttu-id="3bad7-112">Дополнительные возвращаемые значения см. в разделе [службы, возвращающие значения BITS](bits-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3bad7-112">For additional return values, see [BITS Return Values](bits-return-values.md).</span></span> <span data-ttu-id="3bad7-113">Чтобы получить текст сообщения, связанный с возвращаемым значением, вызовите метод [**ибаккграундкопиманажер:: жетеррордескриптион**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .</span><span class="sxs-lookup"><span data-stu-id="3bad7-113">To get the message text associated with the return value, call the [**IBackgroundCopyManager::GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) method.</span></span>

<span data-ttu-id="3bad7-114">Вторым типом ошибки для обработчика является задание, [состояние](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) которого переходит к [ \_ \_ \_ ошибке состояния задания BG](/windows/desktop/api/Bits/ne-bits-bg_job_state) или **\_ \_ \_ Промежуточная \_ Ошибка состояния задания BG**.</span><span class="sxs-lookup"><span data-stu-id="3bad7-114">The second type of error to handle is a job whose [state](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) transitions to [BG\_JOB\_STATE\_ERROR](/windows/desktop/api/Bits/ne-bits-bg_job_state) or **BG\_JOB\_STATE\_TRANSIENT\_ERROR**.</span></span> <span data-ttu-id="3bad7-115">Для получения сведений, относящихся к этим типам ошибок, вызовите метод [**использованием метода ibackgroundcopyjob:: OnError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) задания.</span><span class="sxs-lookup"><span data-stu-id="3bad7-115">To retrieve information related to these types of errors, call the job's [**IBackgroundCopyJob::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) method.</span></span> <span data-ttu-id="3bad7-116">Метод возвращает указатель интерфейса [**ибаккграундкоперрор**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) , который содержит сведения, используемые для определения причины ошибки.</span><span class="sxs-lookup"><span data-stu-id="3bad7-116">The method returns an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer that contains information you use to determine the cause of the error.</span></span> <span data-ttu-id="3bad7-117">Вы также можете получить уведомление об ошибке, зарегистрировав его для получения уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="3bad7-117">You can also receive error notification by registering to receive event notification.</span></span> <span data-ttu-id="3bad7-118">Дополнительные сведения см. [в разделе Регистрация обратного вызова com](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="3bad7-118">For details, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="3bad7-119">Служба BITS считает, что каждое задание является атомарным.</span><span class="sxs-lookup"><span data-stu-id="3bad7-119">BITS considers each job to be atomic.</span></span> <span data-ttu-id="3bad7-120">Если один из файлов в задании создает ошибку, задание остается в состоянии ошибки до тех пор, пока ошибка не будет устранена.</span><span class="sxs-lookup"><span data-stu-id="3bad7-120">If one of the files in the job generates an error, the job remains in an error state until the error is resolved.</span></span> <span data-ttu-id="3bad7-121">Поэтому нельзя удалить файл, который вызывает ошибку из задания.</span><span class="sxs-lookup"><span data-stu-id="3bad7-121">Thus, you cannot delete the file that is causing the error from the job.</span></span> <span data-ttu-id="3bad7-122">Однако если ошибка вызвана недоступностью сервера или недопустимым удаленным файлом, можно вызвать метод [**IBackgroundCopyJob3:: реплацеремотепрефикс**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) или [**IBackgroundCopyFile2:: сетремотенаме**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) для задания нового имени сервера или файла.</span><span class="sxs-lookup"><span data-stu-id="3bad7-122">However, if the error is caused by the server not being available or an invalid remote file, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) or [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method to identify a new server or file name.</span></span>

<span data-ttu-id="3bad7-123">Определив причину ошибки, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="3bad7-123">After determining the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="3bad7-124">Отмените задание, вызвав метод [**использованием метода ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="3bad7-124">Cancel the job by calling the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>
-   <span data-ttu-id="3bad7-125">Для задания загрузки вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) , чтобы сохранить переданные файлы, которые были успешно переданы до возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="3bad7-125">For a download job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method to save the files that transferred successfully before the error occurred.</span></span>
-   <span data-ttu-id="3bad7-126">Исправьте ошибку и вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) , чтобы завершить задание.</span><span class="sxs-lookup"><span data-stu-id="3bad7-126">Fix the error and call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method to finish the job.</span></span>

<span data-ttu-id="3bad7-127">Для задания отправки и ответа проверьте значение элемента **битестотал** структуры [**\_ \_ \_ хода выполнения ответов задания BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) , чтобы определить, произошла ли ошибка в части задания, отправляемой или откликом.</span><span class="sxs-lookup"><span data-stu-id="3bad7-127">For an upload-reply job, check the value of the **BytesTotal** member of the [**BG\_JOB\_REPLY\_PROGRESS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) structure to determine if the error occurred on the upload or reply portion of the job.</span></span> <span data-ttu-id="3bad7-128">Произошла ошибка при отправке, если значение имеет \_ \_ неизвестный размер BG.</span><span class="sxs-lookup"><span data-stu-id="3bad7-128">The error occurred on the upload if the value is BG\_SIZE\_UNKNOWN.</span></span>

<span data-ttu-id="3bad7-129">В следующем примере показано, как получить указатель интерфейса [**ибаккграундкоперрор**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) .</span><span class="sxs-lookup"><span data-stu-id="3bad7-129">The following example shows how to retrieve an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer.</span></span> <span data-ttu-id="3bad7-130">В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3bad7-130">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




