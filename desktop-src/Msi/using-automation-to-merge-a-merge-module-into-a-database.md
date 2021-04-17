---
description: Модули слияния предоставляют стандартный метод для предоставления общих компонентов установщик Windows и настройки логики для приложений.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Использование службы автоматизации для слияния модуля слияния в базу данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673429"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a><span data-ttu-id="2957a-103">Использование службы автоматизации для слияния модуля слияния в базу данных</span><span class="sxs-lookup"><span data-stu-id="2957a-103">Using Automation to Merge a Merge Module into a Database</span></span>

<span data-ttu-id="2957a-104">[Модули слияния](merge-modules.md) предоставляют стандартный метод для предоставления общих [*компонентов*](c-gly.md)установщик Windows и настройки логики для приложений.</span><span class="sxs-lookup"><span data-stu-id="2957a-104">[Merge Modules](merge-modules.md) provide a standard method for you to deliver shared Windows Installer [*components*](c-gly.md), and setup logic to applications.</span></span>

<span data-ttu-id="2957a-105">Модули слияния должны быть объединены в пакет установки с помощью средства слияния.</span><span class="sxs-lookup"><span data-stu-id="2957a-105">Merge modules must be merged into an installation package by using a merge tool.</span></span> <span data-ttu-id="2957a-106">Рекомендуется получить свободно распространяемое средство слияния или приобрести один из средств слияния, доступных из независимых поставщиков программного обеспечения, например, можно использовать [Mergemod.dll](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="2957a-106">The best practice is to obtain a freely distributed merge tool, or purchase one of the merge tools that are available from independent software vendors, for example, you can use [Mergemod.dll](merge-module-automation.md).</span></span>

<span data-ttu-id="2957a-107">В следующей процедуре показано, как объединить модуль слияния в базу данных установщик Windows с помощью [службы автоматизации модуля слияния](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="2957a-107">The following procedure shows you how to merge a merge module into a Windows Installer database by using [Merge Module Automation](merge-module-automation.md).</span></span>

<span data-ttu-id="2957a-108">**Объединение модуля в базу данных**</span><span class="sxs-lookup"><span data-stu-id="2957a-108">**To merge a module into a database**</span></span>

1.  <span data-ttu-id="2957a-109">Откройте файл журнала с помощью метода [**опенлог**](merge-openlog.md) .</span><span class="sxs-lookup"><span data-stu-id="2957a-109">Open a log file by using the [**OpenLog**](merge-openlog.md) method.</span></span>

    <span data-ttu-id="2957a-110">Этот шаг необходим только в том случае, если необходимо создать файл журнала или добавить существующий файл журнала для процесса слияния.</span><span class="sxs-lookup"><span data-stu-id="2957a-110">This step is required only if you need to create a log file, or append an existing log file for the merge process.</span></span>

2.  <span data-ttu-id="2957a-111">Откройте базу данных установки [. msi](windows-installer-file-extensions.md) с помощью метода [**опендатабасе**](merge-opendatabase.md) [**объекта Merge**](merge-object.md).</span><span class="sxs-lookup"><span data-stu-id="2957a-111">Open the [.msi](windows-installer-file-extensions.md) installation database by using the [**OpenDatabase**](merge-opendatabase.md) method of the [**Merge Object**](merge-object.md).</span></span>

    <span data-ttu-id="2957a-112">Этот шаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2957a-112">This step is required.</span></span>

    <span data-ttu-id="2957a-113">Открываемая база данных должна получить модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="2957a-113">The database that you open is the one that you want to receive the merge module.</span></span>

3.  <span data-ttu-id="2957a-114">Откройте модуль [MSM](windows-installer-file-extensions.md) MERGE с помощью метода [**опенмодуле**](merge-openmodule.md) .</span><span class="sxs-lookup"><span data-stu-id="2957a-114">Open the [.msm](windows-installer-file-extensions.md) merge module by using the [**OpenModule**](merge-openmodule.md) method.</span></span>

    <span data-ttu-id="2957a-115">Этот шаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2957a-115">This step is required.</span></span>

    <span data-ttu-id="2957a-116">Это модуль слияния, который объединяется с базой данных.</span><span class="sxs-lookup"><span data-stu-id="2957a-116">This is the merge module that is being merged into the database.</span></span> <span data-ttu-id="2957a-117">Модуль необходимо открыть, прежде чем его можно будет объединить с базой данных установки.</span><span class="sxs-lookup"><span data-stu-id="2957a-117">A module must be opened before it can be merged with an installation database.</span></span>

4.  <span data-ttu-id="2957a-118">Объедините модуль в базу данных установки, вызвав метод [**Merge**](merge-object.md) или [**мержеекс**](merge-mergeex.md) .</span><span class="sxs-lookup"><span data-stu-id="2957a-118">Merge the module into the installation database by calling the [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method.</span></span>

    <span data-ttu-id="2957a-119">Этот шаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2957a-119">This step is required.</span></span>

    <span data-ttu-id="2957a-120">Метод [**Merge**](merge-object.md) или метод [**мержеекс**](merge-mergeex.md) можно вызывать только один раз для слияния определенного сочетания файлов [. msi](windows-installer-file-extensions.md) и. msm.</span><span class="sxs-lookup"><span data-stu-id="2957a-120">The [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method can only be called one time to merge a specific combination of [.msi](windows-installer-file-extensions.md) and .msm files.</span></span>

    > [!Note]  
    > <span data-ttu-id="2957a-121">Метод [**мержеекс**](merge-mergeex.md) доступен только в [Mergemod.dll версии 2,0](merge-module-automation.md) или более поздней и только при использовании интерфейса [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="2957a-121">The [**MergeEx**](merge-mergeex.md) method is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later, and only when using the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface.</span></span>

     

5.  <span data-ttu-id="2957a-122">Получите свойство [**Errors**](merge-errors.md) и изучите коллекцию объектов [**Error**](error-object.md) , которые она возвращает для конфликтов слияния или других ошибок.</span><span class="sxs-lookup"><span data-stu-id="2957a-122">Retrieve the [**Errors**](merge-errors.md) property and examine the collection of [**Error**](error-object.md) objects it returns for merge conflicts or other errors.</span></span>

    <span data-ttu-id="2957a-123">Необходимо устранить все ошибки.</span><span class="sxs-lookup"><span data-stu-id="2957a-123">You must resolve any errors.</span></span>

    <span data-ttu-id="2957a-124">Извлечение является необратимым, и несколько экземпляров коллекции ошибок могут быть получены путем многократного считывания свойства [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="2957a-124">The retrieval is nondestructive, and multiple instances of the error collection can be retrieved by repeatedly reading the [**Errors**](merge-errors.md) property.</span></span>

6.  <span data-ttu-id="2957a-125">Свяжите компоненты модуля слияния с функциями с помощью метода [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="2957a-125">Associate the components of the merge module with the features by using the [**Connect**](merge-connect.md) method.</span></span>

    <span data-ttu-id="2957a-126">Этот шаг необходим только в том случае, если у вас есть компоненты и вы хотите добавить компоненты для слияния в базу данных установки.</span><span class="sxs-lookup"><span data-stu-id="2957a-126">This step is only required if you have existing features and you want to add features to merge into the installation database.</span></span>

    <span data-ttu-id="2957a-127">Перед вызовом этого метода должна существовать функция.</span><span class="sxs-lookup"><span data-stu-id="2957a-127">A feature must exist before you call this method.</span></span> <span data-ttu-id="2957a-128">Дополнительные сведения см. [в разделе Подключение модуля слияния к нескольким компонентам](connecting-a-merge-module-to-multiple-features.md).</span><span class="sxs-lookup"><span data-stu-id="2957a-128">For more information, see [Connecting a Merge Module to Multiple Features](connecting-a-merge-module-to-multiple-features.md).</span></span>

7.  <span data-ttu-id="2957a-129">При необходимости извлеките исходные файлы из модуля, выполнив одно или несколько из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="2957a-129">If necessary, extract source files from the module by doing one or more of the following:</span></span>
    -   <span data-ttu-id="2957a-130">Используйте [**екстрактфилес**](merge-extractfiles.md) или [**екстрактфилесекс**](merge-extractfilesex.md) для извлечения файлов из внедренного CAB-файла, а затем скопируйте в указанный каталог.</span><span class="sxs-lookup"><span data-stu-id="2957a-130">Use [**ExtractFiles**](merge-extractfiles.md) or [**ExtractFilesEx**](merge-extractfilesex.md) to extract files from an embedded .cab file and then copy into a specified directory.</span></span>
        > [!Note]  
        > <span data-ttu-id="2957a-131">Для [**екстрактфилесекс**](merge-extractfilesex.md) требуется [Mergemod.dll версии 2,0](merge-module-automation.md) или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2957a-131">[**ExtractFilesEx**](merge-extractfilesex.md) requires [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         

    -   <span data-ttu-id="2957a-132">Используйте [**екстракткаб**](merge-extractcab.md) для извлечения файлов из внедренного CAB-файла, а затем сохраните в указанном файле.</span><span class="sxs-lookup"><span data-stu-id="2957a-132">Use [**ExtractCAB**](merge-extractcab.md) to extract files from an embedded .cab file, and then save in a specified file.</span></span>
    -   <span data-ttu-id="2957a-133">Используйте [**креатесаурцеимаже**](merge-createsourceimage.md) для извлечения файлов из модуля, а затем после слияния скопируйте в исходное изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="2957a-133">Use [**CreateSourceImage**](merge-createsourceimage.md) to extract files from a module, and then after the merge, copy to a source image on disk.</span></span>
        > [!Note]  
        > <span data-ttu-id="2957a-134">[**Креатесаурцеимаже**](merge-createsourceimage.md) доступен только в [Mergemod.dll версии 2,0](merge-module-automation.md) или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2957a-134">[**CreateSourceImage**](merge-createsourceimage.md) is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         
8.  <span data-ttu-id="2957a-135">Закройте текущий открытый модуль слияния с помощью метода [**клосемодуле**](merge-closemodule.md) .</span><span class="sxs-lookup"><span data-stu-id="2957a-135">Close the current open merge module by using the [**CloseModule**](merge-closemodule.md) method.</span></span>

    <span data-ttu-id="2957a-136">Этот шаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2957a-136">This step is required.</span></span>

9.  <span data-ttu-id="2957a-137">Закройте открытую базу данных установки с помощью метода [**клоседатабасе**](merge-closedatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="2957a-137">Close the open installation database by using the [**CloseDatabase**](merge-closedatabase.md) method.</span></span>

    <span data-ttu-id="2957a-138">Этот шаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2957a-138">This step is required.</span></span>

    <span data-ttu-id="2957a-139">При закрытии базы данных удаляются все сведения о зависимостях, но не затрагиваются все ошибки, которые не извлекаются.</span><span class="sxs-lookup"><span data-stu-id="2957a-139">Closing a database clears all dependency information, but does not affect any errors that are not retrieved.</span></span>

10. <span data-ttu-id="2957a-140">Закройте текущий файл журнала с помощью метода [**клоселог**](merge-closelog.md) .</span><span class="sxs-lookup"><span data-stu-id="2957a-140">Close the current log file by using the [**CloseLog**](merge-closelog.md) method.</span></span>

    <span data-ttu-id="2957a-141">Этот шаг необходим, если открыт файл журнала.</span><span class="sxs-lookup"><span data-stu-id="2957a-141">This step is required if you have an open log file.</span></span>

<span data-ttu-id="2957a-142">После слияния модуля с базой данных с помощью [Mergemod.dll](merge-module-automation.md)необходимо обновить [таблицу мультимедиа](media-table.md) , чтобы описать нужный макет исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="2957a-142">After the module has been merged into the database using [Mergemod.dll](merge-module-automation.md), the [Media Table](media-table.md) must be updated to describe the desired source image layout.</span></span> <span data-ttu-id="2957a-143">Процесс слияния, предоставляемый Mergemod.dll, не обновляет таблицу мультимедиа, так как потребитель модуля слияния может выбрать различные способы размещения исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="2957a-143">The merge process provided by Mergemod.dll does not update the Media Table because the consumer of the merge module can select various ways to layout the source image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2957a-144">См. также</span><span class="sxs-lookup"><span data-stu-id="2957a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2957a-145">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="2957a-145">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



