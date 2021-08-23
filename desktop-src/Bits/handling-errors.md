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
ms.openlocfilehash: d1b0f389b6f0bdeefdfd5868b444384af26027b9b688a8fb83ba89ea370b9360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528814"
---
# <a name="handling-errors-bits"></a>Обработка ошибок (бит)

Существует два типа ошибок, которые могут быть обработаны в приложении. Первая ошибка является вызовом метода со сбоем. Каждый метод возвращает значение **HRESULT** . На странице ссылки для каждого метода указаны возвращаемые значения, которые, скорее всего, будут создаваться. Дополнительные возвращаемые значения см. в разделе [службы, возвращающие значения BITS](bits-return-values.md). Чтобы получить текст сообщения, связанный с возвращаемым значением, вызовите метод [**ибаккграундкопиманажер:: жетеррордескриптион**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .

Вторым типом ошибки для обработчика является задание, [состояние](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) которого переходит к [ \_ \_ \_ ошибке состояния задания BG](/windows/desktop/api/Bits/ne-bits-bg_job_state) или **\_ \_ \_ Промежуточная \_ Ошибка состояния задания BG**. Для получения сведений, относящихся к этим типам ошибок, вызовите метод [**использованием метода ibackgroundcopyjob:: OnError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) задания. Метод возвращает указатель интерфейса [**ибаккграундкоперрор**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) , который содержит сведения, используемые для определения причины ошибки. Вы также можете получить уведомление об ошибке, зарегистрировав его для получения уведомления о событии. Дополнительные сведения см. [в разделе Регистрация обратного вызова com](registering-a-com-callback.md).

Служба BITS считает, что каждое задание является атомарным. Если один из файлов в задании создает ошибку, задание остается в состоянии ошибки до тех пор, пока ошибка не будет устранена. Поэтому нельзя удалить файл, который вызывает ошибку из задания. Однако если ошибка вызвана недоступностью сервера или недопустимым удаленным файлом, можно вызвать метод [**IBackgroundCopyJob3:: реплацеремотепрефикс**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) или [**IBackgroundCopyFile2:: сетремотенаме**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) для задания нового имени сервера или файла.

Определив причину ошибки, выполните одно из следующих действий.

-   Отмените задание, вызвав метод [**использованием метода ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .
-   Для задания загрузки вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) , чтобы сохранить переданные файлы, которые были успешно переданы до возникновения ошибки.
-   Исправьте ошибку и вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) , чтобы завершить задание.

Для задания отправки и ответа проверьте значение элемента **битестотал** структуры [**\_ \_ \_ хода выполнения ответов задания BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) , чтобы определить, произошла ли ошибка в части задания, отправляемой или откликом. Произошла ошибка при отправке, если значение имеет \_ \_ неизвестный размер BG.

В следующем примере показано, как получить указатель интерфейса [**ибаккграундкоперрор**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) . В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым.


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



 

 




