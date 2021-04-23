---
description: Для создания пакета исправлений рекомендуется использовать средство создания исправлений, например Msimsp.exe и Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272785"
---
# <a name="patchwizdll"></a><span data-ttu-id="7c9ce-103">Patchwiz.dll</span><span class="sxs-lookup"><span data-stu-id="7c9ce-103">Patchwiz.dll</span></span>

<span data-ttu-id="7c9ce-104">Для создания пакета исправлений рекомендуется использовать средство создания исправлений, например [Msimsp.exe](msimsp-exe.md) и Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-104">To generate a patch package, it is recommended that you use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and Patchwiz.dll.</span></span> <span data-ttu-id="7c9ce-105">Patchwiz.dll версии 4,0 совместима с пакетами и исправлениями, созданными в более ранних версиях Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-105">Patchwiz.dll version 4.0 is compatible with packages and patches that were authored using earlier versions of the Patchwiz.dll.</span></span> <span data-ttu-id="7c9ce-106">Средство Patchwiz.dll доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="7c9ce-106">The Patchwiz.dll tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="7c9ce-107">В Patchwiz.dll версии 4,0 имеется одна новая функция [уикреатепатчпаккажеекс (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), которая расширяет функциональные возможности [уикреатепатчпаккаже (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="7c9ce-107">Patchwiz.dll version 4.0 has one new function, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), that extends the functionality of [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span></span> <span data-ttu-id="7c9ce-108">Эти функции принимают файл свойств создания исправления (PCP-файл) и создают [пакет исправлений](patch-packages.md)установщика.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-108">These functions take a patch creation properties file (.pcp file) and generate an installer [Patch Package](patch-packages.md).</span></span>

<span data-ttu-id="7c9ce-109">PCP-файл представляет собой двоичный файл базы данных с тем же форматом, что и база данных установщик Windows (MSI-файл), но с другой схемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-109">The .pcp file is a binary database file with the same format as a Windows Installer database (.msi file), but with a different database schema.</span></span> <span data-ttu-id="7c9ce-110">Поэтому PCP-файл можно создать с помощью тех же средств, которые используются для базы данных установщика.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-110">Therefore a .pcp file can be authored by using the same tools used for an installer database.</span></span>

<span data-ttu-id="7c9ce-111">Вы можете создать PCP-файл с помощью редактора таблиц, например [Orca.exe](orca-exe.md) , чтобы ввести данные в пустую базу данных PCP, которая поставляется с пакетом SDK для установщик Windows, Template. PCP.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-111">You can create a .pcp file by using a table editor such as [Orca.exe](orca-exe.md) to enter information into the blank .pcp database provided with the Windows Installer SDK, Template.pcp.</span></span> <span data-ttu-id="7c9ce-112">Дополнительные сведения см. [в разделе Пример исправления небольшого обновления](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="7c9ce-112">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="7c9ce-113">В каждом файле. PCP необходимы следующие таблицы базы данных:</span><span class="sxs-lookup"><span data-stu-id="7c9ce-113">The following database tables are required in every .pcp file:</span></span>

-   [<span data-ttu-id="7c9ce-114">Таблица свойств (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-114">Properties Table (Patchwiz.dll)</span></span>](properties-table-patchwiz-dll-.md)
-   [<span data-ttu-id="7c9ce-115">Таблица Имажефамилиес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-115">ImageFamilies Table (Patchwiz.dll)</span></span>](imagefamilies-table-patchwiz-dll-.md)
-   [<span data-ttu-id="7c9ce-116">Таблица Упградедимажес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-116">UpgradedImages Table (Patchwiz.dll)</span></span>](upgradedimages-table-patchwiz-dll-.md)
-   [<span data-ttu-id="7c9ce-117">Таблица Таржетимажес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-117">TargetImages Table (Patchwiz.dll)</span></span>](targetimages-table-patchwiz-dll-.md)

<span data-ttu-id="7c9ce-118">Следующие таблицы базы данных являются необязательными:</span><span class="sxs-lookup"><span data-stu-id="7c9ce-118">The following database tables are optional:</span></span>

-   [<span data-ttu-id="7c9ce-119">\_Таблица Оптионалдата упградедфилес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-119">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="7c9ce-120">Таблица Фамилифилеранжес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-120">FamilyFileRanges Table (Patchwiz.dll)</span></span>](familyfileranges-table-patchwiz-dll-.md)
-   [<span data-ttu-id="7c9ce-121">\_Таблица Оптионалдата таржетфилес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-121">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="7c9ce-122">Таблица Екстерналфилес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-122">ExternalFiles Table (Patchwiz.dll)</span></span>](externalfiles-table-patchwiz-dll-.md)
-   [<span data-ttu-id="7c9ce-123">Таблица Упградедфилестоигноре (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-123">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

<span data-ttu-id="7c9ce-124">В PCP-файлах, имеющих Минимумрекуиредмсиверсион, равный 300 в таблице [свойств](properties-table-patchwiz-dll-.md) , требуется следующая таблица.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-124">The following table is required in .pcp files that have a MinimumRequiredMsiVersion equal to 300 in the [Properties](properties-table-patchwiz-dll-.md) table.</span></span>

-   [<span data-ttu-id="7c9ce-125">Таблица Патчметадата (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9ce-125">PatchMetadata Table (Patchwiz.dll)</span></span>](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> <span data-ttu-id="7c9ce-126">Таблица является необязательной, если Минимумрекуиредмсиверсион не равно 300.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-126">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

 

<span data-ttu-id="7c9ce-127">Версия Patchwiz.dll, выпущенная с установщик Windows 3,0, может автоматически формировать сведения о последовательности исправлений и добавлять их в [таблицу мсипатчсекуенце](msipatchsequence-table.md) нового исправления.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-127">The version of Patchwiz.dll released with Windows Installer 3.0 can automatically generate patch sequencing information and add it to the [MsiPatchSequence Table](msipatchsequence-table.md) of a new patch.</span></span> <span data-ttu-id="7c9ce-128">[Таблицу патчсекуенце](patchsequence-table--patchwiz-dll-.md) можно использовать для ручного добавления сведений о последовательности обновлений в таблицу мсипатчсекуенце.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-128">The [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) can be used to manually add patch sequencing information the MsiPatchSequence Table.</span></span> <span data-ttu-id="7c9ce-129">Дополнительные сведения см. в разделе [Создание сведений о последовательности исправления](generating-patch-sequence-information---patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="7c9ce-129">For more information, see [Generating Patch Sequence Information](generating-patch-sequence-information---patchwiz-dll-.md).</span></span>

<span data-ttu-id="7c9ce-130">Начиная с версии Patchwiz.dll 2,0, можно увеличить скорость последующего создания исправления с помощью [кэширования сведений об исправлениях (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="7c9ce-130">Beginning with Patchwiz.dll version 2.0, you can increase the speed of subsequent patch creation by using [Patch Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span></span>

<span data-ttu-id="7c9ce-131">Использование общедоступных символов для целевой платформы и двоичных файлов образа обновления позволяет сократить размер двоичного исправления примерно на одну половину.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-131">Using public symbols for your target and upgrade image binaries can reduce binary patch sizes by approximately one half.</span></span> <span data-ttu-id="7c9ce-132">Дополнительные сведения см. [в разделе Использование символов для сокращения размера двоичного исправления](using-symbols-to-reduce-binary-patch-size.md).</span><span class="sxs-lookup"><span data-stu-id="7c9ce-132">For more information, see [Using Symbols to Reduce Binary Patch Size](using-symbols-to-reduce-binary-patch-size.md).</span></span>

<span data-ttu-id="7c9ce-133">Можно указать, что определенные регионы целевого файла будут сохранены при установке исправлений, а сведения в этих регионах будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="7c9ce-133">You can specify that certain regions of the target file be preserved from being overwritten during patching and that the information in those regions be retained.</span></span> <span data-ttu-id="7c9ce-134">Дополнительные сведения см. в разделе [исправление выбранных регионов файла](patching-selected-regions-of-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="7c9ce-134">For more information, see [Patching Selected Regions of a File](patching-selected-regions-of-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c9ce-135">См. также</span><span class="sxs-lookup"><span data-stu-id="7c9ce-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c9ce-136">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="7c9ce-136">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



