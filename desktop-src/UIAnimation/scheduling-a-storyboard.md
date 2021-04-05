---
title: Планирование раскадровки
description: После создания раскадровки она планируется диспетчером анимации.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- 'Раскадровка Windows: анимация, планирование'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067415"
---
# <a name="schedule-a-storyboard"></a>Планирование раскадровки

После создания раскадровки она планируется диспетчером анимации.

## <a name="overview"></a>Обзор

По умолчанию каждая раскадровка запускается немедленно по расписанию. Это означает, что когда раскадровка начинается для анимации одной или нескольких переменных, она может прерывать любые другие раскадровки, анимированные эти же переменные. Однако приложение может указать другие варианты поведения, определив относительный приоритет между раскадровками.

После того как раскадровка запланирована, она больше не может быть изменена. Однако после удаления раскадровки из расписания ее можно запланировать еще раз. Разработчикам следует соблюдать осторожность при повторном использовании раскадровок, так как это следует делать только в том случае, когда нет шансов, что одна и та же раскадровка может потребоваться поместить в очередь из-за действия пользователя, когда оно уже воспроизводилось или поставлено в очередь в расписании.

## <a name="example-code"></a>Пример кода

Следующий пример кода взят из файла MainWindow. cpp в примерах анимации Windows, [управляемой приложениями](application-driven-animation-sample.md) , и [анимацией, управляемой таймером](timer-driven-animation-sample.md). Для планирования раскадровки используется метод [**иуианиматионсторибоард:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) . Этот метод требует текущего времени в качестве параметра.


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

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Иуианиматионсторибоард:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**Иуианиматионтимер:: во время**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Общие сведения о раскадровке](storyboard-construction.md)
</dt> </dl>

 

 




