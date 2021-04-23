---
title: Повторение задачи
description: Планировщик задач может запускать задачу любое количество раз после срабатывания триггера.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- шаблон повторения планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331227"
---
# <a name="repeating-a-task"></a><span data-ttu-id="7b4d8-104">Повторение задачи</span><span class="sxs-lookup"><span data-stu-id="7b4d8-104">Repeating A Task</span></span>

<span data-ttu-id="7b4d8-105">Планировщик задач может запускать задачу любое количество раз после срабатывания триггера.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-105">Task Scheduler can run a task any number of times times after a trigger is fired.</span></span> <span data-ttu-id="7b4d8-106">Для этого триггер определяет шаблон повторения, который указывает, планировщик задач как долго должно повторяться задача и интервал времени между повторениями задач.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-106">To do this, the trigger defines a repetition pattern that tells Task Scheduler how long it should continue to repeat the task and the time interval between each task repetition.</span></span>

## <a name="repetition-pattern"></a><span data-ttu-id="7b4d8-107">Шаблон повторения</span><span class="sxs-lookup"><span data-stu-id="7b4d8-107">Repetition Pattern</span></span>

<span data-ttu-id="7b4d8-108">На следующем рисунке показан шаблон повторения с длительностью 60 минут и интервалом в 25 минут.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-108">The following illustration shows a repetition pattern with a duration of 60 minutes and an interval of 25 minutes.</span></span> <span data-ttu-id="7b4d8-109">Имейте в виду, что в этом случае планировщик задач запускает задачу при срабатывании триггера, она снова запускает задачу через 25 минут, а затем повторно запускает задачу через 50 минут в зависимости от значения [**Свойства Стопатдуратионенд ирепетитионпаттерн**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**репетитионпаттерн. стопатдуратионенд**](repetitionpattern-stopatdurationend.md) для сценариев).</span><span class="sxs-lookup"><span data-stu-id="7b4d8-109">Be aware that in this case, Task Scheduler runs the task when the trigger is fired, it runs the task again after 25 minutes, then runs the task again after 50 minutes depending on the setting of the [**StopAtDurationEnd property of IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) for scripting).</span></span> <span data-ttu-id="7b4d8-110">Если свойство **стопатдуратионенд** имеет значение True, планировщик задач останавливает последний экземпляр задачи, если он по-прежнему выполняется через 60 минут.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-110">If the **StopAtDurationEnd** property is set to True, Task Scheduler stops the last instance of the task if it is still running after 60 minutes.</span></span> <span data-ttu-id="7b4d8-111">Если свойство **стопатдуратионенд** имеет значение false, то последний экземпляр задачи выполняется независимо от длительности.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-111">If the **StopAtDurationEnd** property is set to False, the last instance of the task is run regardless of the duration.</span></span>

![шаблон повторения триггера](images/repetition-pattern.png)

<span data-ttu-id="7b4d8-113">Если зарегистрировать задачу, содержащую триггер с интервалом повтора, равный одной минуте, а длительность повторения — четыре минуты, задача будет запущена пять раз.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-113">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started five times.</span></span> <span data-ttu-id="7b4d8-114">Пять повторений можно определить в следующем шаблоне:</span><span class="sxs-lookup"><span data-stu-id="7b4d8-114">The five repetitions can be defined by the following pattern:</span></span>

1.  <span data-ttu-id="7b4d8-115">Задача начинается в начале первой минуты.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-115">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="7b4d8-116">Следующая задача начинается в конце первой минуты.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-116">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="7b4d8-117">Следующая задача начинается в конце второй минуты.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-117">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="7b4d8-118">Следующая задача начинается в конце третьей минуты.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-118">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="7b4d8-119">Следующая задача начинается в конце четвертой минуты.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-119">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="7b4d8-120">**Windows Server 2003, Windows XP и windows 2000:** Если зарегистрировать задачу, содержащую триггер с интервалом повтора, равный одной минуте, а длительность повторения — четыре минуты, задача будет запущена четыре раза.</span><span class="sxs-lookup"><span data-stu-id="7b4d8-120">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started four times.</span></span>

## <a name="objects-interfaces-and-xml-elements"></a><span data-ttu-id="7b4d8-121">Объекты, интерфейсы и XML-элементы</span><span class="sxs-lookup"><span data-stu-id="7b4d8-121">Objects, Interfaces, and XML Elements</span></span>

<span data-ttu-id="7b4d8-122">Для разработки сценариев шаблон повторения определяется с помощью объекта [**репетитионпаттерн**](repetitionpattern.md) .</span><span class="sxs-lookup"><span data-stu-id="7b4d8-122">For scripting development, the repetition pattern is defined using the [**RepetitionPattern**](repetitionpattern.md) object.</span></span>

<span data-ttu-id="7b4d8-123">Для разработки на C++ шаблон повторения определяется интерфейсом [**ирепетитионпаттерн**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) .</span><span class="sxs-lookup"><span data-stu-id="7b4d8-123">For C++ development, the repetition pattern is defined by the [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) interface.</span></span>

<span data-ttu-id="7b4d8-124">При чтении или записи XML для задачи шаблон повторения указывается в элементе [**повторения**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7b4d8-124">When reading or writing XML for a task, the repetition pattern is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b4d8-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7b4d8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b4d8-126">Триггеры задач</span><span class="sxs-lookup"><span data-stu-id="7b4d8-126">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




