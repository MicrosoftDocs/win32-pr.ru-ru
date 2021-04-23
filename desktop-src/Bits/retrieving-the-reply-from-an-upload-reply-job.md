---
title: Получение ответа из задания Upload-Reply
description: Чтобы передать данные в серверное приложение и вернуть их клиенту, укажите задание в виде задания BG \_ \_ \_ Отправка \_ ответа.
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 582a37a31c13c5cc3e0b44c51a767cfbe465c64c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986217"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a><span data-ttu-id="d9a03-103">Получение ответа из задания Upload-Reply</span><span class="sxs-lookup"><span data-stu-id="d9a03-103">Retrieving the Reply from an Upload-Reply Job</span></span>

<span data-ttu-id="d9a03-104">Задание Upload-Reply BITS, помимо отправки файла на сервер, также просматривает URL-адрес ответа, отправленный в ответ на сервер, а затем автоматически выполняет поиск по URL-адресу ответа и скачивает ответ из него.</span><span class="sxs-lookup"><span data-stu-id="d9a03-104">A BITS Upload-Reply job, in addition to uploading a file to a server, will also examine a reply URL sent as part of the server reply and then automatically follow the reply URL and download a response from it.</span></span> <span data-ttu-id="d9a03-105">Дополнительные сведения о значении заголовка BITS-Reply-URL см. в документации по [ACK для фрагмента](/windows/desktop/Bits/ack-for-fragment) .</span><span class="sxs-lookup"><span data-stu-id="d9a03-105">See the [Ack for Fragment](/windows/desktop/Bits/ack-for-fragment) documentation for more details about the BITS-Reply-URL header value.</span></span>

<span data-ttu-id="d9a03-106">Задайте для параметра Тип задания значение \_ " \_ \_ отправка ответа", \_ чтобы создать задание типа Upload-Reply.</span><span class="sxs-lookup"><span data-stu-id="d9a03-106">Set the job type as BG\_JOB\_TYPE\_UPLOAD\_REPLY to create an Upload-Reply type job.</span></span> <span data-ttu-id="d9a03-107">Данные ответа доступны клиенту после того, как задание перейдет в \_ состояние задания BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d9a03-107">The reply data is available to the client after the job enters the BG\_JOB\_STATE\_TRANSFERRED state.</span></span> <span data-ttu-id="d9a03-108">Чтобы получить ответ, вызовите один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="d9a03-108">To retrieve the reply, call one of the following methods:</span></span>

