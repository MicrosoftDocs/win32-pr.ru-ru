---
title: Планирование раскадровки
description: После создания раскадровки она планируется диспетчером анимации.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- раскадровки Windows анимация, планирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013adc114fd09f518c34bc15ca2e7799381b6cee3dfeeedaf3b26fcae6d506e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008174"
---
# <a name="schedule-a-storyboard"></a>Планирование раскадровки

После создания раскадровки она планируется диспетчером анимации.

## <a name="overview"></a>Обзор

По умолчанию каждая раскадровка запускается немедленно по расписанию. Это означает, что когда раскадровка начинается для анимации одной или нескольких переменных, она может прерывать любые другие раскадровки, анимированные эти же переменные. Однако приложение может указать другие варианты поведения, определив относительный приоритет между раскадровками.

После того как раскадровка запланирована, она больше не может быть изменена. Однако после удаления раскадровки из расписания ее можно запланировать еще раз. Разработчикам следует соблюдать осторожность при повторном использовании раскадровок, так как это следует делать только в том случае, когда нет шансов, что одна и та же раскадровка может потребоваться поместить в очередь из-за действия пользователя, когда оно уже воспроизводилось или поставлено в очередь в расписании.

## <a name="example-code"></a>Пример кода

следующий пример кода взят из файла MainWindow. cpp в Windows анимация, [управляемая приложениями](application-driven-animation-sample.md) , и анимация, [управляемая таймером](timer-driven-animation-sample.md). Для планирования раскадровки используется метод [**иуианиматионсторибоард:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) . Этот метод требует текущего времени в качестве параметра.


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a>Предыдущий шаг

Перед началом этого шага необходимо завершить этот шаг: [Создание раскадровки и добавление переходов](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Иуианиматионсторибоард:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**Иуианиматионтимер:: во время**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Общие сведения о раскадровке](storyboard-construction.md)
</dt> </dl>

 

 




