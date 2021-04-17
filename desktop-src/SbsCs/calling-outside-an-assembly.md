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
# <a name="calling-outside-an-assembly"></a>Вызов за пределами сборки

Размещенные компоненты должны обеспечить активизацию правильного контекста активации при вызове за пределами компонента. Вызывает внешний код, который был найден путем вызова [**креатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) , а затем [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), должен вызываться с тем же контекстом, который использовался для его поиска. Вызывает код, обнаруженный за пределами контекстов активации, или вызовы обратно в приложение размещения должны вызываться с контекстом активации приложения по умолчанию.

Компиляция с \_ \_ включенной поддержкой режима изоляции может быть полезной при вызове за пределами размещенных компонентов. Однако это означает, что только вызовы API Windows будут изолированы от контекста активации компонента. Это достаточно для большинства случаев, поскольку вызовы функций сторонних производителей не имеют контекста, активированного перед вызовом. Компиляция с \_ \_ включенной поддержкой режима изоляции не помогает, если компонент использует несколько контекстов активации с различными API-интерфейсами платформы.

Для реализации этого используйте активатор контекста активации, как в примере [изоляции компонентов](isolating-components.md). Здесь внешние. manifest — это набор зависимостей за пределами компонентов, с которыми был создан компонент. возможно, он содержит список компонентов, которые должны быть загружены и использованы во время выполнения. Интерналконтекст. manifest содержит набор зависимостей, которые компонент будет использовать в течение своего времени существования, который должен быть установлен во всех EntryPoint извне. Обратите внимание, что этот внутренний контекст активируется во всех EntryPoint, а активатор контекста используется с областями C++, поэтому правильный контекст задается при вызове для различных внешних кодов, используемых этим компонентом.

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

 

 
