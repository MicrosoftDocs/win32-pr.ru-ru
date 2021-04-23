---
description: Контексты активации — это объекты, подсчитанные по ссылке. Приложение должно иметь ссылку на контекст активации, чтобы его можно было использовать.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Контексты активации подсчета ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff00afa0dd3a347e14ff9723c06d54af4520ce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647628"
---
# <a name="reference-counting-activation-contexts"></a><span data-ttu-id="f4939-104">Контексты активации подсчета ссылок</span><span class="sxs-lookup"><span data-stu-id="f4939-104">Reference Counting Activation Contexts</span></span>

<span data-ttu-id="f4939-105">Контексты активации — это объекты, подсчитанные по ссылке.</span><span class="sxs-lookup"><span data-stu-id="f4939-105">Activation contexts are reference-counted objects.</span></span> <span data-ttu-id="f4939-106">Приложение должно иметь ссылку на контекст активации, чтобы его можно было использовать.</span><span class="sxs-lookup"><span data-stu-id="f4939-106">Your application must have a reference on an activation context in order to use it.</span></span> <span data-ttu-id="f4939-107">Функции API контекста активации, которые принимают контекст активации, могут выполнять собственный подсчет ссылок.</span><span class="sxs-lookup"><span data-stu-id="f4939-107">The functions of the Activation Context API that take an activation context can perform their own reference counting.</span></span> <span data-ttu-id="f4939-108">Например, [**активатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) увеличивает и [**деактиватеакткткс**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) уменьшает число ссылок.</span><span class="sxs-lookup"><span data-stu-id="f4939-108">For example, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) increases and [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) decreases the reference count.</span></span> <span data-ttu-id="f4939-109">Если приложение передает контекст активации без использования этих функций, приложение должно предоставить собственный метод подсчета ссылок.</span><span class="sxs-lookup"><span data-stu-id="f4939-109">If however your application passes an activation context without using these functions, the application should provide its own method of reference counting.</span></span>

<span data-ttu-id="f4939-110">Когда приложение вызывает [**креатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), возвращаемый маркер будет иметь счетчик ссылок, равный одному.</span><span class="sxs-lookup"><span data-stu-id="f4939-110">When an application calls [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), the handle returned will have a reference count of one.</span></span> <span data-ttu-id="f4939-111">После завершения работы приложения с контекстом активации необходимо освободить обработчик и уменьшить число ссылок, вызвав [**релеасеакткткс**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span><span class="sxs-lookup"><span data-stu-id="f4939-111">After the application finishes with the activation context, the handle should be released and the reference count decreased by calling [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span></span> <span data-ttu-id="f4939-112">Не пытайтесь использовать [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**хеапфри**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)или другие функции управления памятью в обработчике контекста активации.</span><span class="sxs-lookup"><span data-stu-id="f4939-112">Do not attempt to use [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree), or any other memory-management functions on the activation context handle.</span></span>

<span data-ttu-id="f4939-113">В следующем примере показан метод обработки подсчета ссылок в течение времени существования контекста активации.</span><span class="sxs-lookup"><span data-stu-id="f4939-113">The following example shows a method for handling reference counting over the lifetime of an activation context.</span></span> <span data-ttu-id="f4939-114">Функция Func создает контекст активации, который затем передается в целевой объект объекта, что увеличивает значение счетчика ссылок до 2.</span><span class="sxs-lookup"><span data-stu-id="f4939-114">The function Funct creates an activation context, which it then passes to the object Target, which increments the reference count to 2.</span></span> <span data-ttu-id="f4939-115">После этого функция Func освобождает ссылку на контекст активации и уменьшает значение счетчика ссылок обратно на 1.</span><span class="sxs-lookup"><span data-stu-id="f4939-115">Funct then releases its reference on the activation context and decreases the reference count back to 1.</span></span> <span data-ttu-id="f4939-116">Целевой объект затем владеет собственной ссылкой при повторном вызове Сетакткткс или при уничтожении объекта.</span><span class="sxs-lookup"><span data-stu-id="f4939-116">Target then owns releasing its own reference when SetActCtx is called again or when the object is destroyed.</span></span>


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



 

 
