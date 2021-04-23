---
title: Чтение значений переменных анимации
description: Каждый раз, когда приложение рисуется, оно должно считывать текущие значения переменных анимации, представляющих визуальные характеристики для анимации.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- Анимация для переменных анимации Windows, чтение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691596"
---
# <a name="read-the-animation-variable-values"></a><span data-ttu-id="85e23-104">Чтение значений переменных анимации</span><span class="sxs-lookup"><span data-stu-id="85e23-104">Read the Animation Variable Values</span></span>

<span data-ttu-id="85e23-105">Каждый раз, когда приложение рисуется, оно должно считывать текущие значения переменных анимации, представляющих визуальные характеристики для анимации.</span><span class="sxs-lookup"><span data-stu-id="85e23-105">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span>

## <a name="overview"></a><span data-ttu-id="85e23-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="85e23-106">Overview</span></span>

<span data-ttu-id="85e23-107">При рисовании фрейма приложение может использовать метод [**иуианиматионвариабле:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) или [**Иуианиматионвариабле:: жетинтежервалуе**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) для запроса значений любых переменных анимации, которые будут влиять на визуальные элементы внутри рамки.</span><span class="sxs-lookup"><span data-stu-id="85e23-107">When drawing a frame, an application can use the [**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) or [**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to request the values of any animation variables that will affect visuals within the frame.</span></span> <span data-ttu-id="85e23-108">Можно вырезать переменную анимации в диапазон значений ([**сетловербаунд**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) и [**сетуппербаунд**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) и запросить его значение округление до целого, используя указанную схему округления ([**сетраундингмоде**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span><span class="sxs-lookup"><span data-stu-id="85e23-108">It is possible to clip an animation variable to a range of values ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)), and to request its value be rounded to an integer using a specified rounding scheme ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span></span>

<span data-ttu-id="85e23-109">Вместо того чтобы считывать значения всех переменных для каждого кадра, приложение может использовать метод [**иуианиматионвариабле:: сетвариаблечанжехандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) или [**Иуианиматионвариабле:: сетвариаблеинтежерчанжехандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) для регистрации одного или нескольких обработчиков изменения переменных для получения уведомлений только в случае изменения значения переменных (IUIAnimationVariableChangeHandler [**:**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged): OnValueChanged) или округленного значения ([**IUIAnimationVariableIntegerChangeHandler:: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span><span class="sxs-lookup"><span data-stu-id="85e23-109">Instead of reading the values of all variables for every frame, an application can use the [**IUIAnimationVariable::SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) or [**IUIAnimationVariable::SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) method to register one or more variable change handlers to receive notifications only when there is a change to the variables' value ([**IUIAnimationVariableChangeHandler::OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) or rounded value ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span></span> <span data-ttu-id="85e23-110">Для обнаружения переменных, передаваемых обработчикам изменений переменных, приложение может применять теги к переменным с помощью метода [**иуианиматионвариабле:: сеттаг**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) .</span><span class="sxs-lookup"><span data-stu-id="85e23-110">To identify the variables passed to variable change handlers, an application can apply tags to variables using the [**IUIAnimationVariable::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) method.</span></span> <span data-ttu-id="85e23-111">Это объекты (IUnknown \* ), целочисленные пары, интерпретируемые приложением.</span><span class="sxs-lookup"><span data-stu-id="85e23-111">These are object (IUnknown\*), integer pairs that are interpreted by the application.</span></span>

## <a name="example-code"></a><span data-ttu-id="85e23-112">Пример кода</span><span class="sxs-lookup"><span data-stu-id="85e23-112">Example Code</span></span>

<span data-ttu-id="85e23-113">Следующий пример кода взят из эскиза. cpp в [макете сетки](/windows/desktop/UIAnimation/grid-layout-sample)образца анимации Windows. см. метод Кмаинвиндов:: Render.</span><span class="sxs-lookup"><span data-stu-id="85e23-113">The following example code is taken from Thumbnail.cpp in the Windows Animation sample [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::Render method.</span></span> <span data-ttu-id="85e23-114">Он использует метод [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) для считывания значений в виде значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="85e23-114">It uses the [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) method to read the values as floating-point values.</span></span>


```C++
// Get the x-coordinate and y-coordinate animation variable values

DOUBLE x=0;
hr = m_pAnimationVariableX->GetValue(&x);
if (SUCCEEDED(hr))
{
    DOUBLE y=0;
    hr = m_pAnimationVariableY->GetValue(&y);
    if (SUCCEEDED(hr))
    {
        // Draw the object

        ...

    }
}
```



<span data-ttu-id="85e23-115">Следующий пример кода взят из файла MainWindow. cpp в примере анимации на основе [таймера](timer-driven-animation-sample.md)Windows. см. метод Кмаинвиндов::D Равбаккграунд.</span><span class="sxs-lookup"><span data-stu-id="85e23-115">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::DrawBackground method.</span></span> <span data-ttu-id="85e23-116">Для считывания значений в виде целочисленных значений используется метод [**жетинтежервалуе**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) .</span><span class="sxs-lookup"><span data-stu-id="85e23-116">It uses the [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to read the values as integer values.</span></span>


```C++
// Get the RGB animation variable values

INT32 red;
HRESULT hr = m_pAnimationVariableRed->GetIntegerValue(
    &red
    );
if (SUCCEEDED(hr))
{
    INT32 green;
    hr = m_pAnimationVariableGreen->GetIntegerValue(
        &green
        );
    if (SUCCEEDED(hr))
    {
        INT32 blue;
        hr = m_pAnimationVariableBlue->GetIntegerValue(
            &blue
            );
        if (SUCCEEDED(hr))
        {
            // Set the RGB of the background brush to the new animated value

            ...
                
            // Paint the background

            ...

        }
    }

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="85e23-117">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="85e23-117">Previous Step</span></span>

<span data-ttu-id="85e23-118">Перед началом этого шага необходимо выполнить действия [в статье обновление диспетчера анимации и рисование кадров](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="85e23-118">Before starting this step, you should have completed this step: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="85e23-119">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="85e23-119">Next Step</span></span>

<span data-ttu-id="85e23-120">После завершения этого шага следующий шаг: [Создание раскадровки и добавление переходов](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="85e23-120">After completing this step, the next step is: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="85e23-121">См. также</span><span class="sxs-lookup"><span data-stu-id="85e23-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85e23-122">**Иуианиматионвариабле:: Жетинтежервалуе**</span><span class="sxs-lookup"><span data-stu-id="85e23-122">**IUIAnimationVariable::GetIntegerValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[<span data-ttu-id="85e23-123">**Иуианиматионвариабле:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="85e23-123">**IUIAnimationVariable::GetValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[<span data-ttu-id="85e23-124">Общие сведения о анимации Windows</span><span class="sxs-lookup"><span data-stu-id="85e23-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 