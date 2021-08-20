---
title: Создание раскадровки и добавление переходов
description: Чтобы создать анимацию, приложение должно создать раскадровку.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- раскадровки Windows анимация, создание
- раскадровки Windows анимации, добавление переходов
- переходы Windows анимация, создание
- переходы Windows анимация, добавление в раскадровку
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f992ae7720fea692d5e0b813e6cb9c35fab61d4bf2c781c928d9c8fcd08adb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999644"
---
# <a name="create-a-storyboard-and-add-transitions"></a>Создание раскадровки и добавление переходов

Чтобы создать анимацию, приложение должно создать раскадровку.

## <a name="overview"></a>Обзор

Ниже приведены общие шаги для создания раскадровки.

1.  Создание раскадровки
2.  Создание одного или нескольких переходов
3.  Добавление переходов в раскадровку с указанием переменных, которые они анимированы

Пустую раскадровку можно создать с помощью диспетчера анимации. Приложение должно заполнить каждую раскадровку с помощью переходов. Каждый переход указывает, как изменяется одна переменная анимации за заданный интервал времени. переходы можно создавать с помощью компонента библиотеки переходов, который входит в Windowsную анимацию. Кроме того, приложение может создавать собственные пользовательские переходы или использовать библиотеку переходов от третьей стороны. Когда приложение добавляет переход к раскадровке, оно указывает, какую переменную анимации будет анимировать переход.

Раскадровка может включать переходы по одной или нескольким переменным анимации. Более сложные раскадровки могут использовать ключевые кадры для синхронизации запуска или завершения переходов или для указания частей раскадровки, которые должны повторяться (фиксированное число раз или неопределенное время).

## <a name="example-code"></a>Пример кода

следующий пример кода берется из файла MainWindow. cpp в Windows анимации, [управляемой таймером](timer-driven-animation-sample.md). см. метод Кмаинвиндов:: Чанжеколор. В этом примере создается Раскадровка (шаг 1) с помощью метода [**иуианиматионманажер:: креатесторибоард**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , создаются переходы (шаг 2) с помощью метода [**Иуианиматионтранситионлибрари:: креатеакцелератедецелератетранситион**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) и добавляются переходы к раскадровке (шаг 3) с помощью метода [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .


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



## <a name="previous-step"></a>Предыдущий шаг

Перед началом этого шага необходимо выполнить шаг: [чтение значений переменных анимации](updating---application-driven-animation.md).

## <a name="next-step"></a>Следующий шаг

После завершения этого шага следующий шаг: [планирование раскадровки](scheduling-a-storyboard.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Иуианиматионманажер:: Креатесторибоард**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**Иуианиматионсторибоард:: Аддтранситион**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**Иуианиматионтранситионлибрари:: Креатеакцелератедецелератетранситион**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[Общие сведения о раскадровке](storyboard-construction.md)
</dt> </dl>

 

 




