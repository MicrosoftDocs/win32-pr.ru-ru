---
title: начало работы с помощью пакета SDK для проигрывателя Windows Media
description: начало работы с помощью пакета SDK для проигрывателя Windows Media
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Проигрыватель Windows Media Mobile, подключаемые модули
- Проигрыватель Windows Media Mobile, подключаемые модули пользовательского интерфейса
- Подключаемые модули мобильных устройств проигрывателя Windows Media
- подключаемые модули, Пользовательский интерфейс
- подключаемые модули, проигрыватель Windows Media Mobile
- подключаемые модули пользовательского интерфейса, мобильные проигрыватели Windows Media
- Подключаемые модули пользовательского интерфейса, проигрыватель Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800628"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a><span data-ttu-id="6e6be-110">начало работы с помощью пакета SDK для проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="6e6be-110">Getting Started with the Windows Media Player SDK</span></span>

<span data-ttu-id="6e6be-111">Чтобы создать подключаемый модуль, сначала необходимо установить Microsoft eMbedded Visual C++ 4,0 и Visual Studio 2003.</span><span class="sxs-lookup"><span data-stu-id="6e6be-111">To create your plug-in, you first need to install Microsoft eMbedded Visual C++ 4.0 and Visual Studio 2003.</span></span> <span data-ttu-id="6e6be-112">Необходимо также установить пакет SDK для Pocket PC 2003 или пакет SDK для Smartphone 2003, который является отдельным загружаемым компонентом.</span><span class="sxs-lookup"><span data-stu-id="6e6be-112">You must also install the Pocket PC 2003 SDK or the Smartphone 2003 SDK, which are separate downloads.</span></span> <span data-ttu-id="6e6be-113">Для компиляции и запуска проекта устройство Pocket PC или смартфон с операционной системой Windows Mobile 2003 Second Edition необходимо синхронизировать с компьютером разработчика с помощью Microsoft ActiveSync® 3.7.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="6e6be-113">To compile and run the project, a Pocket PC or Smartphone device running the Windows Mobile 2003 Second Edition operating system must be synchronized with the development computer by using Microsoft ActiveSync® 3.7.1 or later.</span></span>

<span data-ttu-id="6e6be-114">Так как подключаемые модули пользовательского интерфейса на устройствах Windows Mobile используют ту же модель подключаемых модулей, что и настольные версии, вы можете использовать мастер подключаемых модулей проигрывателя Windows Media в качестве отправной точки при создании фонового подключаемого модуля пользовательского интерфейса, который будет работать с проигрывателем Windows Media 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="6e6be-114">Because UI plug-ins on Windows Mobile devices use the same plug-in model as the desktop versions, you can use the Windows Media Player Plug-in Wizard as a starting point when creating a background UI plug-in that will work with Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="6e6be-115">Чтобы создать код подключаемого модуля пользовательского интерфейса, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6e6be-115">To create UI plug-in code, do the following:</span></span>

1.  <span data-ttu-id="6e6be-116">Откройте Visual Studio 2003 и запустите новый проект в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="6e6be-116">Open Visual Studio 2003, and start a new project in Visual C++.</span></span>
2.  <span data-ttu-id="6e6be-117">В области **шаблоны** выберите **Мастер подключаемых модулей проигрывателя Windows Media** .</span><span class="sxs-lookup"><span data-stu-id="6e6be-117">Select **Windows Media Player Plug-in Wizard** from the **Templates** pane.</span></span>
3.  <span data-ttu-id="6e6be-118">Присвойте проекту имя Нетворкплугин и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-118">Name your project NetworkPlugin and click **OK**.</span></span>
4.  <span data-ttu-id="6e6be-119">Выберите **подключаемый модуль пользовательского интерфейса** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-119">Select **UI Plug-in** and click **Next**.</span></span>
5.  <span data-ttu-id="6e6be-120">Выберите **фон** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-120">Select **Background** and click **Next**.</span></span>
6.  <span data-ttu-id="6e6be-121">Нажмите кнопку **Далее**, чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="6e6be-121">Click **Next** to finish the wizard.</span></span> <span data-ttu-id="6e6be-122">Если вы собираетесь отслеживать события с помощью подключаемого модуля, перед завершением работы мастера необходимо проверить **события прослушивания** , а также ознакомиться с документацией по интерфейсу **ивмпевентс** , чтобы узнать, какие события поддерживаются проигрывателем Windows Media 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="6e6be-122">If you are going to monitor events with your plug-in, you must check **Listen to events** before finishing the wizard, and you should read the documentation for the **IWMPEvents** interface to find out which events are supported on Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="6e6be-123">Теперь, когда вы создали код подключаемого модуля пользовательского интерфейса, необходимо создать пустой проект Windows CE DLL в eMbedded Visual C++ 4,0.</span><span class="sxs-lookup"><span data-stu-id="6e6be-123">Now that you have created your UI plug-in code, you need to create an empty Windows CE DLL project in eMbedded Visual C++ 4.0.</span></span> <span data-ttu-id="6e6be-124">Затем скопируйте созданные мастером исходные файлы в этот новый проект, чтобы они были скомпилированы с помощью компилятора ARM4.</span><span class="sxs-lookup"><span data-stu-id="6e6be-124">Then copy your wizard-generated source files to that new project so that they will compile with the ARM4 compiler.</span></span>

<span data-ttu-id="6e6be-125">Создание пустого проекта</span><span class="sxs-lookup"><span data-stu-id="6e6be-125">To create an empty project</span></span>

1.  <span data-ttu-id="6e6be-126">Запустите новый проект во встроенной Visual C++, а затем выберите **вце Dynamic-Link Library (библиотека** ) в области **проекты** .</span><span class="sxs-lookup"><span data-stu-id="6e6be-126">Start a new project in eMbedded Visual C++, and then select **WCE Dynamic-Link Library** from the **Projects** pane.</span></span>
2.  <span data-ttu-id="6e6be-127">Присвойте проекту имя и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-127">Name your project and click **OK**.</span></span>
3.  <span data-ttu-id="6e6be-128">Убедитесь, что выбран **пустой проект Windows CE DLL** , и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-128">Make sure **An empty Windows CE DLL project** is selected, and then click **Finish**.</span></span>
4.  <span data-ttu-id="6e6be-129">Щелкните элемент меню **проект** .</span><span class="sxs-lookup"><span data-stu-id="6e6be-129">Click the **Project** menu item.</span></span>
5.  <span data-ttu-id="6e6be-130">Выберите **Добавить в проект**, а затем щелкните **файлы**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-130">Select **Add to Project**, and then click **Files**.</span></span>
6.  <span data-ttu-id="6e6be-131">Выберите файлы C++, созданные с помощью мастера подключаемых модулей, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-131">Select the C++ files you created with the plug-in wizard, and then click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e6be-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6e6be-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e6be-133">**Создание подключаемого модуля пользовательского интерфейса для проигрывателя Windows Media 10 Mobile**</span><span class="sxs-lookup"><span data-stu-id="6e6be-133">**Creating a User Interface Plug-in for Windows Media Player 10 Mobile**</span></span>](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[<span data-ttu-id="6e6be-134">**Интерфейс Ивмпевентс**</span><span class="sxs-lookup"><span data-stu-id="6e6be-134">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




