---
title: Создание основных объектов анимации
description: Чтобы использовать анимацию Windows в приложении, первым шагом является создание небольшого набора основных объектов анимации.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- Анимация объектов анимации Windows в объектах диспетчера анимации, создание
- Анимация объектов таймера Windows, создание
- Анимация объектов библиотек переходов Windows, создание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd1cab32e72bf1382469ada52abeecee47b6a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413432"
---
# <a name="create-the-main-animation-objects"></a><span data-ttu-id="32bb4-106">Создание основных объектов анимации</span><span class="sxs-lookup"><span data-stu-id="32bb4-106">Create the Main Animation Objects</span></span>

<span data-ttu-id="32bb4-107">Чтобы использовать анимацию Windows в приложении, первым шагом является создание небольшого набора основных объектов анимации.</span><span class="sxs-lookup"><span data-stu-id="32bb4-107">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span>

## <a name="overview"></a><span data-ttu-id="32bb4-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="32bb4-108">Overview</span></span>

<span data-ttu-id="32bb4-109">Используйте функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания диспетчера анимации, таймера анимации и объектов библиотеки переходов.</span><span class="sxs-lookup"><span data-stu-id="32bb4-109">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create the animation manager, animation timer, and transition library objects.</span></span>

<span data-ttu-id="32bb4-110">Эти объекты необходимы для создания и показа анимаций, поэтому они обычно не должны освобождаться до завершения работы приложения.</span><span class="sxs-lookup"><span data-stu-id="32bb4-110">These objects will be needed to create and display animations, so they usually should not be released until the application is shutting down.</span></span> <span data-ttu-id="32bb4-111">Если ни один из зарегистрированных обратных вызовов не может создать ссылочный цикл, освобождение объектов достаточно для правильной очистки.</span><span class="sxs-lookup"><span data-stu-id="32bb4-111">If there is no chance that any registered callbacks could have created a reference cycle, releasing the objects is sufficient for a proper cleanup.</span></span> <span data-ttu-id="32bb4-112">В противном случае приложение может очищаться путем очистки обратных вызовов (передача **значений NULL** в месте каждого из них) или путем вызова метода [**завершения работы**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) диспетчера анимации.</span><span class="sxs-lookup"><span data-stu-id="32bb4-112">Otherwise, the application can clean up by clearing the callbacks (passing **NULL** in the place of each) or by calling the animation manager's [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method.</span></span>

## <a name="example-code"></a><span data-ttu-id="32bb4-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="32bb4-113">Example Code</span></span>

<span data-ttu-id="32bb4-114">Следующий пример кода взят из файла MainWindow. cpp в примерах анимации Windows. см. метод Кмаинвиндов:: Инитиализеаниматион.</span><span class="sxs-lookup"><span data-stu-id="32bb4-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples; see the CMainWindow::InitializeAnimation method.</span></span>


```C++
// Create the animation manager object

HRESULT hr = CoCreateInstance(
    CLSID_UIAnimationManager,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&m_pAnimationManager)
    );

if (SUCCEEDED(hr))
{
    // Create the animation timer object

    hr = CoCreateInstance(
        CLSID_UIAnimationTimer,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pAnimationTimer)
        );

    if (SUCCEEDED(hr))
    {
        // Create the transition library object

        hr = CoCreateInstance(
            CLSID_UIAnimationTransitionLibrary,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_PPV_ARGS(&m_pTransitionLibrary)
            );

        ...

    }

    ...

}
```



<span data-ttu-id="32bb4-115">Обратите внимание на следующие определения из файла MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="32bb4-115">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animation components

    IUIAnimationManager *m_pAnimationManager;
    IUIAnimationTimer *m_pAnimationTimer;
    IUIAnimationTransitionLibrary *m_pTransitionLibrary;

    ...

};
```



## <a name="next-step"></a><span data-ttu-id="32bb4-116">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="32bb4-116">Next Step</span></span>

<span data-ttu-id="32bb4-117">После завершения этого шага следующий шаг: [Создание переменных анимации](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="32bb4-117">After completing this step, the next step is: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="32bb4-118">См. также</span><span class="sxs-lookup"><span data-stu-id="32bb4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32bb4-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="32bb4-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="32bb4-120">**иуианиматионманажер**</span><span class="sxs-lookup"><span data-stu-id="32bb4-120">**IUIAnimationManager**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[<span data-ttu-id="32bb4-121">**иуианиматионтимер**</span><span class="sxs-lookup"><span data-stu-id="32bb4-121">**IUIAnimationTimer**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[<span data-ttu-id="32bb4-122">**иуианиматионтранситионлибрари**</span><span class="sxs-lookup"><span data-stu-id="32bb4-122">**IUIAnimationTransitionLibrary**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[<span data-ttu-id="32bb4-123">Общие сведения о анимации Windows</span><span class="sxs-lookup"><span data-stu-id="32bb4-123">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 