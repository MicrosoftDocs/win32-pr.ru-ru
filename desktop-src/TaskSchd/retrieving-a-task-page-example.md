---
title: Получение примера страницы задачи
description: Чтобы получить страницу задачи, необходимо вызвать ITask QueryInterface, чтобы получить интерфейс Ипровидетаскпаже, а затем вызвать Ипровидетаскпаже @ Page. Метод метода Page возвращает на страницу маркер, который затем может использоваться для вывода запрошенной страницы.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- получение планировщик задач страницы задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070171"
---
# <a name="retrieving-a-task-page-example"></a><span data-ttu-id="23a92-105">Получение примера страницы задачи</span><span class="sxs-lookup"><span data-stu-id="23a92-105">Retrieving a Task Page Example</span></span>

<span data-ttu-id="23a92-106">Чтобы получить страницу задачи, необходимо вызвать метод **ITask:: QueryInterface** , чтобы получить интерфейс [**ипровидетаскпаже**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) , а затем вызвать [**ипровидетаскпаже::-Page**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span><span class="sxs-lookup"><span data-stu-id="23a92-106">To retrieve a task page you must call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface, then call [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span></span> <span data-ttu-id="23a92-107">Метод метода **Page** возвращает на страницу маркер, который затем может использоваться для вывода запрошенной страницы.</span><span class="sxs-lookup"><span data-stu-id="23a92-107">The **GetPage** method returns a handle to the page, which can then be used to display the page you requested.</span></span>

> [!Note]  
> <span data-ttu-id="23a92-108">В следующем примере кода все интерфейсы освобождаются после того, как они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="23a92-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="23a92-109">В следующей процедуре описывается создание нового триггера.</span><span class="sxs-lookup"><span data-stu-id="23a92-109">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="23a92-110">**Создание нового триггера**</span><span class="sxs-lookup"><span data-stu-id="23a92-110">**To create a new trigger**</span></span>

1.  <span data-ttu-id="23a92-111">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="23a92-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="23a92-112">(В этом примере предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="23a92-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="23a92-113">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="23a92-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="23a92-114">(Обратите внимание, что в этом примере возвращается задача "задача тестирования".)</span><span class="sxs-lookup"><span data-stu-id="23a92-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="23a92-115">Вызовите метод **ITask:: QueryInterface** , чтобы получить интерфейс [**ипровидетаскпаже**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) и [**ипровидетаскпаже::-Page**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) , чтобы получить страницу.</span><span class="sxs-lookup"><span data-stu-id="23a92-115">Call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface and [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) to retrieve the page.</span></span>
4.  <span data-ttu-id="23a92-116">С помощью возвращенного маркера страницы отобразите страницу.</span><span class="sxs-lookup"><span data-stu-id="23a92-116">Using the returned page handle, display the page.</span></span>



| <span data-ttu-id="23a92-117">Пример кода</span><span class="sxs-lookup"><span data-stu-id="23a92-117">For a code example of</span></span>                                   | <span data-ttu-id="23a92-118">См.</span><span class="sxs-lookup"><span data-stu-id="23a92-118">See</span></span>                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="23a92-119">Получение и отображение страницы задачи для известной задачи</span><span class="sxs-lookup"><span data-stu-id="23a92-119">Retrieving and displaying the Task page of a known task</span></span> | [<span data-ttu-id="23a92-120">Получение страницы задачи</span><span class="sxs-lookup"><span data-stu-id="23a92-120">Retrieving a Task Page</span></span>](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a><span data-ttu-id="23a92-121">См. также</span><span class="sxs-lookup"><span data-stu-id="23a92-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23a92-122">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="23a92-122">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 