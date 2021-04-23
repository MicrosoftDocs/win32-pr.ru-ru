---
description: Функции обратного вызова из размещенных компонентов делают возможным размещение. Однако возможно, что размещенный компонент активировал другой контекст активации, используемый для доступа к подключаемым модулям или собственным компонентам.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Использование обратных вызовов из размещенных компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef302601985bc7e56a296bc8f494e48e18d785e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144497"
---
# <a name="using-callbacks-from-hosted-components"></a><span data-ttu-id="b82f4-104">Использование обратных вызовов из размещенных компонентов</span><span class="sxs-lookup"><span data-stu-id="b82f4-104">Using Callbacks From Hosted Components</span></span>

<span data-ttu-id="b82f4-105">Функции обратного вызова из размещенных компонентов делают возможным размещение.</span><span class="sxs-lookup"><span data-stu-id="b82f4-105">Callbacks from hosted components are what make hosting possible.</span></span> <span data-ttu-id="b82f4-106">Однако возможно, что размещенный компонент активировал другой контекст активации, используемый для доступа к подключаемым модулям или собственным компонентам.</span><span class="sxs-lookup"><span data-stu-id="b82f4-106">However, it is possible that the component you are hosting has activated another activation context that it uses to access plug-ins or components of its own.</span></span> <span data-ttu-id="b82f4-107">В этом случае, если размещенный компонент оставляет в стеке контекст активации, ссылающийся на собственный COM-объект, приложение размещения может вызвать [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы получить объект, который должен быть собственной реализацией, а вместо этого получить объект размещенного компонента.</span><span class="sxs-lookup"><span data-stu-id="b82f4-107">In this case, if the hosted component leaves an activation context on the stack that refers to its own COM object, the hosting application might call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get an object that it expects to be its own implementation and instead receive the hosted component's object.</span></span> <span data-ttu-id="b82f4-108">Чтобы предотвратить такое наследование контекстов активации, хорошим приложениям размещения следует сначала активировать свой собственный известный контекст активации во время обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b82f4-108">To prevent this inheritance of activation contexts, a good hosting applications should activate its own well-known activation context first during a callback.</span></span>

<span data-ttu-id="b82f4-109">Рассмотрим следующий пример, защищающий код ведущего приложения:</span><span class="sxs-lookup"><span data-stu-id="b82f4-109">Consider the following example that protects the hosting application's code:</span></span>

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

<span data-ttu-id="b82f4-110">Это гарантирует, что правильный контекст активации будет установлен перед передачей запроса в некоторую внутреннюю реализацию **Func**.</span><span class="sxs-lookup"><span data-stu-id="b82f4-110">This ensures that a proper activation context is set before passing the request on to some inner implementation of **Funct**.</span></span> <span data-ttu-id="b82f4-111">Ваша собственная реализация может иметь встроенную реализацию, но предыдущий метод обеспечивает более простое взаимодействие, просто создавая делегированные оболочки.</span><span class="sxs-lookup"><span data-stu-id="b82f4-111">Your own implementation can have the actual implementation inline, but the preceding method ensures easier interoperability by just creating delegated wrappers.</span></span> <span data-ttu-id="b82f4-112">Рекомендуется использовать аналогичный метод при предоставлении обычных обратных вызовов (не COM).</span><span class="sxs-lookup"><span data-stu-id="b82f4-112">It is recommended to use a similar method when exposing normal (non-COM) callbacks.</span></span>

 

 
