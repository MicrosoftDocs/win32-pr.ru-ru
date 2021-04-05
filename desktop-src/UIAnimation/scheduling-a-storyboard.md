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
# <a name="schedule-a-storyboard"></a><span data-ttu-id="12106-104">Планирование раскадровки</span><span class="sxs-lookup"><span data-stu-id="12106-104">Schedule a Storyboard</span></span>

<span data-ttu-id="12106-105">После создания раскадровки она планируется диспетчером анимации.</span><span class="sxs-lookup"><span data-stu-id="12106-105">After a storyboard is created, it is scheduled by the animation manager.</span></span>

## <a name="overview"></a><span data-ttu-id="12106-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="12106-106">Overview</span></span>

<span data-ttu-id="12106-107">По умолчанию каждая раскадровка запускается немедленно по расписанию.</span><span class="sxs-lookup"><span data-stu-id="12106-107">By default, each storyboard starts immediately when it is scheduled.</span></span> <span data-ttu-id="12106-108">Это означает, что когда раскадровка начинается для анимации одной или нескольких переменных, она может прерывать любые другие раскадровки, анимированные эти же переменные.</span><span class="sxs-lookup"><span data-stu-id="12106-108">This means that when a storyboard starts to animate one or more variables, it may interrupt any other storyboards animating those same variables.</span></span> <span data-ttu-id="12106-109">Однако приложение может указать другие варианты поведения, определив относительный приоритет между раскадровками.</span><span class="sxs-lookup"><span data-stu-id="12106-109">However, an application may specify other behaviors by determining the relative priority between storyboards.</span></span>

<span data-ttu-id="12106-110">После того как раскадровка запланирована, она больше не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="12106-110">After a storyboard has been scheduled, it can no longer be altered.</span></span> <span data-ttu-id="12106-111">Однако после удаления раскадровки из расписания ее можно запланировать еще раз.</span><span class="sxs-lookup"><span data-stu-id="12106-111">However, after a storyboard has been removed from the schedule, it can be scheduled for play again.</span></span> <span data-ttu-id="12106-112">Разработчикам следует соблюдать осторожность при повторном использовании раскадровок, так как это следует делать только в том случае, когда нет шансов, что одна и та же раскадровка может потребоваться поместить в очередь из-за действия пользователя, когда оно уже воспроизводилось или поставлено в очередь в расписании.</span><span class="sxs-lookup"><span data-stu-id="12106-112">Developers should exercise caution when re-using storyboards, as this should only be done where there is no chance that the same storyboard might need to be queued due to a user action when it is already playing or queued in the schedule.</span></span>

## <a name="example-code"></a><span data-ttu-id="12106-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="12106-113">Example Code</span></span>

<span data-ttu-id="12106-114">Следующий пример кода взят из файла MainWindow. cpp в примерах анимации Windows, [управляемой приложениями](application-driven-animation-sample.md) , и [анимацией, управляемой таймером](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="12106-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="12106-115">Для планирования раскадровки используется метод [**иуианиматионсторибоард:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) .</span><span class="sxs-lookup"><span data-stu-id="12106-115">It uses the [**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) method to schedule the storyboard.</span></span> <span data-ttu-id="12106-116">Этот метод требует текущего времени в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="12106-116">This method requires the current time as a parameter.</span></span>


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



## <a name="previous-step"></a><span data-ttu-id="12106-117">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="12106-117">Previous Step</span></span>

<span data-ttu-id="12106-118">Перед началом этого шага необходимо завершить этот шаг: [Создание раскадровки и добавление переходов](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="12106-118">Before starting this step, you should have completed this step: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12106-119">См. также</span><span class="sxs-lookup"><span data-stu-id="12106-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12106-120">**Иуианиматионсторибоард:: Schedule**</span><span class="sxs-lookup"><span data-stu-id="12106-120">**IUIAnimationStoryboard::Schedule**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[<span data-ttu-id="12106-121">**Иуианиматионтимер:: во время**</span><span class="sxs-lookup"><span data-stu-id="12106-121">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="12106-122">Общие сведения о раскадровке</span><span class="sxs-lookup"><span data-stu-id="12106-122">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




