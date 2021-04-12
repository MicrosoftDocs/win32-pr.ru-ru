---
title: Создание раскадровки и добавление переходов
description: Чтобы создать анимацию, приложение должно создать раскадровку.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- Раскадровка анимация Windows, создание
- Раскадровка анимация Windows, Добавление переходов
- переходы по анимации Windows, создание
- переходы по анимации Windows, добавление в раскадровку
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee85aac4db11371c9a1e4a2aa254421d217cfd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331648"
---
# <a name="create-a-storyboard-and-add-transitions"></a><span data-ttu-id="fc847-107">Создание раскадровки и добавление переходов</span><span class="sxs-lookup"><span data-stu-id="fc847-107">Create a Storyboard and Add Transitions</span></span>

<span data-ttu-id="fc847-108">Чтобы создать анимацию, приложение должно создать раскадровку.</span><span class="sxs-lookup"><span data-stu-id="fc847-108">To create an animation, an application must construct a storyboard.</span></span>

## <a name="overview"></a><span data-ttu-id="fc847-109">Обзор</span><span class="sxs-lookup"><span data-stu-id="fc847-109">Overview</span></span>

<span data-ttu-id="fc847-110">Ниже приведены общие шаги для создания раскадровки.</span><span class="sxs-lookup"><span data-stu-id="fc847-110">The general steps for constructing a storyboard are as follows:</span></span>

1.  <span data-ttu-id="fc847-111">Создание раскадровки</span><span class="sxs-lookup"><span data-stu-id="fc847-111">Create a storyboard</span></span>
2.  <span data-ttu-id="fc847-112">Создание одного или нескольких переходов</span><span class="sxs-lookup"><span data-stu-id="fc847-112">Create one or more transitions</span></span>
3.  <span data-ttu-id="fc847-113">Добавление переходов в раскадровку с указанием переменных, которые они анимированы</span><span class="sxs-lookup"><span data-stu-id="fc847-113">Add the transitions to the storyboard, specifying which variables they animate</span></span>

<span data-ttu-id="fc847-114">Пустую раскадровку можно создать с помощью диспетчера анимации.</span><span class="sxs-lookup"><span data-stu-id="fc847-114">An empty storyboard can be created using the animation manager.</span></span> <span data-ttu-id="fc847-115">Приложение должно заполнить каждую раскадровку с помощью переходов.</span><span class="sxs-lookup"><span data-stu-id="fc847-115">The application must populate each storyboard with transitions.</span></span> <span data-ttu-id="fc847-116">Каждый переход указывает, как изменяется одна переменная анимации за заданный интервал времени.</span><span class="sxs-lookup"><span data-stu-id="fc847-116">Each transition specifies how a single animation variable changes over a given time interval.</span></span> <span data-ttu-id="fc847-117">Переходы можно создавать с помощью компонента библиотеки переходов, который входит в состав анимации Windows.</span><span class="sxs-lookup"><span data-stu-id="fc847-117">Transitions can be created using the transition library component included in Windows Animation.</span></span> <span data-ttu-id="fc847-118">Кроме того, приложение может создавать собственные пользовательские переходы или использовать библиотеку переходов от третьей стороны.</span><span class="sxs-lookup"><span data-stu-id="fc847-118">Alternately, an application can create its own custom transitions or use a transition library from a third party.</span></span> <span data-ttu-id="fc847-119">Когда приложение добавляет переход к раскадровке, оно указывает, какую переменную анимации будет анимировать переход.</span><span class="sxs-lookup"><span data-stu-id="fc847-119">When the application adds a transition to a storyboard, it specifies which animation variable the transition will animate.</span></span>

<span data-ttu-id="fc847-120">Раскадровка может включать переходы по одной или нескольким переменным анимации.</span><span class="sxs-lookup"><span data-stu-id="fc847-120">A storyboard may include transitions on one or more animation variables.</span></span> <span data-ttu-id="fc847-121">Более сложные раскадровки могут использовать ключевые кадры для синхронизации запуска или завершения переходов или для указания частей раскадровки, которые должны повторяться (фиксированное число раз или неопределенное время).</span><span class="sxs-lookup"><span data-stu-id="fc847-121">More complex storyboards can use keyframes to synchronize the starts or ends of transitions, or to specify portions of the storyboard that should repeat (a fixed number of times or indefinitely).</span></span>

