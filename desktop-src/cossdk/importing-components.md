---
description: Средство администрирования служб компонентов можно использовать для импорта в приложения конкретных компонентов, которые уже зарегистрированы на компьютере как компоненты COM в реестре Windows.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Импорт компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496029"
---
# <a name="importing-components"></a><span data-ttu-id="bb668-103">Импорт компонентов</span><span class="sxs-lookup"><span data-stu-id="bb668-103">Importing Components</span></span>

<span data-ttu-id="bb668-104">Средство администрирования служб компонентов можно использовать для импорта в приложения конкретных компонентов, которые уже зарегистрированы на компьютере как компоненты COM в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="bb668-104">You can use the Component Services administrative tool to import into applications specific components that have already been registered on your computer as COM components in the Windows registry.</span></span> <span data-ttu-id="bb668-105">При импорте компонента не устанавливаются сведения о интерфейсе или методе, необходимые для задания свойств интерфейса или для настройки доступа к компоненту с удаленного клиента.</span><span class="sxs-lookup"><span data-stu-id="bb668-105">Importing a component does not install the interface or method information required to set interface properties or to configure access to the component from a remote client.</span></span> <span data-ttu-id="bb668-106">Поэтому, если это возможно, следует установить, а не импортировать ненастроенные компоненты.</span><span class="sxs-lookup"><span data-stu-id="bb668-106">Therefore, if possible, you should install rather than import unconfigured components.</span></span>

> [!Note]  
> <span data-ttu-id="bb668-107">При импорте компонента в приложение COM+ COM+ не заполняет сведения об интерфейсе и методе для компонента.</span><span class="sxs-lookup"><span data-stu-id="bb668-107">When importing a component into a COM+ application, COM+ does not populate interface and method information for the component.</span></span> <span data-ttu-id="bb668-108">Во время экспорта прокси приложения COM+ не будет предоставлять сведения о маршалировании (библиотеки типов, прокси-серверы и заглушки) для некоторых или всех интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="bb668-108">During the export of an application proxy, COM+ will not provide marshaling information (type libraries or proxy/stubs) for some or all of the interfaces.</span></span> <span data-ttu-id="bb668-109">Экспорт прокси приложений, содержащих импортированные компоненты, завершится ошибкой или выдаст предупреждение.</span><span class="sxs-lookup"><span data-stu-id="bb668-109">Exporting application proxies that contain imported components will fail or cause a warning to be issued.</span></span>

 

<span data-ttu-id="bb668-110">**Импорт компонента в приложение COM+**</span><span class="sxs-lookup"><span data-stu-id="bb668-110">**To import a component into a COM+ application**</span></span>

1.  <span data-ttu-id="bb668-111">В дереве консоли средства администрирования "службы компонентов" выберите компьютер, на котором размещено приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="bb668-111">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="bb668-112">Откройте папку **приложения COM+** для этого компьютера и выберите приложение, в котором необходимо установить компонент.</span><span class="sxs-lookup"><span data-stu-id="bb668-112">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component.</span></span>

3.  <span data-ttu-id="bb668-113">Откройте папку приложение и выберите **компоненты**.</span><span class="sxs-lookup"><span data-stu-id="bb668-113">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="bb668-114">В меню **действие** наведите указатель на пункт **создать** и выберите пункт **компонент**.</span><span class="sxs-lookup"><span data-stu-id="bb668-114">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="bb668-115">Можно также щелкнуть правой кнопкой мыши папку **компоненты** , наведите указатель на пункт **создать** и выберите пункт **компонент**.</span><span class="sxs-lookup"><span data-stu-id="bb668-115">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="bb668-116">На странице **приветствия** мастера установки приложения COM+ нажмите кнопку **Далее**, а затем в диалоговом окне **Импорт или установка компонента** нажмите кнопку **импортировать компоненты, которые уже зарегистрированы**.</span><span class="sxs-lookup"><span data-stu-id="bb668-116">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Import component(s) that are already registered**.</span></span>

6.  <span data-ttu-id="bb668-117">В диалоговом окне **Выбор компонентов для импорта** установите флажок **сведения** , чтобы просмотреть полные сведения о уже зарегистрированных компонентах.</span><span class="sxs-lookup"><span data-stu-id="bb668-117">In the **Choose Components to Import** dialog box, select the **Details** check box to see complete information about the components that are already registered.</span></span> <span data-ttu-id="bb668-118">Выберите компоненты, которые необходимо импортировать из списка, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bb668-118">Select the component(s) you want to import from the displayed list, and click **Next**.</span></span>

7.  <span data-ttu-id="bb668-119">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bb668-119">Click **Finish**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb668-120">См. также</span><span class="sxs-lookup"><span data-stu-id="bb668-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb668-121">Копирование компонентов</span><span class="sxs-lookup"><span data-stu-id="bb668-121">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="bb668-122">Создание нового приложения COM+</span><span class="sxs-lookup"><span data-stu-id="bb668-122">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="bb668-123">Удаление приложения COM+</span><span class="sxs-lookup"><span data-stu-id="bb668-123">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="bb668-124">Установка новых компонентов</span><span class="sxs-lookup"><span data-stu-id="bb668-124">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="bb668-125">Перемещение компонентов</span><span class="sxs-lookup"><span data-stu-id="bb668-125">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="bb668-126">Удаление компонента из приложения COM+</span><span class="sxs-lookup"><span data-stu-id="bb668-126">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



