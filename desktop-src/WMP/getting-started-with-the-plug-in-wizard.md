---
title: начало работы с помощью мастера подключаемых модулей
description: начало работы с помощью мастера подключаемых модулей
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Подключаемые модули проигрывателя Windows Media, Установка подключаемого модуля
- подключаемые модули, Установка подключаемого модуля
- Создание подключаемых модулей, мастер установки подключаемых модулей
- Мастер подключаемых модулей проигрывателя Windows Media, установка
- Мастер установки подключаемых модулей
- Мастер подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986684"
---
# <a name="getting-started-with-the-plug-in-wizard"></a><span data-ttu-id="d17d6-109">начало работы с помощью мастера подключаемых модулей</span><span class="sxs-lookup"><span data-stu-id="d17d6-109">Getting Started with the Plug-in Wizard</span></span>

<span data-ttu-id="d17d6-110">Чтобы настроить среду разработки для создания подключаемых модулей проигрывателя Windows Media, необходимо установить следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="d17d6-110">To set up your development environment for creating Windows Media Player plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="d17d6-111">Microsoft Visual Studio .NET 2003 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d17d6-111">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="d17d6-112">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d17d6-112">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="d17d6-113">Windows SDK, который включает в себя пакет SDK для проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="d17d6-113">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="d17d6-114">Мастер подключаемых модулей проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="d17d6-114">Windows Media Player Plug-in Wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="d17d6-115">Установка мастера</span><span class="sxs-lookup"><span data-stu-id="d17d6-115">Installing the Wizard</span></span>

<span data-ttu-id="d17d6-116">Чтобы установить мастер подключаемых модулей проигрывателя Windows Media, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d17d6-116">Perform the following steps to install the Windows Media Player Plug-in Wizard.</span></span>

1.  <span data-ttu-id="d17d6-117">Откройте папку, в которую вы установили Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d17d6-117">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="d17d6-118">Разверните папку, чтобы просмотреть ее вложенные папки, и перейдите к примерам \\ \\ \\ мастеров мультимедиа WMP \\ вмпвиз.</span><span class="sxs-lookup"><span data-stu-id="d17d6-118">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span>
2.  <span data-ttu-id="d17d6-119">Нахождение следующих трех файлов:</span><span class="sxs-lookup"><span data-stu-id="d17d6-119">Locate the following three files:</span></span>
    -   <span data-ttu-id="d17d6-120">вмпвиз. vsz</span><span class="sxs-lookup"><span data-stu-id="d17d6-120">wmpwiz.vsz</span></span>
    -   <span data-ttu-id="d17d6-121">вмпвиз. VSDir</span><span class="sxs-lookup"><span data-stu-id="d17d6-121">wmpwiz.vsdir</span></span>
    -   <span data-ttu-id="d17d6-122">вмпвиз. ico</span><span class="sxs-lookup"><span data-stu-id="d17d6-122">wmpwiz.ico</span></span>
3.  <span data-ttu-id="d17d6-123">С помощью текстового редактора, например Блокнота, измените файл вмпвиз. vsz.</span><span class="sxs-lookup"><span data-stu-id="d17d6-123">Using a text editor, such as Notepad, edit the wmpwiz.vsz file.</span></span>

    <span data-ttu-id="d17d6-124">Найдите следующую строку:</span><span class="sxs-lookup"><span data-stu-id="d17d6-124">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="d17d6-125">Измените `<VsWizardEngine version goes here>` одно из следующих значений в зависимости от установленной версии Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d17d6-125">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="d17d6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d17d6-126">Value</span></span>              | <span data-ttu-id="d17d6-127">Версия Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d17d6-127">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="d17d6-128">Всвизарденгине. 7.1</span><span class="sxs-lookup"><span data-stu-id="d17d6-128">VsWizardEngine.7.1</span></span> | <span data-ttu-id="d17d6-129">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="d17d6-129">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="d17d6-130">Всвизарденгине. 8.0</span><span class="sxs-lookup"><span data-stu-id="d17d6-130">VsWizardEngine.8.0</span></span> | <span data-ttu-id="d17d6-131">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="d17d6-131">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="d17d6-132">Всвизарденгине. 9.0</span><span class="sxs-lookup"><span data-stu-id="d17d6-132">VsWizardEngine.9.0</span></span> | <span data-ttu-id="d17d6-133">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="d17d6-133">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="d17d6-134">Найдите следующую строку:</span><span class="sxs-lookup"><span data-stu-id="d17d6-134">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    <span data-ttu-id="d17d6-135">Перейдите `<path to wmpwiz directory goes here>` к пути, где расположены файлы мастера.</span><span class="sxs-lookup"><span data-stu-id="d17d6-135">Change `<path to wmpwiz directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="d17d6-136">Например, предположим, что у вас есть Visual Studio 2008, а файлы мастера находятся здесь: C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ \\ Media WMP \\ Wizards \\ вмпвиз.</span><span class="sxs-lookup"><span data-stu-id="d17d6-136">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span> <span data-ttu-id="d17d6-137">Затем файл вмпвиз. vsz будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d17d6-137">Then your wmpwiz.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="d17d6-138">Откройте папку, в которой установлена Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d17d6-138">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="d17d6-139">Разверните папку, чтобы просмотреть ее вложенные папки, и выберите папку с именем вкпрожектс.</span><span class="sxs-lookup"><span data-stu-id="d17d6-139">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="d17d6-140">Скопируйте три файла, перечисленные в шаге 2, в папку вкпрожектс.</span><span class="sxs-lookup"><span data-stu-id="d17d6-140">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="d17d6-141">Теперь мастер установлен.</span><span class="sxs-lookup"><span data-stu-id="d17d6-141">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d17d6-142">См. также</span><span class="sxs-lookup"><span data-stu-id="d17d6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d17d6-143">Создание подключаемого модуля</span><span class="sxs-lookup"><span data-stu-id="d17d6-143">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> <dt>

[<span data-ttu-id="d17d6-144">Использование мастера подключаемых модулей в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d17d6-144">Using the Plug-in Wizard with Visual Studio</span></span>](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




