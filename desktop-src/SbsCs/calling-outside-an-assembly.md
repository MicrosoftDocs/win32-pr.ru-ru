---
description: Вызов за пределами сборки
ms.assetid: 7a59f707-fb89-4899-891f-4cd556b62b26
title: Вызов за пределами сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed60536c3daa62957929dd1d3f1a850fd551ae9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650886"
---
# <a name="calling-outside-an-assembly"></a><span data-ttu-id="c059e-103">Вызов за пределами сборки</span><span class="sxs-lookup"><span data-stu-id="c059e-103">Calling Outside An Assembly</span></span>

<span data-ttu-id="c059e-104">Размещенные компоненты должны обеспечить активизацию правильного контекста активации при вызове за пределами компонента.</span><span class="sxs-lookup"><span data-stu-id="c059e-104">Hosted components should ensure that the correct activation context is active when calling outside the component.</span></span> <span data-ttu-id="c059e-105">Вызывает внешний код, который был найден путем вызова [**креатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) , а затем [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), должен вызываться с тем же контекстом, который использовался для его поиска.</span><span class="sxs-lookup"><span data-stu-id="c059e-105">Calls into outside code that was found by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) and then [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), should be called with the same context that was used to find it.</span></span> <span data-ttu-id="c059e-106">Вызывает код, обнаруженный за пределами контекстов активации, или вызовы обратно в приложение размещения должны вызываться с контекстом активации приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c059e-106">Calls into code that was found outside of activation contexts, or calls back into the hosting application should be called with the application default activation context.</span></span>

<span data-ttu-id="c059e-107">Компиляция с \_ \_ включенной поддержкой режима изоляции может быть полезной при вызове за пределами размещенных компонентов.</span><span class="sxs-lookup"><span data-stu-id="c059e-107">Compiling with ISOLATION\_AWARE\_ENABLED defined may be useful when calling outside of hosted components.</span></span> <span data-ttu-id="c059e-108">Однако это означает, что только вызовы API Windows будут изолированы от контекста активации компонента.</span><span class="sxs-lookup"><span data-stu-id="c059e-108">However this means that only calls to Windows APIs are isolated to the component's activation context.</span></span> <span data-ttu-id="c059e-109">Это достаточно для большинства случаев, поскольку вызовы функций сторонних производителей не имеют контекста, активированного перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="c059e-109">This is sufficient for most cases because calls to third-party functions do not have a context activated before being called.</span></span> <span data-ttu-id="c059e-110">Компиляция с \_ \_ включенной поддержкой режима изоляции не помогает, если компонент использует несколько контекстов активации с различными API-интерфейсами платформы.</span><span class="sxs-lookup"><span data-stu-id="c059e-110">Compiling with ISOLATION\_AWARE\_ENABLED defined does not help if your component uses several activation contexts with various platform APIs.</span></span>

<span data-ttu-id="c059e-111">Для реализации этого используйте активатор контекста активации, как в примере [изоляции компонентов](isolating-components.md).</span><span class="sxs-lookup"><span data-stu-id="c059e-111">To implement this, use an activation context activator like the example presented in [Isolating Components](isolating-components.md).</span></span> <span data-ttu-id="c059e-112">Здесь внешние. manifest — это набор зависимостей за пределами компонентов, с которыми был создан компонент. возможно, он содержит список компонентов, которые должны быть загружены и использованы во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="c059e-112">Here externals.manifest is the set of dependencies outside those the component was built with; perhaps it contains some extendable list of components that are to be loaded and used during runtime.</span></span> <span data-ttu-id="c059e-113">Интерналконтекст. manifest содержит набор зависимостей, которые компонент будет использовать в течение своего времени существования, который должен быть установлен во всех EntryPoint извне.</span><span class="sxs-lookup"><span data-stu-id="c059e-113">The internalcontext.manifest contains the set of dependencies that the component is sure to use during its lifetime, and which should be set in all entrypoints from the outside.</span></span> <span data-ttu-id="c059e-114">Обратите внимание, что этот внутренний контекст активируется во всех EntryPoint, а активатор контекста используется с областями C++, поэтому правильный контекст задается при вызове для различных внешних кодов, используемых этим компонентом.</span><span class="sxs-lookup"><span data-stu-id="c059e-114">Notice that this internal context is activated in all entrypoints, while the context activator is used with C++ scoping so that the proper context is set when calling out to the various outside code that this component uses.</span></span>

``` syntax
CActivationContext s_InternalContext;
CActivationContext s_OutboundContext;
CActivationContext s_ExternalContext;

void MyInitializeFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};

    s_OutboundContext.Set(NULL);

    actctx.lpSource = TEXT("internalcontext.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_InternalActCtx.Set(hActCtx);
    ReleaseActCtx(hActCtx);

    actctx.lpSource = TEXT("externals.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_ExternalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
}

void foo() 
{
    // Some code that makes a few calls
    {
        CActCtxActivator CallUnknown(s_OutboundContext);
        pfnUnknownImplementor(...);
    }
    {
        CActCtxActivator CallDependency(s_ExternalContext);
        KnownExternalDependencyPtr->Call();
    }
}

void WINAPI MyEntrypoint() 
{
    CActCtxActivator ContextFirewall(s_InternalContext);
    // Do some work here
    foo();
    // Some more work here
}
```

 

 
