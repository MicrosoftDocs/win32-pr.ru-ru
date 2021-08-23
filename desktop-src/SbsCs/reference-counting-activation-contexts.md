---
description: Контексты активации — это объекты, подсчитанные по ссылке. Приложение должно иметь ссылку на контекст активации, чтобы его можно было использовать.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Контексты активации подсчета ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f7806a452dc8b98f824069be0cd584c39f45ad9807a97a11f6f3d7c4929f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141937"
---
# <a name="reference-counting-activation-contexts"></a>Контексты активации подсчета ссылок

Контексты активации — это объекты, подсчитанные по ссылке. Приложение должно иметь ссылку на контекст активации, чтобы его можно было использовать. Функции API контекста активации, которые принимают контекст активации, могут выполнять собственный подсчет ссылок. Например, [**активатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) увеличивает и [**деактиватеакткткс**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) уменьшает число ссылок. Если приложение передает контекст активации без использования этих функций, приложение должно предоставить собственный метод подсчета ссылок.

Когда приложение вызывает [**креатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), возвращаемый маркер будет иметь счетчик ссылок, равный одному. После завершения работы приложения с контекстом активации необходимо освободить обработчик и уменьшить число ссылок, вызвав [**релеасеакткткс**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx). Не пытайтесь использовать [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**хеапфри**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)или другие функции управления памятью в обработчике контекста активации.

В следующем примере показан метод обработки подсчета ссылок в течение времени существования контекста активации. Функция Func создает контекст активации, который затем передается в целевой объект объекта, что увеличивает значение счетчика ссылок до 2. После этого функция Func освобождает ссылку на контекст активации и уменьшает значение счетчика ссылок обратно на 1. Целевой объект затем владеет собственной ссылкой при повторном вызове Сетакткткс или при уничтожении объекта.


```C++
#include <windows.h>

class CMyObject 
{
private:
    HANDLE m_hActCtx;
public:
    CMyObject() : m_hActCtx(INVALID_HANDLE_VALUE) { }
    ~CMyObject() 
    { 
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
            m_hActCtx = INVALID_HANDLE_VALUE;
        }
    }
    void SetActCtx(HANDLE hActCtx) 
    {
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
        }
        m_hActCtx = hActCtx;
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            AddRefActCtx(m_hActCtx);
        }
    }
    void DoWorkWithActCtx();
};

void Funct(CMyObject &Target) 
{
    HANDLE hActCtx;
    ACTCTX actctx = { sizeof(ACTCTX) };
    hActCtx = CreateActCtx(&actctx);  //create activation context  
    Target.SetActCtx(hActCtx);    //pass activation context to Target; 
    // actctx now has 1 more reference
    ReleaseActCtx(hActCtx);
}
```



 

 
