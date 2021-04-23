---
title: Пример перечисления задач
description: Чтобы перечислить задачи, необходимо вызвать перечисление Итасксчедулер, чтобы создать объект перечисления. Затем используйте интерфейс Иенумворкитемс объекта перечисления, чтобы перечислить задачи в папке "запланированные задания".
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672353"
---
# <a name="enumerating-tasks-example"></a><span data-ttu-id="d9977-104">Пример перечисления задач</span><span class="sxs-lookup"><span data-stu-id="d9977-104">Enumerating Tasks Example</span></span>

<span data-ttu-id="d9977-105">Чтобы перечислить задачи, необходимо вызвать [**итасксчедулер:: Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) , чтобы создать [*объект перечисления*](e.md).</span><span class="sxs-lookup"><span data-stu-id="d9977-105">To enumerate tasks, you must call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to create an [*enumeration object*](e.md).</span></span> <span data-ttu-id="d9977-106">Затем используйте интерфейс [**иенумворкитемс**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) объекта перечисления, чтобы перечислить задачи в папке "запланированные задания".</span><span class="sxs-lookup"><span data-stu-id="d9977-106">Then, use the enumeration object's [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="d9977-107">Следующая процедура описывает, как перечислить задачи в папке «Назначенные задания».</span><span class="sxs-lookup"><span data-stu-id="d9977-107">The following procedure describes how to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="d9977-108">**Перечисление задач в папке «Назначенные задания»**</span><span class="sxs-lookup"><span data-stu-id="d9977-108">**To enumerate the tasks in the Scheduled Tasks folder**</span></span>

1.  <span data-ttu-id="d9977-109">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="d9977-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="d9977-110">(В этом примере предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="d9977-110">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="d9977-111">Вызовите [**итасксчедулер:: Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) , чтобы получить объект перечисления.</span><span class="sxs-lookup"><span data-stu-id="d9977-111">Call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to get an enumeration object.</span></span>
3.  <span data-ttu-id="d9977-112">Чтобы получить задачи, вызовите метод [**иенумворкитемс:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) .</span><span class="sxs-lookup"><span data-stu-id="d9977-112">Call [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) to retrieve the tasks.</span></span> <span data-ttu-id="d9977-113">(В этом примере предпринимается попытка получить пять задач при каждом вызове.)</span><span class="sxs-lookup"><span data-stu-id="d9977-113">(This example tries to retrieve five tasks with each call.)</span></span>
4.  <span data-ttu-id="d9977-114">Обработка возвращенных задач.</span><span class="sxs-lookup"><span data-stu-id="d9977-114">Process the tasks returned.</span></span> <span data-ttu-id="d9977-115">(Этот пример просто выводит на экран имя каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="d9977-115">(This example simply prints the name of each task to the screen.</span></span>
5.  <span data-ttu-id="d9977-116">Ресурсы выпуска.</span><span class="sxs-lookup"><span data-stu-id="d9977-116">Release resources.</span></span> <span data-ttu-id="d9977-117">Вызовите [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память, используемую для имен.</span><span class="sxs-lookup"><span data-stu-id="d9977-117">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory used for names.</span></span>



| <span data-ttu-id="d9977-118">Пример кода</span><span class="sxs-lookup"><span data-stu-id="d9977-118">For a code example of</span></span>                                                         | <span data-ttu-id="d9977-119">См.</span><span class="sxs-lookup"><span data-stu-id="d9977-119">See</span></span>                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d9977-120">Перечисление всех задач в папке "запланированные задания" на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="d9977-120">Enumerating all the tasks in the Scheduled Tasks folder of the local computer</span></span> | [<span data-ttu-id="d9977-121">Пример кода C/C++. Перечисление задач</span><span class="sxs-lookup"><span data-stu-id="d9977-121">C/C++ Code Example: Enumerating Tasks</span></span>](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a><span data-ttu-id="d9977-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d9977-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9977-123">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="d9977-123">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 