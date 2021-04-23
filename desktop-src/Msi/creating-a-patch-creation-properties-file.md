---
description: Чтобы воспроизвести образец пакета исправлений, требуется программное средство для создания и редактирования пакета исправлений установщик Windows.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Создание файла свойств для создания исправления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664666"
---
# <a name="creating-a-patch-creation-properties-file"></a><span data-ttu-id="8d250-103">Создание файла свойств для создания исправления</span><span class="sxs-lookup"><span data-stu-id="8d250-103">Creating a Patch Creation Properties File</span></span>

<span data-ttu-id="8d250-104">Чтобы воспроизвести образец пакета исправлений, требуется программное средство для создания и редактирования пакета исправлений установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="8d250-104">To reproduce the sample patch package, you need a software tool capable of creating and editing a Windows Installer patch package.</span></span> <span data-ttu-id="8d250-105">Несколько средств создания пакетов исправлений доступны у независимых поставщиков программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="8d250-105">Several patch package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="8d250-106">В примере, описанном в следующих разделах, используется редактор базы данных установщик Windows с именем Orca, который позволяет создать файл свойств создания исправлений (расширение PCP).</span><span class="sxs-lookup"><span data-stu-id="8d250-106">The example discussed in the following sections uses a Windows Installer database editor called Orca to author a patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="8d250-107">Файл с расширением PCP можно использовать с служебными программами [Msimsp.exe](msimsp-exe.md) и [Patchwiz.dll](patchwiz-dll.md) для создания пакета исправлений установщик Windows (MSP).</span><span class="sxs-lookup"><span data-stu-id="8d250-107">The .pcp file may be used with the utilities [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate a Windows Installer patch package (.msp extension).</span></span> <span data-ttu-id="8d250-108">Orca, Msimsp.exe и Patchwiz.dll предоставляются в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="8d250-108">Orca, Msimsp.exe, and Patchwiz.dll are provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="8d250-109">Пустой файл свойств создания исправления Template. PCP также предоставляется вместе с пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="8d250-109">A blank patch creation properties file, template.pcp, is also provided with the SDK.</span></span> <span data-ttu-id="8d250-110">Создайте копию Template. PCP и переименуйте эту копию MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="8d250-110">Make a copy of template.pcp and rename this copy MNP2000.pcp.</span></span> <span data-ttu-id="8d250-111">Используйте Orca или другой редактор базы данных для ввода следующих данных в таблицу свойств MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="8d250-111">Use Orca or another database editor to enter the following data into the Properties table of MNP2000.pcp.</span></span> <span data-ttu-id="8d250-112">В таблице свойств содержатся глобальные параметры для пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="8d250-112">The Properties table contains global settings for the patch package.</span></span>

[<span data-ttu-id="8d250-113">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="8d250-113">Properties Table</span></span>](properties-table-patchwiz-dll-.md)



| <span data-ttu-id="8d250-114">Имя</span><span class="sxs-lookup"><span data-stu-id="8d250-114">Name</span></span>                               | <span data-ttu-id="8d250-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8d250-115">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="8d250-116">алловпродукткодемисматчес</span><span class="sxs-lookup"><span data-stu-id="8d250-116">AllowProductCodeMismatches</span></span>         | <span data-ttu-id="8d250-117">1</span><span class="sxs-lookup"><span data-stu-id="8d250-117">1</span></span>                                      |
| <span data-ttu-id="8d250-118">алловпродуктверсионмажормисматчес</span><span class="sxs-lookup"><span data-stu-id="8d250-118">AllowProductVersionMajorMismatches</span></span> | <span data-ttu-id="8d250-119">1</span><span class="sxs-lookup"><span data-stu-id="8d250-119">1</span></span>                                      |
| <span data-ttu-id="8d250-120">апипатчингсимболфлагс</span><span class="sxs-lookup"><span data-stu-id="8d250-120">ApiPatchingSymbolFlags</span></span>             | <span data-ttu-id="8d250-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d250-121">0x00000000</span></span>                             |
| <span data-ttu-id="8d250-122">донтремоветемпфолдервхенфинишед</span><span class="sxs-lookup"><span data-stu-id="8d250-122">DontRemoveTempFolderWhenFinished</span></span>   | <span data-ttu-id="8d250-123">1</span><span class="sxs-lookup"><span data-stu-id="8d250-123">1</span></span>                                      |
| <span data-ttu-id="8d250-124">инклудевхолефилесонли</span><span class="sxs-lookup"><span data-stu-id="8d250-124">IncludeWholeFilesOnly</span></span>              | <span data-ttu-id="8d250-125">0</span><span class="sxs-lookup"><span data-stu-id="8d250-125">0</span></span>                                      |
| <span data-ttu-id="8d250-126">листофпатчгуидстореплаце</span><span class="sxs-lookup"><span data-stu-id="8d250-126">ListOfPatchGUIDsToReplace</span></span>          |                                        |
| <span data-ttu-id="8d250-127">листофтаржетпродукткодес</span><span class="sxs-lookup"><span data-stu-id="8d250-127">ListOfTargetProductCodes</span></span>           | \*                                     |
| <span data-ttu-id="8d250-128">патчгуид</span><span class="sxs-lookup"><span data-stu-id="8d250-128">PatchGUID</span></span>                          | <span data-ttu-id="8d250-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span><span class="sxs-lookup"><span data-stu-id="8d250-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span></span> |
| <span data-ttu-id="8d250-130">патчаутпутпас</span><span class="sxs-lookup"><span data-stu-id="8d250-130">PatchOutputPath</span></span>                    | <span data-ttu-id="8d250-131">c: \\ Output. MSP</span><span class="sxs-lookup"><span data-stu-id="8d250-131">c:\\output.msp</span></span>                         |
| <span data-ttu-id="8d250-132">патчсаурцелист</span><span class="sxs-lookup"><span data-stu-id="8d250-132">PatchSourceList</span></span>                    | <span data-ttu-id="8d250-133">патчсаурцелист</span><span class="sxs-lookup"><span data-stu-id="8d250-133">PatchSourceList</span></span>                        |



 

<span data-ttu-id="8d250-134">Используйте редактор базы данных для ввода следующих данных в таблицу Имажефамилиес MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="8d250-134">Use the database editor to enter the following data into the ImageFamilies table of MNP2000.pcp.</span></span> <span data-ttu-id="8d250-135">Таблица Имажефамилиес содержит сведения, которые будут добавлены в [таблицу мультимедиа](media-table.md) во время установки исправлений.</span><span class="sxs-lookup"><span data-stu-id="8d250-135">The ImageFamilies table contains information to be added to the [Media table](media-table.md) during patching.</span></span>

[<span data-ttu-id="8d250-136">Таблица Имажефамилиес</span><span class="sxs-lookup"><span data-stu-id="8d250-136">ImageFamilies Table</span></span>](imagefamilies-table-patchwiz-dll-.md)



| <span data-ttu-id="8d250-137">Семейство</span><span class="sxs-lookup"><span data-stu-id="8d250-137">Family</span></span>  | <span data-ttu-id="8d250-138">медиасркпропнаме</span><span class="sxs-lookup"><span data-stu-id="8d250-138">MediaSrcPropName</span></span> | <span data-ttu-id="8d250-139">медиадискид</span><span class="sxs-lookup"><span data-stu-id="8d250-139">MediaDiskId</span></span> | <span data-ttu-id="8d250-140">филесекуенцестарт</span><span class="sxs-lookup"><span data-stu-id="8d250-140">FileSequenceStart</span></span> | <span data-ttu-id="8d250-141">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="8d250-141">DiskPrompt</span></span> | <span data-ttu-id="8d250-142">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="8d250-142">VolumeLabel</span></span> |
|---------|------------------|-------------|-------------------|------------|-------------|
| <span data-ttu-id="8d250-143">мнпаппс</span><span class="sxs-lookup"><span data-stu-id="8d250-143">MNPapps</span></span> | <span data-ttu-id="8d250-144">мнпсркпропнаме</span><span class="sxs-lookup"><span data-stu-id="8d250-144">MNPSrcPropName</span></span>   | <span data-ttu-id="8d250-145">2</span><span class="sxs-lookup"><span data-stu-id="8d250-145">2</span></span>           | <span data-ttu-id="8d250-146">1000</span><span class="sxs-lookup"><span data-stu-id="8d250-146">1000</span></span>              |            |             |



 

<span data-ttu-id="8d250-147">Введите следующие данные в таблицу Упградедимажес MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="8d250-147">Enter the following data into the UpgradedImages table of MNP2000.pcp.</span></span> <span data-ttu-id="8d250-148">Таблица Упградедимажес содержит сведения о обновленном образе, созданном при [планировании небольшого обновления](planning-a-small-update-patch.md).</span><span class="sxs-lookup"><span data-stu-id="8d250-148">The UpgradedImages table contains information about the Upgraded image you created in [Planning a Small Update Patch](planning-a-small-update-patch.md).</span></span>

[<span data-ttu-id="8d250-149">Таблица Упградедимажес</span><span class="sxs-lookup"><span data-stu-id="8d250-149">UpgradedImages Table</span></span>](upgradedimages-table-patchwiz-dll-.md)



| <span data-ttu-id="8d250-150">Обновлено</span><span class="sxs-lookup"><span data-stu-id="8d250-150">Upgraded</span></span>   | <span data-ttu-id="8d250-151">мсипас</span><span class="sxs-lookup"><span data-stu-id="8d250-151">MsiPath</span></span>                                           | <span data-ttu-id="8d250-152">патчмсипас</span><span class="sxs-lookup"><span data-stu-id="8d250-152">PatchMsiPath</span></span> | <span data-ttu-id="8d250-153">симболпасс</span><span class="sxs-lookup"><span data-stu-id="8d250-153">SymbolPaths</span></span> | <span data-ttu-id="8d250-154">Семейство</span><span class="sxs-lookup"><span data-stu-id="8d250-154">Family</span></span>  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| <span data-ttu-id="8d250-155">MNP \_ фиксированный</span><span class="sxs-lookup"><span data-stu-id="8d250-155">MNP\_fixed</span></span> | <span data-ttu-id="8d250-156">В. \\ Примечание. обновление \_ установщика \\ \\ Обновлено \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="8d250-156">C:\\Note\_Installer\\Patch\\Upgraded\\MNP2000.msi</span></span> |              |             | <span data-ttu-id="8d250-157">мнпаппс</span><span class="sxs-lookup"><span data-stu-id="8d250-157">MNPapps</span></span> |



 

<span data-ttu-id="8d250-158">Введите следующие данные в таблицу Таржетимажес MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="8d250-158">Enter the following data into the TargetImages table of MNP2000.pcp.</span></span> <span data-ttu-id="8d250-159">Таблица Таржетимажес содержит сведения о целевом образе.</span><span class="sxs-lookup"><span data-stu-id="8d250-159">The TargetImages table contains information about the Target image.</span></span>

[<span data-ttu-id="8d250-160">Таблица Таржетимажес</span><span class="sxs-lookup"><span data-stu-id="8d250-160">TargetImages Table</span></span>](targetimages-table-patchwiz-dll-.md)



| <span data-ttu-id="8d250-161">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="8d250-161">Target</span></span>     | <span data-ttu-id="8d250-162">мсипас</span><span class="sxs-lookup"><span data-stu-id="8d250-162">MsiPath</span></span>                                         | <span data-ttu-id="8d250-163">симболпасс</span><span class="sxs-lookup"><span data-stu-id="8d250-163">SymbolPaths</span></span> | <span data-ttu-id="8d250-164">Обновлено</span><span class="sxs-lookup"><span data-stu-id="8d250-164">Upgraded</span></span>   | <span data-ttu-id="8d250-165">Заказ</span><span class="sxs-lookup"><span data-stu-id="8d250-165">Order</span></span> | <span data-ttu-id="8d250-166">продуктвалидатефлагс</span><span class="sxs-lookup"><span data-stu-id="8d250-166">ProductValidateFlags</span></span> | <span data-ttu-id="8d250-167">игноремиссингсркфилес</span><span class="sxs-lookup"><span data-stu-id="8d250-167">IgnoreMissingSrcFiles</span></span> |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| <span data-ttu-id="8d250-168">\_Ошибка MNP</span><span class="sxs-lookup"><span data-stu-id="8d250-168">MNP\_error</span></span> | <span data-ttu-id="8d250-169">В. \\ Примечание \_ . \\ \\ целевой объект исправления установщика \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="8d250-169">C:\\Note\_Installer\\Patch\\Target\\MNP2000.msi</span></span> |             | <span data-ttu-id="8d250-170">MNP \_ фиксированный</span><span class="sxs-lookup"><span data-stu-id="8d250-170">MNP\_fixed</span></span> | <span data-ttu-id="8d250-171">1</span><span class="sxs-lookup"><span data-stu-id="8d250-171">1</span></span>     |                      | <span data-ttu-id="8d250-172">0</span><span class="sxs-lookup"><span data-stu-id="8d250-172">0</span></span>                     |



 

<span data-ttu-id="8d250-173">Для примера пакета исправлений оставьте пустыми следующие таблицы в MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="8d250-173">For the sample patch package, leave the following tables in MNP2000.pcp blank.</span></span>

[<span data-ttu-id="8d250-174">\_Таблица Оптионалдата упградедфилес</span><span class="sxs-lookup"><span data-stu-id="8d250-174">UpgradedFiles\_OptionalData Table</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="8d250-175">Таблица Фамилифилеранжес</span><span class="sxs-lookup"><span data-stu-id="8d250-175">FamilyFileRanges Table</span></span>](familyfileranges-table-patchwiz-dll-.md)

[<span data-ttu-id="8d250-176">\_Таблица Оптионалдата таржетфилес</span><span class="sxs-lookup"><span data-stu-id="8d250-176">TargetFiles\_OptionalData Table</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="8d250-177">Таблица Екстерналфилес</span><span class="sxs-lookup"><span data-stu-id="8d250-177">ExternalFiles Table</span></span>](externalfiles-table-patchwiz-dll-.md)

[<span data-ttu-id="8d250-178">Таблица Упградедфилестоигноре</span><span class="sxs-lookup"><span data-stu-id="8d250-178">UpgradedFilesToIgnore Table</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

[<span data-ttu-id="8d250-179">Продолжить</span><span class="sxs-lookup"><span data-stu-id="8d250-179">Continue</span></span>](generating-a-patch-package.md)

 

 



