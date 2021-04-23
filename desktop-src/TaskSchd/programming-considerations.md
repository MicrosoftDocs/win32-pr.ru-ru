---
title: Вопросы программирования (планировщик задач)
description: При разработке приложений, использующих планировщик задач 1,0, учитывайте следующие вопросы программирования. Приложение должно убедиться, что служба планировщик задач запущена, прежде чем пытаться выполнить вызовы с помощью API планировщик задач. При извлечении строк убедитесь, что вы вызываете CoTaskMemFree, чтобы освободить каждую строку после того, как она больше не нужна. При извлечении массивов строк убедитесь, что сначала выпустите каждую строку в массиве, а затем Освободите сам массив. При создании или изменении рабочего элемента, включая триггеры, связанные с рабочим элементом, необходимо вызвать IPersistFile Save, чтобы сохранить рабочий элемент на диске. После использования любого интерфейса, предоставляемого планировщик задач API, убедитесь, что для освобождения интерфейса вызовите метод IUnknown Release. Интерфейс IUnknown поддерживается каждым объектом планировщик задач.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- Запуск планировщик задач
- рекомендации по программированию планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105672439"
---
# <a name="programming-considerations-task-scheduler"></a><span data-ttu-id="9c240-107">Вопросы программирования (планировщик задач)</span><span class="sxs-lookup"><span data-stu-id="9c240-107">Programming Considerations (Task Scheduler)</span></span>

<span data-ttu-id="9c240-108">При разработке приложений, использующих планировщик задач 1,0, учитывайте следующие вопросы программирования.</span><span class="sxs-lookup"><span data-stu-id="9c240-108">When developing applications that use the Task Scheduler 1.0, keep the following programming issues in mind.</span></span>

-   <span data-ttu-id="9c240-109">Приложение должно убедиться, что служба планировщик задач запущена, прежде чем пытаться выполнить вызовы с помощью API планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="9c240-109">Your application must ensure the Task Scheduler service is running before attempting to make any calls using the Task Scheduler API.</span></span>
-   <span data-ttu-id="9c240-110">При извлечении строк убедитесь, что вы вызываете [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить каждую строку после того, как она больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="9c240-110">When retrieving strings, make sure that you call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release each string after it is no longer needed.</span></span> <span data-ttu-id="9c240-111">При извлечении массивов строк убедитесь, что сначала выпустите каждую строку в массиве, а затем Освободите сам массив.</span><span class="sxs-lookup"><span data-stu-id="9c240-111">When retrieving arrays of strings, make sure you first release each string in the array and then release the array itself.</span></span>
-   <span data-ttu-id="9c240-112">При создании или изменении рабочего элемента, включая триггеры, связанные с рабочим элементом, обязательно вызовите [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , чтобы сохранить рабочий элемент на диске.</span><span class="sxs-lookup"><span data-stu-id="9c240-112">When creating or modifying a work item, including triggers associated with a work item, make sure you call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the work item to disk.</span></span>
-   <span data-ttu-id="9c240-113">После использования любого интерфейса, предоставляемого планировщик задач API, убедитесь, что вызывается метод [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , чтобы освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="9c240-113">After using any of the interfaces that are provided by the Task Scheduler API, make sure you call [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the interface.</span></span> <span data-ttu-id="9c240-114">[**Интерфейс IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) поддерживается каждым объектом планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="9c240-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is supported by each Task Scheduler object.</span></span>

<span data-ttu-id="9c240-115">Раздел using документации по планировщик задач содержит многочисленные примеры, которые следуют этим рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="9c240-115">The Using section of the Task Scheduler documentation provides numerous examples that follow these guidelines.</span></span> <span data-ttu-id="9c240-116">В таблице ниже приводятся ссылки на некоторые из этих примеров.</span><span class="sxs-lookup"><span data-stu-id="9c240-116">The table below provides jumps to some of these examples.</span></span>

| <span data-ttu-id="9c240-117">Пример</span><span class="sxs-lookup"><span data-stu-id="9c240-117">For an example of</span></span>         | <span data-ttu-id="9c240-118">См.</span><span class="sxs-lookup"><span data-stu-id="9c240-118">See</span></span>                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c240-119">Освобождение строк</span><span class="sxs-lookup"><span data-stu-id="9c240-119">Releasing strings</span></span>         | [<span data-ttu-id="9c240-120">Получение примеров свойств рабочего элемента</span><span class="sxs-lookup"><span data-stu-id="9c240-120">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="9c240-121">Сохранение рабочих элементов на диск</span><span class="sxs-lookup"><span data-stu-id="9c240-121">Saving work items to disk</span></span> | [<span data-ttu-id="9c240-122">Примеры настройки свойств рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="9c240-122">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |
| <span data-ttu-id="9c240-123">Освобождение интерфейсов</span><span class="sxs-lookup"><span data-stu-id="9c240-123">Releasing interfaces</span></span>      | [<span data-ttu-id="9c240-124">Создание задачи с помощью примера Невворкитем</span><span class="sxs-lookup"><span data-stu-id="9c240-124">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |



 

 

 