-   [<span data-ttu-id="d9a03-109">**IBackgroundCopyJob2:: Жетреплидата**</span><span class="sxs-lookup"><span data-stu-id="d9a03-109">**IBackgroundCopyJob2::GetReplyData**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    <span data-ttu-id="d9a03-110">Предоставляет копию данных ответа в памяти.</span><span class="sxs-lookup"><span data-stu-id="d9a03-110">Provides an in-memory copy of the reply data.</span></span> <span data-ttu-id="d9a03-111">Используйте этот метод для чтения данных ответа до или после вызова метода [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="d9a03-111">Use this method to read the reply data before or after calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="d9a03-112">Если данные ответа превышают 1 МБ, приложение должно вызвать метод [**IBackgroundCopyJob2:: жетреплифиленаме**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) , чтобы получить имя файла ответов и напрямую прочитать его содержимое.</span><span class="sxs-lookup"><span data-stu-id="d9a03-112">If the reply data exceeds 1 MB, the application must call the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method to retrieve the name of the reply file and read its contents directly.</span></span>

-   [<span data-ttu-id="d9a03-113">**IBackgroundCopyJob2:: Жетреплифиленаме**</span><span class="sxs-lookup"><span data-stu-id="d9a03-113">**IBackgroundCopyJob2::GetReplyFileName**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    <span data-ttu-id="d9a03-114">Предоставляет имя файла, содержащего ответ.</span><span class="sxs-lookup"><span data-stu-id="d9a03-114">Provides the name of the file that contains the reply.</span></span> <span data-ttu-id="d9a03-115">Перед открытием и чтением файла ответов необходимо вызвать метод **использованием метода ibackgroundcopyjob:: Complete** ; файл ответов недоступен для клиента, пока не будет вызван **полный** метод.</span><span class="sxs-lookup"><span data-stu-id="d9a03-115">You must call the **IBackgroundCopyJob::Complete** method before opening and reading the reply file; the reply file is not available to the client until you call the **Complete** method.</span></span>

<span data-ttu-id="d9a03-116">Вызывайте эти методы в методе [**ибаккграундкопикаллбакк:: жобтрансферред**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) только в том случае, если ответ небольшой и может быть обработан быстро, чтобы не блокировать поток обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d9a03-116">Call these methods in your [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) method only if the reply is small and can be processed quickly so as to not block the callback thread.</span></span> <span data-ttu-id="d9a03-117">Если вместо обратного вызова используется [**уведомление командной строки**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) , передайте идентификатор задания в исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="d9a03-117">If you use [**command line notification**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) instead of the callback, pass the job identifier to the executable file.</span></span> <span data-ttu-id="d9a03-118">Исполняемый файл использует идентификатор задания для вызова **полного** метода, чтобы сделать ответный файл доступным.</span><span class="sxs-lookup"><span data-stu-id="d9a03-118">The executable file uses the job identifier to call the **Complete** method to make the reply file available.</span></span>

<span data-ttu-id="d9a03-119">В следующих примерах показано, как использовать каждый метод для получения данных ответа.</span><span class="sxs-lookup"><span data-stu-id="d9a03-119">The following examples show how to use each method to retrieve the reply data.</span></span>

-   [<span data-ttu-id="d9a03-120">Использование Жетреплидата</span><span class="sxs-lookup"><span data-stu-id="d9a03-120">Using GetReplyData</span></span>](#using-getreplydata)
-   [<span data-ttu-id="d9a03-121">Использование Жетреплифиленаме</span><span class="sxs-lookup"><span data-stu-id="d9a03-121">Using GetReplyFileName</span></span>](#using-getreplyfilename)

## <a name="using-getreplydata"></a><span data-ttu-id="d9a03-122">Использование Жетреплидата</span><span class="sxs-lookup"><span data-stu-id="d9a03-122">Using GetReplyData</span></span>

<span data-ttu-id="d9a03-123">В следующем примере показано, как получить данные ответа с помощью метода [**IBackgroundCopyJob2:: жетреплидата**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) .</span><span class="sxs-lookup"><span data-stu-id="d9a03-123">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) method.</span></span> <span data-ttu-id="d9a03-124">В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым, тип задания — upload-Reply, а состояние задания — «передача \_ состояния задания BG» \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d9a03-124">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of the job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
BYTE* pReply = NULL;
UINT64 ReplySize;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyData method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyData(&pReply, &ReplySize);
    if (S_OK == hr))
    {
        if (pReply)
        {
            //Do something with the data.
            CoTaskMemFree(pReply);
        }
        else
        {
            //The server application did not return a reply.
        }
    }
    else if (BG_E_TOO_LARGE == hr)
    {
        //The reply exceeds 1 MB. To retrieve the reply, get the reply file name,
        //complete the job, open the reply file, and read the reply.
    }
    else
    {
        //Handle the error
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



## <a name="using-getreplyfilename"></a><span data-ttu-id="d9a03-125">Использование Жетреплифиленаме</span><span class="sxs-lookup"><span data-stu-id="d9a03-125">Using GetReplyFileName</span></span>

<span data-ttu-id="d9a03-126">В следующем примере показано, как получить данные ответа с помощью метода [**IBackgroundCopyJob2:: жетреплифиленаме**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) .</span><span class="sxs-lookup"><span data-stu-id="d9a03-126">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method.</span></span> <span data-ttu-id="d9a03-127">В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым, тип задания — "Отправить-ответить", а состояние задания — " \_ \_ передано состояние задания BG" \_ .</span><span class="sxs-lookup"><span data-stu-id="d9a03-127">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR* pszFileName = NULL;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyFileName method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyFileName(&pszFileName);
    if (SUCCEEDED(hr))
    {
        //Calling the Complete method removes the job from the queue, 
        //so make sure you maintain an interface pointer to this job 
        //or retrieve any job related information that you require 
        //when processing the reply.
        hr = pJob->Complete();

        //Open, read the file, and do something with the data.
        CoTaskMemFree(pszFileName);
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



 

 




