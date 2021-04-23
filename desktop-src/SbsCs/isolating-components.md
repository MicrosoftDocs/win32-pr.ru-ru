---
description: Хорошо созданные компоненты не повлиять среду хост-приложения и не вызывают контексты активации.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Изоляция компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e201375f50324209380a4ecef5fa762ae70e56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897106"
---
# <a name="isolating-components"></a><span data-ttu-id="2a45b-103">Изоляция компонентов</span><span class="sxs-lookup"><span data-stu-id="2a45b-103">Isolating Components</span></span>

<span data-ttu-id="2a45b-104">Хорошо созданные компоненты не повлиять среду хост-приложения и не вызывают контексты активации.</span><span class="sxs-lookup"><span data-stu-id="2a45b-104">Well-authored components do not perturb the environment of the hosting application, nor do they leak activation contexts.</span></span> <span data-ttu-id="2a45b-105">Хорошо созданные компоненты выполняют собственное управление контекстом, а не полагаться на среду ведущего приложения.</span><span class="sxs-lookup"><span data-stu-id="2a45b-105">Well-authored components perform their own context management rather than relying on the hosting application's environment.</span></span>

<span data-ttu-id="2a45b-106">Автор размещенного компонента находится в лучшем положении, чтобы точно знать, какие другие сборки требуются компоненту.</span><span class="sxs-lookup"><span data-stu-id="2a45b-106">The author of the hosted component is in the best position to know exactly which other assemblies the component requires.</span></span> <span data-ttu-id="2a45b-107">Полагаться на ведущее приложение, чтобы обеспечить правильную среду для размещенного компонента, — вероятный источник ошибок.</span><span class="sxs-lookup"><span data-stu-id="2a45b-107">Relying on the host application to provide the correct environment for your hosted component is a probable source of errors.</span></span> <span data-ttu-id="2a45b-108">Вместо этого создайте манифест для размещенного компонента, который указывает все его зависимости, а затем скомпилируйте с \_ \_ включенной поддержкой изоляции.</span><span class="sxs-lookup"><span data-stu-id="2a45b-108">Instead, create a manifest for your hosted component that specifies all its dependencies, and then compile using ISOLATION\_AWARE\_ENABLED.</span></span> <span data-ttu-id="2a45b-109">Это гарантирует, что внешние вызовы, выполняемые компонентом, будут изолированы и использовать правильные версии.</span><span class="sxs-lookup"><span data-stu-id="2a45b-109">This ensures that outside calls made by your component are isolated and use the correct versions.</span></span> <span data-ttu-id="2a45b-110">Так как контекст активации, используемый в режиме изоляции, используется \_ \_ для каждой библиотеки DLL, его можно использовать в нескольких библиотеках DLL, каждый из которых имеет собственный манифест, вызывающий зависимости.</span><span class="sxs-lookup"><span data-stu-id="2a45b-110">Because the activation context that ISOLATION\_AWARE\_ENABLED uses is per-DLL, it is safe to use in multiple DLLs, each with their own manifest calling out dependencies.</span></span>

<span data-ttu-id="2a45b-111">Если невозможно выполнить компиляцию с включенной поддержкой режима \_ изоляции \_ , используйте решение, аналогичное представленному при [использовании обратных вызовов из размещенных компонентов](using-callbacks-from-hosted-components.md).</span><span class="sxs-lookup"><span data-stu-id="2a45b-111">If it is not possible to compile with ISOLATION\_AWARE\_ENABLED, then use a solution like the one presented in [Using Callbacks From Hosted Components](using-callbacks-from-hosted-components.md).</span></span>

<span data-ttu-id="2a45b-112">Необходимо активировать собственный контекст активации во всех точках входа, которые может вызывать приложение размещения, чтобы убедиться, что размещенный компонент полностью работает с правильным контекстом активации.</span><span class="sxs-lookup"><span data-stu-id="2a45b-112">You should activate your own activation context in all the entry points that the hosting application can call to ensure that your hosted component runs entirely with the correct activation context.</span></span> <span data-ttu-id="2a45b-113">Для упрощения изменения всех EntryPoint можно использовать вспомогательный объект C++.</span><span class="sxs-lookup"><span data-stu-id="2a45b-113">You can use a C++ helper object to facilitate changing all the entrypoints.</span></span> <span data-ttu-id="2a45b-114">Например, можно использовать класс C++, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="2a45b-114">For example, you could use a C++ class such as the following:</span></span>


```C++
#include <windows.h>

class CActivationContext 
{
    HANDLE m_hActivationContext;

public:
    CActivationContext() : m_hActivationContext(INVALID_HANDLE_VALUE) 
    {
    }

    VOID Set(HANDLE hActCtx) 
    {
        if (hActCtx != INVALID_HANDLE_VALUE)
            AddRefActCtx(hActCtx);

        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
        m_hActivationContext = hActCtx;
    }

    ~CActivationContext() 
    {
        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
    }

    BOOL Activate(ULONG_PTR &ulpCookie) 
    {
        return ActivateActCtx(m_hActivationContext, &ulpCookie);
    }

    BOOL Deactivate(ULONG_PTR ulpCookie) 
    {
        return DeactivateActCtx(0, ulpCookie);
    }
};

class CActCtxActivator 
{
    CActivationContext &m_ActCtx;
    ULONG_PTR m_Cookie;
    bool m_fActivated;

public:
    CActCtxActivator(CActivationContext& src, bool fActivate = true) 
        : m_ActCtx(src), m_Cookie(0), m_fActivated(false) 
    {
        if (fActivate) {
            if (src.Activate(m_Cookie))
                m_fActivated = true;
        }
    }

    ~CActCtxActivator() 
    {
        if (m_fActivated) {
            m_ActCtx.Deactivate(m_Cookie);
            m_fActivated = false;
        }
    }
};

```



<span data-ttu-id="2a45b-115">Затем его можно использовать в компоненте, используя глобальную переменную для хранения контекста активации, который должен быть активирован в каждой точке входа.</span><span class="sxs-lookup"><span data-stu-id="2a45b-115">This can then be used in your component, using a global variable to store the activation context that should be activated on each entry point.</span></span> <span data-ttu-id="2a45b-116">Таким образом, компонент можно изолировать из приложения размещения.</span><span class="sxs-lookup"><span data-stu-id="2a45b-116">In this way, you can isolate your component from your hosting application.</span></span>


```C++
CActivationContext s_GlobalContext;

void MyExportedEntrypoint(void) 
{
    CActCtxActivator ScopedContext(s_GlobalContext);
    // Do whatever work here
    // Destructor automatically deactivates the context
}

void MyInitializerFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};
    hActCtx = CreateActCtx(&actctx);
    s_GlobalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
    // The static destructor for s_GlobalContext destroys the
    // activation context on component unload.
}
```



 

 



