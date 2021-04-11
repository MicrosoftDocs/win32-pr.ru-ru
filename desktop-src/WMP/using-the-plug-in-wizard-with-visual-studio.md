---
title: Использование мастера подключаемых модулей в Visual Studio
description: Использование мастера подключаемых модулей в Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Подключаемые модули проигрывателя Windows Media, Visual Studio
- подключаемые модули, Visual Studio
- Создание подключаемых модулей, Visual Studio
- Мастер подключаемых модулей проигрывателя Windows Media, Visual Studio
- Visual Studio, мастер подключаемых модулей проигрывателя Windows Media
- Мастер подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330712"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="ee0aa-109">Использование мастера подключаемых модулей в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ee0aa-109">Using the Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="ee0aa-110">После установки необходимых компонентов можно быстро создать подключаемый модуль, который будет служить отправной точкой.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-110">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="ee0aa-111">Следующие шаги помогут вам.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-111">The following steps will guide you.</span></span>

1.  <span data-ttu-id="ee0aa-112">Запустите Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-112">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="ee0aa-113">В меню **файл** наведите указатель мыши на пункт **создать** и выберите пункт **проект**.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-113">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="ee0aa-114">В списке **типы проектов** выберите **Visual C++ проекты**.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-114">In **Project Types**, select **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="ee0aa-115">В окне **шаблоны** выберите **Мастер подключаемых модулей проигрывателя Windows Media**.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-115">In **Templates**, select **Windows Media Player Plug-in Wizard**.</span></span>
5.  <span data-ttu-id="ee0aa-116">Введите имя проекта.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-116">Enter a name for your project.</span></span>
6.  <span data-ttu-id="ee0aa-117">Введите расположение проекта.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-117">Enter a location for your project.</span></span> <span data-ttu-id="ee0aa-118">Это папка, в которую будут копироваться файлы проекта.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-118">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="ee0aa-119">Нажмите кнопку **ОК** , чтобы запустить мастер.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-119">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="ee0aa-120">Выберите тип подключаемого модуля, который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-120">Select the type of plug-in you want to create.</span></span>
9.  <span data-ttu-id="ee0aa-121">Заполните оставшиеся диалоговые окна в мастере.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-121">Complete any remaining dialog boxes in the wizard.</span></span>
10. <span data-ttu-id="ee0aa-122">Используйте среду разработки Visual Studio для построения проекта.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-122">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="ee0aa-123">В Windows Vista и более поздних версиях проект не будет успешно построен, если вы не запустите Visual Studio с полным маркером доступа администратора.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-123">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="ee0aa-124">Щелкните правой кнопкой мыши имя или значок Visual Studio и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-124">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="ee0aa-125">Прежде чем пытаться выполнить сборку проекта, необходимо настроить среду разработки так, чтобы она указывала на папки с именами include и lib, где установлен Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-125">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="ee0aa-126">Компилятору и компоновщику потребуется доступ к некоторым файлам в этих папках.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-126">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="ee0aa-127">Если вы запустили программу регистрации Visual Studio, которая поставляется вместе с Windows SDK, возможно, среда разработки уже настроена так, чтобы она указывала на папки Windows SDK include и lib.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-127">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="ee0aa-128">В противном случае необходимо вручную настроить среду разработки.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-128">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="ee0aa-129">Чтобы вручную настроить Visual Studio, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-129">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="ee0aa-130">В меню **Сервис** выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-130">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="ee0aa-131">Щелкните **проекты и решения**, а затем выберите **каталоги VC + +**.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-131">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="ee0aa-132">В разделе **Показ каталогов для** выберите **включить файлы** или **файлы библиотек**.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-132">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="ee0aa-133">Добавьте каталоги для необходимых файлов.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-133">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee0aa-134">См. также</span><span class="sxs-lookup"><span data-stu-id="ee0aa-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee0aa-135">Создание подключаемого модуля</span><span class="sxs-lookup"><span data-stu-id="ee0aa-135">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> </dl>

 

 




