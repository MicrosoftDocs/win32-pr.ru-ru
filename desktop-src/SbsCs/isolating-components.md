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
# <a name="isolating-components"></a>Изоляция компонентов

Хорошо созданные компоненты не повлиять среду хост-приложения и не вызывают контексты активации. Хорошо созданные компоненты выполняют собственное управление контекстом, а не полагаться на среду ведущего приложения.

Автор размещенного компонента находится в лучшем положении, чтобы точно знать, какие другие сборки требуются компоненту. Полагаться на ведущее приложение, чтобы обеспечить правильную среду для размещенного компонента, — вероятный источник ошибок. Вместо этого создайте манифест для размещенного компонента, который указывает все его зависимости, а затем скомпилируйте с \_ \_ включенной поддержкой изоляции. Это гарантирует, что внешние вызовы, выполняемые компонентом, будут изолированы и использовать правильные версии. Так как контекст активации, используемый в режиме изоляции, используется \_ \_ для каждой библиотеки DLL, его можно использовать в нескольких библиотеках DLL, каждый из которых имеет собственный манифест, вызывающий зависимости.

Если невозможно выполнить компиляцию с включенной поддержкой режима \_ изоляции \_ , используйте решение, аналогичное представленному при [использовании обратных вызовов из размещенных компонентов](using-callbacks-from-hosted-components.md).

Необходимо активировать собственный контекст активации во всех точках входа, которые может вызывать приложение размещения, чтобы убедиться, что размещенный компонент полностью работает с правильным контекстом активации. Для упрощения изменения всех EntryPoint можно использовать вспомогательный объект C++. Например, можно использовать класс C++, как показано ниже:


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



Затем его можно использовать в компоненте, используя глобальную переменную для хранения контекста активации, который должен быть активирован в каждой точке входа. Таким образом, компонент можно изолировать из приложения размещения.


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



 

 



