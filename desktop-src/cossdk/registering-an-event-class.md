---
description: Чтобы подписчики могли найти класс событий и подписываться на него, классы событий должны быть зарегистрированы в каталоге COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Регистрация класса событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807367"
---
# <a name="registering-an-event-class"></a><span data-ttu-id="f4a7f-103">Регистрация класса событий</span><span class="sxs-lookup"><span data-stu-id="f4a7f-103">Registering an Event Class</span></span>

<span data-ttu-id="f4a7f-104">Чтобы подписчики могли найти класс событий и подписываться на него, классы событий должны быть зарегистрированы в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-104">So that subscribers can find an event class and subscribe to it, event classes must be registered in the COM+ catalog.</span></span> <span data-ttu-id="f4a7f-105">Для COM+ требуется библиотека типов, которая описывает интерфейсы и методы событий, чтобы они могли правильно сопоставлять и связывать подписчиков и издателей.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-105">COM+ requires a type library that describes the event interfaces and methods so that it can properly match and connect subscribers and publishers.</span></span> <span data-ttu-id="f4a7f-106">Библиотека типов должна находиться в библиотеке DLL с собственной регистрацией или сопровождаться ей.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-106">The type library must reside in or be accompanied by a self-registering DLL.</span></span>

<span data-ttu-id="f4a7f-107">Для регистрации класса событий в каталоге COM+ можно использовать средство администрирования служб компонентов или административные функции COM+.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-107">You can use the Component Services administrative tool or the COM+ Administrative functions to register an event class in the COM+ catalog.</span></span>

<span data-ttu-id="f4a7f-108">**Регистрация класса событий с помощью средства администрирования "службы компонентов"**</span><span class="sxs-lookup"><span data-stu-id="f4a7f-108">**To register an event class with the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="f4a7f-109">Создайте новое приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-109">Create a new COM+ application.</span></span>

2.  <span data-ttu-id="f4a7f-110">Откройте папку приложение и выберите **компоненты**.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-110">Open the application folder and select **Components**.</span></span>

3.  <span data-ttu-id="f4a7f-111">В меню **действие** выберите команду **создать**.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-111">On the **Action** menu, click **New**.</span></span> <span data-ttu-id="f4a7f-112">(Можно также выбрать папку **компоненты** , щелкнуть правой кнопкой мыши, наведите указатель на пункт **создать** и выберите пункт **компонент**.)</span><span class="sxs-lookup"><span data-stu-id="f4a7f-112">(You can also select the **Components** folder, right-click, point to **New**, and then click **Component**.)</span></span>

4.  <span data-ttu-id="f4a7f-113">Щелкните **установить новые классы событий**.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-113">Click **Install new event class(es)**.</span></span>

5.  <span data-ttu-id="f4a7f-114">Введите путь к библиотеке DLL компонента класса событий.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-114">Enter the path to the event class component DLL.</span></span>

6.  <span data-ttu-id="f4a7f-115">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-115">Click **OK**.</span></span>

<span data-ttu-id="f4a7f-116">Класс событий регистрируется в каталоге COM+ и может быть найден подписчиками, заинтересованными в получении сведений, предоставленных классом событий.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-116">The event class is registered in the COM+ catalog and can be located by subscribers interested in obtaining the information provided by the event class.</span></span> <span data-ttu-id="f4a7f-117">Сведения о том, как зарегистрировать класс событий с помощью административных интерфейсов COM+, см. в разделе [**икомадминкаталог:: инсталлевенткласс**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span><span class="sxs-lookup"><span data-stu-id="f4a7f-117">For information about how to register the event class by using the COM+ administrative interfaces, see [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4a7f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f4a7f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4a7f-119">Регистрация подписки</span><span class="sxs-lookup"><span data-stu-id="f4a7f-119">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 



