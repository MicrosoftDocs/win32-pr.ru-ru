---
description: Разработчики создают пакет исправлений, создавая файл создания исправления и используя Msimsp.exe для вызова функции Уикреатепатчпаккажеекс в Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Создание пакета исправлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264858"
---
# <a name="creating-a-patch-package"></a><span data-ttu-id="b3505-103">Создание пакета исправлений</span><span class="sxs-lookup"><span data-stu-id="b3505-103">Creating a Patch Package</span></span>

<span data-ttu-id="b3505-104">Разработчики создают пакет исправлений, создавая файл создания исправления и используя [Msimsp.exe](msimsp-exe.md) для вызова функции [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) в [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="b3505-104">Developers create a patch package by generating a patch creation file and using [Msimsp.exe](msimsp-exe.md) to call the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="b3505-105">Msimsp.exe и Patchwiz.dll предоставляются в пакете SDK для установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="b3505-105">Msimsp.exe and Patchwiz.dll are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="b3505-106">Дополнительные сведения см. [в разделе Пример исправления небольшого обновления](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="b3505-106">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="b3505-107">Поскольку применение исправления к пакету установщик Windows приводит к установке исходных источников с помощью нового MSI-файла, новый MSI-файл должен быть совместим с макетом исходного источника.</span><span class="sxs-lookup"><span data-stu-id="b3505-107">Because the application of a patch to a Windows Installer package results in the installation of the original sources using a new .msi file, the new .msi file must remain compatible with the layout of the original source.</span></span>

<span data-ttu-id="b3505-108">При создании пакета исправлений необходимо использовать образ установки без сжатия, чтобы создать исправление, например административный образ или образ установки без сжатия с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="b3505-108">When you author a patch package you must use an uncompressed setup image to create a patch, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="b3505-109">Необходимо также соблюдать следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="b3505-109">You must also adhere to the following restrictions:</span></span>

-   <span data-ttu-id="b3505-110">Не переносите файлы из одной папки в другую.</span><span class="sxs-lookup"><span data-stu-id="b3505-110">Do not move files from one folder to another.</span></span>
-   <span data-ttu-id="b3505-111">Не переносите файлы из одного CAB-файла в другой.</span><span class="sxs-lookup"><span data-stu-id="b3505-111">Do not move files from one cabinet to another.</span></span>
-   <span data-ttu-id="b3505-112">Не изменяйте порядок файлов в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="b3505-112">Do not change the order of files in a cabinet.</span></span>
-   <span data-ttu-id="b3505-113">Не изменяйте порядковый номер существующих файлов.</span><span class="sxs-lookup"><span data-stu-id="b3505-113">Do not change the sequence number of existing files.</span></span> <span data-ttu-id="b3505-114">Порядковый номер — это значение, указанное в столбце Sequence [таблицы File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="b3505-114">The sequence number is the value specified in the Sequence column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="b3505-115">Все новые файлы, добавленные исправлением, должны быть помещены в конец существующей последовательности файлов.</span><span class="sxs-lookup"><span data-stu-id="b3505-115">Any new files that are added by the patch must be placed at the end of the existing file sequence.</span></span> <span data-ttu-id="b3505-116">Порядковый номер нового файла в обновленном образе должен быть больше, чем самый крупный порядковый номер существующих файлов в целевом образе.</span><span class="sxs-lookup"><span data-stu-id="b3505-116">The sequence number of any new file in the upgraded image must be greater than the largest sequence number of existing files in the target image.</span></span>
-   <span data-ttu-id="b3505-117">Не изменяйте первичные ключи в [таблице файлов](file-table.md) между исходной и новой версией MSI файла.</span><span class="sxs-lookup"><span data-stu-id="b3505-117">Do not change the primary keys in the [File Table](file-table.md) between the original and new .msi file versions.</span></span>
    > [!Note]  
    > <span data-ttu-id="b3505-118">Файл должен иметь тот же ключ в [таблице файлов](file-table.md) целевого и обновленного образа.</span><span class="sxs-lookup"><span data-stu-id="b3505-118">The file must have the same key in the [File Table](file-table.md) of both the target image and the updated image.</span></span> <span data-ttu-id="b3505-119">Строковые значения в столбце File обеих таблиц должны быть идентичными, включая регистр.</span><span class="sxs-lookup"><span data-stu-id="b3505-119">The string values in the File column of both tables must be identical, including the case.</span></span>

     

-   <span data-ttu-id="b3505-120">Не создавайте пакет с ключами [таблицы файлов](file-table.md) , отличающимися только регистром, например, не используйте следующий пример таблицы.</span><span class="sxs-lookup"><span data-stu-id="b3505-120">Do not author a package with [File Table](file-table.md) keys that differ only in case, for example, avoid the following table example.</span></span>

    

    | <span data-ttu-id="b3505-121">Файл</span><span class="sxs-lookup"><span data-stu-id="b3505-121">File</span></span>       | <span data-ttu-id="b3505-122">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="b3505-122">Component\_</span></span> | <span data-ttu-id="b3505-123">FileName</span><span class="sxs-lookup"><span data-stu-id="b3505-123">FileName</span></span>   |
    |------------|-------------|------------|
    | <span data-ttu-id="b3505-124">readMe.txt</span><span class="sxs-lookup"><span data-stu-id="b3505-124">readme.txt</span></span> | <span data-ttu-id="b3505-125">Comp1</span><span class="sxs-lookup"><span data-stu-id="b3505-125">Comp1</span></span>       | <span data-ttu-id="b3505-126">readMe.txt</span><span class="sxs-lookup"><span data-stu-id="b3505-126">readme.txt</span></span> |
    | <span data-ttu-id="b3505-127">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="b3505-127">ReadMe.txt</span></span> | <span data-ttu-id="b3505-128">Comp2</span><span class="sxs-lookup"><span data-stu-id="b3505-128">Comp2</span></span>       | <span data-ttu-id="b3505-129">readMe.txt</span><span class="sxs-lookup"><span data-stu-id="b3505-129">readme.txt</span></span> |

    

     

    <span data-ttu-id="b3505-130">Установщик Windows может разрешить предыдущий пример таблицы, если comp1 и Comp2 установлены в разных каталогах, но для создания исправления для пакета нельзя использовать [Msimsp.exe](msimsp-exe.md) или [Patchwiz.dll](patchwiz-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="b3505-130">The Windows Installer can allow the previous table example when Comp1 and Comp2 are installed on different directories, but then you cannot use [Msimsp.exe](msimsp-exe.md) or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package.</span></span> <span data-ttu-id="b3505-131">Msimsp.exe и Patchwiz.dll вызывают Makecab.exe, что не учитывает регистр и завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b3505-131">Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive and fails.</span></span>

    <span data-ttu-id="b3505-132">При использовании модулей слияния в программе установки убедитесь, что порядковые номера и структура файлов соответствуют приведенным выше рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="b3505-132">When using merge modules in the setup, ensure that file sequence numbers and layout adhere to the above guidelines.</span></span>

 

 



