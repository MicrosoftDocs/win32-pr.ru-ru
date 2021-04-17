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
# <a name="read-the-animation-variable-values"></a>Чтение значений переменных анимации

Каждый раз, когда приложение рисуется, оно должно считывать текущие значения переменных анимации, представляющих визуальные характеристики для анимации.

## <a name="overview"></a>Обзор

При рисовании фрейма приложение может использовать метод [**иуианиматионвариабле:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) или [**Иуианиматионвариабле:: жетинтежервалуе**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) для запроса значений любых переменных анимации, которые будут влиять на визуальные элементы внутри рамки. Можно вырезать переменную анимации в диапазон значений ([**сетловербаунд**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) и [**сетуппербаунд**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) и запросить его значение округление до целого, используя указанную схему округления ([**сетраундингмоде**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).

Вместо того чтобы считывать значения всех переменных для каждого кадра, приложение может использовать метод [**иуианиматионвариабле:: сетвариаблечанжехандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) или [**Иуианиматионвариабле:: сетвариаблеинтежерчанжехандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) для регистрации одного или нескольких обработчиков изменения переменных для получения уведомлений только в случае изменения значения переменных (IUIAnimationVariableChangeHandler [**:**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged): OnValueChanged) или округленного значения ([**IUIAnimationVariableIntegerChangeHandler:: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)). Для обнаружения переменных, передаваемых обработчикам изменений переменных, приложение может применять теги к переменным с помощью метода [**иуианиматионвариабле:: сеттаг**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) . Это объекты (IUnknown \* ), целочисленные пары, интерпретируемые приложением.

## <a name="example-code"></a>Пример кода

Следующий пример кода взят из эскиза. cpp в [макете сетки](/windows/desktop/UIAnimation/grid-layout-sample)образца анимации Windows. см. метод Кмаинвиндов:: Render. Он использует метод [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) для считывания значений в виде значений с плавающей запятой.


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



Следующий пример кода взят из файла MainWindow. cpp в примере анимации на основе [таймера](timer-driven-animation-sample.md)Windows. см. метод Кмаинвиндов::D Равбаккграунд. Для считывания значений в виде целочисленных значений используется метод [**жетинтежервалуе**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) .


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



## <a name="previous-step"></a>Предыдущий шаг

Перед началом этого шага необходимо выполнить действия [в статье обновление диспетчера анимации и рисование кадров](introducing-windows-animation-manager.md).

## <a name="next-step"></a>Следующий шаг

После завершения этого шага следующий шаг: [Создание раскадровки и добавление переходов](updating---timer-driven-animation.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Иуианиматионвариабле:: Жетинтежервалуе**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**Иуианиматионвариабле:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Общие сведения о анимации Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 