## <a name="example-code"></a><span data-ttu-id="fc847-122">Пример кода</span><span class="sxs-lookup"><span data-stu-id="fc847-122">Example Code</span></span>

<span data-ttu-id="fc847-123">Следующий пример кода взят из файла MainWindow. cpp в примере анимации на основе [таймера](timer-driven-animation-sample.md)Windows. см. метод Кмаинвиндов:: Чанжеколор.</span><span class="sxs-lookup"><span data-stu-id="fc847-123">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::ChangeColor method.</span></span> <span data-ttu-id="fc847-124">В этом примере создается Раскадровка (шаг 1) с помощью метода [**иуианиматионманажер:: креатесторибоард**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , создаются переходы (шаг 2) с помощью метода [**Иуианиматионтранситионлибрари:: креатеакцелератедецелератетранситион**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) и добавляются переходы к раскадровке (шаг 3) с помощью метода [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .</span><span class="sxs-lookup"><span data-stu-id="fc847-124">This example creates the storyboard (step 1) using the [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) method, creates the transitions (step 2) using the [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) method, and adds the transitions to the storyboard (step 3) using the [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) method.</span></span>


```C++
const UI_ANIMATION_SECONDS DURATION = 0.5;
const DOUBLE ACCELERATION_RATIO = 0.5;
const DOUBLE DECELERATION_RATIO = 0.5;

// Create a storyboard

IUIAnimationStoryboard *pStoryboard = NULL;
HRESULT hr = m_pAnimationManager->CreateStoryboard(
    &pStoryboard
    );
if (SUCCEEDED(hr))
{
    // Create transitions for the RGB animation variables

    IUIAnimationTransition *pTransitionRed;
    hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
        DURATION,
        red,
        ACCELERATION_RATIO,
        DECELERATION_RATIO,
        &pTransitionRed
        );
    if (SUCCEEDED(hr))
    {
        IUIAnimationTransition *pTransitionGreen;
        hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
            DURATION,
            green,
            ACCELERATION_RATIO,
            DECELERATION_RATIO,
            &pTransitionGreen
            );
        if (SUCCEEDED(hr))
        {
            IUIAnimationTransition *pTransitionBlue;
            hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
                DURATION,
                blue,
                ACCELERATION_RATIO,
                DECELERATION_RATIO,
                &pTransitionBlue
                );
            if (SUCCEEDED(hr))
            {
                // Add transitions to the storyboard

                hr = pStoryboard->AddTransition(
                    m_pAnimationVariableRed,
                    pTransitionRed
                    );
                if (SUCCEEDED(hr))
                {
                    hr = pStoryboard->AddTransition(
                        m_pAnimationVariableGreen,
                        pTransitionGreen
                        );
                    if (SUCCEEDED(hr))
                    {
                        hr = pStoryboard->AddTransition(
                            m_pAnimationVariableBlue,
                            pTransitionBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            // Get the current time and schedule the storyboard for play

                            ...

}
```



## <a name="previous-step"></a><span data-ttu-id="fc847-125">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="fc847-125">Previous Step</span></span>

<span data-ttu-id="fc847-126">Перед началом этого шага необходимо выполнить шаг: [чтение значений переменных анимации](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="fc847-126">Before starting this step, you should have completed this step: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="fc847-127">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="fc847-127">Next Step</span></span>

<span data-ttu-id="fc847-128">После завершения этого шага следующий шаг: [планирование раскадровки](scheduling-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="fc847-128">After completing this step, the next step is: [Schedule a Storyboard](scheduling-a-storyboard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc847-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fc847-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc847-130">**Иуианиматионманажер:: Креатесторибоард**</span><span class="sxs-lookup"><span data-stu-id="fc847-130">**IUIAnimationManager::CreateStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[<span data-ttu-id="fc847-131">**Иуианиматионсторибоард:: Аддтранситион**</span><span class="sxs-lookup"><span data-stu-id="fc847-131">**IUIAnimationStoryboard::AddTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[<span data-ttu-id="fc847-132">**Иуианиматионтранситионлибрари:: Креатеакцелератедецелератетранситион**</span><span class="sxs-lookup"><span data-stu-id="fc847-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[<span data-ttu-id="fc847-133">Общие сведения о раскадровке</span><span class="sxs-lookup"><span data-stu-id="fc847-133">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




