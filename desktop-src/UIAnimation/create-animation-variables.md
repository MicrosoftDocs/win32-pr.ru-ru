---
title: Создание переменных анимации
description: Приложение должно создать переменную анимации для каждой визуальной характеристики, которая должна быть анимирована с помощью анимации Windows.
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- Анимация переменных анимации Windows, создание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c059a924e22700bb4abd794435ad708a2775a9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413473"
---
# <a name="create-animation-variables"></a><span data-ttu-id="4844e-104">Создание переменных анимации</span><span class="sxs-lookup"><span data-stu-id="4844e-104">Create Animation Variables</span></span>

<span data-ttu-id="4844e-105">Приложение должно создать переменную анимации для каждой визуальной характеристики, которая должна быть анимирована с помощью анимации Windows.</span><span class="sxs-lookup"><span data-stu-id="4844e-105">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span>

## <a name="overview"></a><span data-ttu-id="4844e-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="4844e-106">Overview</span></span>

<span data-ttu-id="4844e-107">Переменные анимации создаются с помощью диспетчера анимации, и приложение должно хранить ссылку на каждый из них, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="4844e-107">Animation variables are created using the animation manager, and the application should retain a reference to each for as long as it is needed.</span></span> <span data-ttu-id="4844e-108">Приложение, как правило, создает каждую переменную анимации одновременно с визуальным объектом, на котором он анимируется.</span><span class="sxs-lookup"><span data-stu-id="4844e-108">Your application will generally create each animation variable at the same time as the visual object it animates.</span></span>

<span data-ttu-id="4844e-109">При создании переменной анимации необходимо указать ее начальное значение.</span><span class="sxs-lookup"><span data-stu-id="4844e-109">When an animation variable is created, its initial value must be specified.</span></span> <span data-ttu-id="4844e-110">После этого его значение можно изменить только путем планирования раскадровок, которые ее анимировать.</span><span class="sxs-lookup"><span data-stu-id="4844e-110">Thereafter, its value can only be altered by scheduling storyboards that animate it.</span></span>

<span data-ttu-id="4844e-111">Переменные анимации передаются как параметры при создании раскадровок, поэтому приложение не должно освобождать их до тех пор, пока визуальные характеристики, которые они представляют, больше не нужны для анимации, как правило, когда связанные визуальные объекты будут уничтожены.</span><span class="sxs-lookup"><span data-stu-id="4844e-111">Animation variables are passed as parameters when storyboards are constructed, so the application should not release them until the visual characteristics they represent no longer need to be animated, typically when the associated visual objects are about to be destroyed.</span></span>

## <a name="example-code"></a><span data-ttu-id="4844e-112">Пример кода</span><span class="sxs-lookup"><span data-stu-id="4844e-112">Example Code</span></span>

