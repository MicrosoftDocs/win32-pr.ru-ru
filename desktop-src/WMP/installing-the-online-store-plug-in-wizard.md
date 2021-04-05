---
title: Установка мастера подключаемых модулей интернет-магазина
description: Установка мастера подключаемых модулей интернет-магазина
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Интернет-магазины проигрывателя Windows Media, подключаемые модули
- Интернет-магазины, подключаемые модули
- Тип 1 Интернет-магазины, подключаемые модули
- Интернет-магазин проигрывателя Windows Media в Интернете, мастер подключаемых модулей
- Интернет-магазины, мастер подключаемых модулей
- Тип 1 Интернет-магазины, мастер подключаемых модулей
- Интернет-магазины проигрывателя Windows Media, Установка подключаемого модуля
- Интернет-магазины, Установка подключаемого модуля
- Тип 1 Интернет-магазины, Установка подключаемого модуля
- подключаемые модули, Интернет-магазины проигрывателя Windows Media
- подключаемые модули, Интернет-магазины
- подключаемые модули, тип 1 Интернет-магазины
- подключаемые модули, Установка подключаемого модуля
- подключаемые модули, мастер подключаемых модулей
- Подключаемые модули проигрывателя Windows Media, введите 1 Интернет-магазины
- Подключаемые модули проигрывателя Windows Media, Интернет-магазины
- Подключаемые модули проигрывателя Windows Media, Интернет-магазины проигрывателя Windows Media
- Подключаемые модули проигрывателя Windows Media, Установка подключаемого модуля
- Подключаемые модули проигрывателя Windows Media, мастер подключаемых модулей
- Мастер установки подключаемых модулей
- Мастер подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068089"
---
# <a name="installing-the-online-store-plug-in-wizard"></a><span data-ttu-id="f2c2e-124">Установка мастера подключаемых модулей интернет-магазина</span><span class="sxs-lookup"><span data-stu-id="f2c2e-124">Installing the Online Store Plug-in Wizard</span></span>

<span data-ttu-id="f2c2e-125">Чтобы настроить среду разработки для создания подключаемых модулей интернет-магазина типа 1, необходимо установить следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="f2c2e-125">To set up your development environment for creating type 1 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="f2c2e-126">Microsoft Visual Studio 2005 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f2c2e-126">Microsoft Visual Studio 2005 or later</span></span>
-   <span data-ttu-id="f2c2e-127">Проигрыватель Windows Media 11 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f2c2e-127">Windows Media Player 11 or later</span></span>
-   <span data-ttu-id="f2c2e-128">Windows SDK, который включает в себя пакет SDK для проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="f2c2e-128">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="f2c2e-129">Мастер подключаемых модулей интернет-магазина</span><span class="sxs-lookup"><span data-stu-id="f2c2e-129">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="f2c2e-130">Установка мастера</span><span class="sxs-lookup"><span data-stu-id="f2c2e-130">Installing the Wizard</span></span>

<span data-ttu-id="f2c2e-131">Чтобы установить мастер подключаемых модулей интернет-магазина в Visual Studio, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-131">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="f2c2e-132">Откройте папку, в которую вы установили Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-132">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="f2c2e-133">Разверните папку, чтобы просмотреть ее вложенные папки, и перейдите к примерам \\ \\ \\ мастеров мультимедиа WMP \\ службы.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-133">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="f2c2e-134">Нахождение следующих трех файлов:</span><span class="sxs-lookup"><span data-stu-id="f2c2e-134">Locate the following three files:</span></span>
    -   <span data-ttu-id="f2c2e-135">вмпсервицес. vsz</span><span class="sxs-lookup"><span data-stu-id="f2c2e-135">wmpservices.vsz</span></span>
    -   <span data-ttu-id="f2c2e-136">вмпсервицес. VSDir</span><span class="sxs-lookup"><span data-stu-id="f2c2e-136">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="f2c2e-137">вмпсервицес. ico</span><span class="sxs-lookup"><span data-stu-id="f2c2e-137">wmpservices.ico</span></span>
3.  <span data-ttu-id="f2c2e-138">С помощью текстового редактора, например Блокнота, измените файл вмпсервицес. vsz.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-138">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="f2c2e-139">Найдите следующую строку:</span><span class="sxs-lookup"><span data-stu-id="f2c2e-139">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="f2c2e-140">Измените `<VsWizardEngine version goes here>` одно из следующих значений в зависимости от установленной версии Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-140">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="f2c2e-141">Значение</span><span class="sxs-lookup"><span data-stu-id="f2c2e-141">Value</span></span>              | <span data-ttu-id="f2c2e-142">Версия Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f2c2e-142">Visual Studio version</span></span> |
    |--------------------|-----------------------|
    | <span data-ttu-id="f2c2e-143">Всвизарденгине. 8.0</span><span class="sxs-lookup"><span data-stu-id="f2c2e-143">VsWizardEngine.8.0</span></span> | <span data-ttu-id="f2c2e-144">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="f2c2e-144">Visual Studio 2005</span></span>    |
    | <span data-ttu-id="f2c2e-145">Всвизарденгине. 9.0</span><span class="sxs-lookup"><span data-stu-id="f2c2e-145">VsWizardEngine.9.0</span></span> | <span data-ttu-id="f2c2e-146">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="f2c2e-146">Visual Studio 2008</span></span>    |

    

     

    <span data-ttu-id="f2c2e-147">Найдите следующую строку:</span><span class="sxs-lookup"><span data-stu-id="f2c2e-147">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="f2c2e-148">Перейдите `<path to wmpservices directory goes here>` к пути, где расположены файлы мастера.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-148">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="f2c2e-149">Например, предположим, что у вас есть Visual Studio 2008, а файлы мастера находятся здесь: C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ \\ Media WMP \\ Wizards \\ Services.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-149">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="f2c2e-150">Затем файл вмпсервицес. vsz будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f2c2e-150">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="f2c2e-151">Откройте папку, в которой установлена Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-151">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="f2c2e-152">Разверните папку, чтобы просмотреть ее вложенные папки, и выберите папку с именем вкпрожектс.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-152">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="f2c2e-153">Скопируйте три файла, перечисленные в шаге 2, в папку вкпрожектс.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-153">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="f2c2e-154">Теперь мастер установлен.</span><span class="sxs-lookup"><span data-stu-id="f2c2e-154">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2c2e-155">См. также</span><span class="sxs-lookup"><span data-stu-id="f2c2e-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2c2e-156">Создание подключаемого модуля для Интернет-магазина типа 1</span><span class="sxs-lookup"><span data-stu-id="f2c2e-156">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




