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
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>Получение ответа из задания Upload-Reply

Задание Upload-Reply BITS, помимо отправки файла на сервер, также просматривает URL-адрес ответа, отправленный в ответ на сервер, а затем автоматически выполняет поиск по URL-адресу ответа и скачивает ответ из него. Дополнительные сведения о значении заголовка BITS-Reply-URL см. в документации по [ACK для фрагмента](/windows/desktop/Bits/ack-for-fragment) .

Задайте для параметра Тип задания значение \_ " \_ \_ отправка ответа", \_ чтобы создать задание типа Upload-Reply. Данные ответа доступны клиенту после того, как задание перейдет в \_ состояние задания BG \_ \_ . Чтобы получить ответ, вызовите один из следующих методов:

-   [**IBackgroundCopyJob2:: Жетреплидата**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    Предоставляет копию данных ответа в памяти. Используйте этот метод для чтения данных ответа до или после вызова метода [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Если данные ответа превышают 1 МБ, приложение должно вызвать метод [**IBackgroundCopyJob2:: жетреплифиленаме**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) , чтобы получить имя файла ответов и напрямую прочитать его содержимое.

-   [**IBackgroundCopyJob2:: Жетреплифиленаме**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    Предоставляет имя файла, содержащего ответ. Перед открытием и чтением файла ответов необходимо вызвать метод **использованием метода ibackgroundcopyjob:: Complete** ; файл ответов недоступен для клиента, пока не будет вызван **полный** метод.

Вызывайте эти методы в методе [**ибаккграундкопикаллбакк:: жобтрансферред**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) только в том случае, если ответ небольшой и может быть обработан быстро, чтобы не блокировать поток обратного вызова. Если вместо обратного вызова используется [**уведомление командной строки**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) , передайте идентификатор задания в исполняемый файл. Исполняемый файл использует идентификатор задания для вызова **полного** метода, чтобы сделать ответный файл доступным.

В следующих примерах показано, как использовать каждый метод для получения данных ответа.

-   [Использование Жетреплидата](#using-getreplydata)
-   [Использование Жетреплифиленаме](#using-getreplyfilename)

## <a name="using-getreplydata"></a>Использование Жетреплидата

В следующем примере показано, как получить данные ответа с помощью метода [**IBackgroundCopyJob2:: жетреплидата**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) . В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым, тип задания — upload-Reply, а состояние задания — «передача \_ состояния задания BG» \_ \_ .


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



## <a name="using-getreplyfilename"></a>Использование Жетреплифиленаме

В следующем примере показано, как получить данные ответа с помощью метода [**IBackgroundCopyJob2:: жетреплифиленаме**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) . В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым, тип задания — "Отправить-ответить", а состояние задания — " \_ \_ передано состояние задания BG" \_ .


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



 

 




