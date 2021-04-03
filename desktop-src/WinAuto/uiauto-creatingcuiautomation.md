---
title: Создание объекта Куиаутоматион
description: В этом разделе описывается, как приступить к написанию клиентского приложения Microsoft UI Automation путем создания экземпляра объекта, реализующего Иуиаутоматион.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- Клиенты, создание объекта Куиаутоматион
- Клиенты, объект Куиаутоматион
- Модель автоматизации пользовательского интерфейса, объект Куиаутоматион
- Модель автоматизации пользовательского интерфейса, создание объекта Куиаутоматион
- Создание объекта Куиаутоматион
- Объект Куиаутоматион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987568"
---
# <a name="creating-the-cuiautomation-object"></a><span data-ttu-id="14ff0-109">Создание объекта Куиаутоматион</span><span class="sxs-lookup"><span data-stu-id="14ff0-109">Creating the CUIAutomation Object</span></span>

<span data-ttu-id="14ff0-110">В этом разделе описывается, как приступить к написанию клиентского приложения Microsoft UI Automation путем создания экземпляра объекта, реализующего [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="14ff0-110">This section describes how to get started writing a Microsoft UI Automation client application by instantiating an object that implements [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>

<span data-ttu-id="14ff0-111">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="14ff0-111">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="14ff0-112">Объект Куиаутоматион</span><span class="sxs-lookup"><span data-stu-id="14ff0-112">The CUIAutomation Object</span></span>](#the-cuiautomation-object)
-   [<span data-ttu-id="14ff0-113">Создание объекта</span><span class="sxs-lookup"><span data-stu-id="14ff0-113">Creating the Object</span></span>](#creating-the-object)
-   [<span data-ttu-id="14ff0-114">См. также</span><span class="sxs-lookup"><span data-stu-id="14ff0-114">Related topics</span></span>](#related-topics)

## <a name="the-cuiautomation-object"></a><span data-ttu-id="14ff0-115">Объект Куиаутоматион</span><span class="sxs-lookup"><span data-stu-id="14ff0-115">The CUIAutomation Object</span></span>

<span data-ttu-id="14ff0-116">Первым шагом в использовании модели автоматизации пользовательского интерфейса является создание объекта класса [**куиаутоматион**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="14ff0-116">The first step in using UI Automation is to create an object of the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) class.</span></span> <span data-ttu-id="14ff0-117">Этот объект предоставляет интерфейс [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , который является шлюзом для всех других объектов и интерфейсов, используемых клиентскими приложениями.</span><span class="sxs-lookup"><span data-stu-id="14ff0-117">This object exposes the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface, which is the gateway to all the other objects and interfaces that are used by client applications.</span></span> <span data-ttu-id="14ff0-118">Помимо прочего, **иуиаутоматион** используется для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="14ff0-118">Among other things, **IUIAutomation** is used for the following tasks:</span></span>

-   <span data-ttu-id="14ff0-119">Подписка на события.</span><span class="sxs-lookup"><span data-stu-id="14ff0-119">Subscribing to events.</span></span>
-   <span data-ttu-id="14ff0-120">Создание условий.</span><span class="sxs-lookup"><span data-stu-id="14ff0-120">Creating conditions.</span></span> <span data-ttu-id="14ff0-121">Условия — это объекты, используемые для ограничения области поиска элементов модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14ff0-121">Conditions are objects used to narrow the scope of searches for UI Automation elements.</span></span>
-   <span data-ttu-id="14ff0-122">Получение элементов автоматизации пользовательского интерфейса непосредственно с рабочего стола (корневого элемента) или из экранных координат или дескрипторов окна.</span><span class="sxs-lookup"><span data-stu-id="14ff0-122">Obtaining UI Automation elements directly from the desktop (the root element), or from screen coordinates or window handles.</span></span>
-   <span data-ttu-id="14ff0-123">Создание объектов обхода дерева, которые можно использовать для навигации по иерархии элементов модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14ff0-123">Creating tree walker objects that can be used to navigate the hierarchy of UI Automation elements.</span></span>
-   <span data-ttu-id="14ff0-124">Преобразование типов данных.</span><span class="sxs-lookup"><span data-stu-id="14ff0-124">Converting data types.</span></span>

## <a name="creating-the-object"></a><span data-ttu-id="14ff0-125">Создание объекта</span><span class="sxs-lookup"><span data-stu-id="14ff0-125">Creating the Object</span></span>

<span data-ttu-id="14ff0-126">Чтобы приступить к использованию модели автоматизации пользовательского интерфейса в приложении, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="14ff0-126">To get started using UI Automation in your application, take the following steps:</span></span>

-   <span data-ttu-id="14ff0-127">Включите UIAutomation. h в заголовки проекта.</span><span class="sxs-lookup"><span data-stu-id="14ff0-127">Include UIAutomation.h in your project headers.</span></span> <span data-ttu-id="14ff0-128">UIAutomation. h предоставляет другие заголовки, определяющие API.</span><span class="sxs-lookup"><span data-stu-id="14ff0-128">UIAutomation.h brings in the other headers that define the API.</span></span>
-   <span data-ttu-id="14ff0-129">Объявите указатель на [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="14ff0-129">Declare a pointer to [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>
-   <span data-ttu-id="14ff0-130">Инициализация объектной модели компонента (COM).</span><span class="sxs-lookup"><span data-stu-id="14ff0-130">Initialize the Component Object Model (COM).</span></span>
-   <span data-ttu-id="14ff0-131">Создайте экземпляр [**куиаутоматион**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) и извлеките интерфейс [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) в указатель.</span><span class="sxs-lookup"><span data-stu-id="14ff0-131">Create an instance of [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) and retrieve the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in your pointer.</span></span>

<span data-ttu-id="14ff0-132">Следующий пример функции инициализирует COM, а затем создает объект [**куиаутоматион**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , получая интерфейс [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) в указателе *ппаутоматион* .</span><span class="sxs-lookup"><span data-stu-id="14ff0-132">The following example function initializes COM, and then creates the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) object, retrieving the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in the *ppAutomation* pointer.</span></span>


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a><span data-ttu-id="14ff0-133">См. также</span><span class="sxs-lookup"><span data-stu-id="14ff0-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="14ff0-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="14ff0-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="14ff0-135">Обзор событий автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="14ff0-135">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="14ff0-136">Получение элементов автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="14ff0-136">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> </dl>

 

 