-   [<span data-ttu-id="4844e-113">Анимация цветов</span><span class="sxs-lookup"><span data-stu-id="4844e-113">Animating Colors</span></span>](#animating-colors)
-   [<span data-ttu-id="4844e-114">Анимация координат x и y</span><span class="sxs-lookup"><span data-stu-id="4844e-114">Animating x and y Coordinates</span></span>](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a><span data-ttu-id="4844e-115">Анимация цветов</span><span class="sxs-lookup"><span data-stu-id="4844e-115">Animating Colors</span></span>

<span data-ttu-id="4844e-116">Следующий пример кода взят из файла MainWindow. cpp в примерах анимации Windows, [управляемой приложениями](application-driven-animation-sample.md) , и [анимацией, управляемой таймером](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4844e-116">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="4844e-117">В этом примере три переменные анимации создаются с помощью [**креатеаниматионвариабле**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) для представления цветов фона.</span><span class="sxs-lookup"><span data-stu-id="4844e-117">In the example, three animation variables are created using [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) to represent background colors.</span></span> <span data-ttu-id="4844e-118">Код также использует методы [**сетловербаунд**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) и [**сетуппербаунд**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) для управления значением переменной анимации.</span><span class="sxs-lookup"><span data-stu-id="4844e-118">The code also uses the [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) methods to control the value of the animation variable.</span></span>


```
const DOUBLE INITIAL_RED = COLOR_MAX;
const DOUBLE INITIAL_GREEN = COLOR_MAX;
const DOUBLE INITIAL_BLUE = COLOR_MAX;

HRESULT hr = m_pAnimationManager->CreateAnimationVariable(
    INITIAL_RED,
    &m_pAnimationVariableRed
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableRed->SetLowerBound(COLOR_MIN);
    if (SUCCEEDED(hr))
    {
        hr = m_pAnimationVariableRed->SetUpperBound(COLOR_MAX);
        if (SUCCEEDED(hr))
        {
            hr = m_pAnimationManager->CreateAnimationVariable(
                INITIAL_GREEN,
                &m_pAnimationVariableGreen
                );
            if (SUCCEEDED(hr))
            {
                hr = m_pAnimationVariableGreen->SetLowerBound(COLOR_MIN);
                if (SUCCEEDED(hr))
                {
                    hr = m_pAnimationVariableGreen->SetUpperBound(COLOR_MAX);
                    if (SUCCEEDED(hr))
                    {
                        hr = m_pAnimationManager->CreateAnimationVariable(
                            INITIAL_BLUE,
                            &m_pAnimationVariableBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            hr = m_pAnimationVariableBlue->SetLowerBound(COLOR_MIN);
                            if (SUCCEEDED(hr))
                            {
                                hr = m_pAnimationVariableBlue->SetUpperBound(COLOR_MAX);
                            }
                        }
                    }
                }
            }
        }
    }
}
```



<span data-ttu-id="4844e-119">Обратите внимание на следующие определения из файла MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="4844e-119">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animated Variables

    IUIAnimationVariable *m_pAnimationVariableRed;
    IUIAnimationVariable *m_pAnimationVariableGreen;
    IUIAnimationVariable *m_pAnimationVariableBlue;

    ...

};
```



### <a name="animating-x-and-y-coordinates"></a><span data-ttu-id="4844e-120">Анимация координат x и y</span><span class="sxs-lookup"><span data-stu-id="4844e-120">Animating x and y Coordinates</span></span>

<span data-ttu-id="4844e-121">Следующий пример кода взят из эскиза. cpp в [примере макета сетки](/windows/desktop/UIAnimation/grid-layout-sample)Windows Animation. см. метод Кмаинвиндов:: Креатеаниматионвариаблес.</span><span class="sxs-lookup"><span data-stu-id="4844e-121">The following example code is taken from Thumbnail.cpp in the Windows Animation [Grid Layout Sample](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::CreateAnimationVariables method.</span></span> <span data-ttu-id="4844e-122">Для представления координат X и Y каждого объекта создаются две переменные анимации.</span><span class="sxs-lookup"><span data-stu-id="4844e-122">Two animation variables are created to represent the X and Y coordinates of each object.</span></span>


```C++
// Create the animation variables for the x and y coordinates

hr = m_pAnimationManager->CreateAnimationVariable(
    xInitial,
    &m_pAnimationVariableX
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->CreateAnimationVariable(
        yInitial,
        &m_pAnimationVariableY
        );

    ...

}
```



<span data-ttu-id="4844e-123">Обратите внимание на следующие определения из эскиза. h.</span><span class="sxs-lookup"><span data-stu-id="4844e-123">Note the following definitions from Thumbnail.h.</span></span>


```
class CThumbnail
{
public:

    ...

    // X and Y Animation Variables

    IUIAnimationVariable *m_pAnimationVariableX;
    IUIAnimationVariable *m_pAnimationVariableY;

    ...

};
```



<span data-ttu-id="4844e-124">Переменные анимации — это числа с плавающей запятой, но их значения также можно получить как целые числа.</span><span class="sxs-lookup"><span data-stu-id="4844e-124">Animation variables are floating-point numbers, but their values can be fetched as integers, too.</span></span> <span data-ttu-id="4844e-125">По умолчанию каждое значение округляется до ближайшего целого числа, но можно переопределить режим округления, используемый для переменной.</span><span class="sxs-lookup"><span data-stu-id="4844e-125">By default, each value will be rounded to the nearest integer, but it is possible to override the rounding mode used for a variable.</span></span> <span data-ttu-id="4844e-126">В следующем примере кода используется метод [**сетраундингмоде**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) , чтобы указать, что значения должны округляться вниз.</span><span class="sxs-lookup"><span data-stu-id="4844e-126">The following example code uses the [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) method to specify that the values should always be rounded down.</span></span>


```C++
hr = m_pAnimationVariableX->SetRoundingMode(
    UI_ANIMATION_ROUNDING_MODE_FLOOR
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableY->SetRoundingMode(
        UI_ANIMATION_ROUNDING_MODE_FLOOR
        );

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="4844e-127">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="4844e-127">Previous Step</span></span>

<span data-ttu-id="4844e-128">Перед началом этого шага необходимо выполнить действия [в статье Создание основных объектов анимации](adding-animation-to-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="4844e-128">Before starting this step, you should have completed this step: [Create the Main Animation Objects](adding-animation-to-an-application.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="4844e-129">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="4844e-129">Next Step</span></span>

<span data-ttu-id="4844e-130">После выполнения этого шага следующий шаг: [Обновление диспетчера анимации и рисование кадров](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="4844e-130">After completing this step, the next step is: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4844e-131">См. также</span><span class="sxs-lookup"><span data-stu-id="4844e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4844e-132">**Иуианиматионманажер:: Креатеаниматионвариабле**</span><span class="sxs-lookup"><span data-stu-id="4844e-132">**IUIAnimationManager::CreateAnimationVariable**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[<span data-ttu-id="4844e-133">**Иуианиматионвариабле:: Сетловербаунд**</span><span class="sxs-lookup"><span data-stu-id="4844e-133">**IUIAnimationVariable::SetLowerBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[<span data-ttu-id="4844e-134">**Иуианиматионвариабле:: Сетраундингмоде**</span><span class="sxs-lookup"><span data-stu-id="4844e-134">**IUIAnimationVariable::SetRoundingMode**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[<span data-ttu-id="4844e-135">**Иуианиматионвариабле:: Сетуппербаунд**</span><span class="sxs-lookup"><span data-stu-id="4844e-135">**IUIAnimationVariable::SetUpperBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[<span data-ttu-id="4844e-136">Общие сведения о анимации Windows</span><span class="sxs-lookup"><span data-stu-id="4844e-136">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 