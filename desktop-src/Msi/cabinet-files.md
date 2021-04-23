---
description: CAB — это один файл, обычно с расширением CAB, в котором хранятся сжатые файлы в библиотеке файлов.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: CAB-файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662915"
---
# <a name="cabinet-files"></a><span data-ttu-id="bf237-103">CAB-файлы</span><span class="sxs-lookup"><span data-stu-id="bf237-103">Cabinet Files</span></span>

<span data-ttu-id="bf237-104">CAB — это один файл, обычно с расширением CAB, в котором хранятся сжатые файлы в библиотеке файлов.</span><span class="sxs-lookup"><span data-stu-id="bf237-104">A cabinet is a single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="bf237-105">Формат CAB является эффективным способом упаковки нескольких файлов, так как сжатие выполняется через границы файлов, что значительно улучшает степень сжатия.</span><span class="sxs-lookup"><span data-stu-id="bf237-105">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, which significantly improves the compression ratio.</span></span>

<span data-ttu-id="bf237-106">Разработчики могут использовать средство создания CAB-файлов, например Makecab.exe, чтобы сделать CAB-файлы для использования с пакетами установщика.</span><span class="sxs-lookup"><span data-stu-id="bf237-106">Developers can use a cabinet file creation tool such as Makecab.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="bf237-107">Служебная программа Makecab.exe входит в состав [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="bf237-107">The Makecab.exe utility is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="bf237-108">Разработчики также могут использовать средство создания CAB-файлов, например Cabarc.exe, чтобы сделать CAB-файлы для использования с пакетами установщика.</span><span class="sxs-lookup"><span data-stu-id="bf237-108">Developers can also use a cabinet file creation tool such as Cabarc.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="bf237-109">Это средство выполняет запись в структуру CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="bf237-109">This tool writes to the Diamond cabinet structure.</span></span>

<span data-ttu-id="bf237-110">Ключи файлов, хранящиеся в CAB-файле, должны соответствовать записям в столбце file [таблицы File](file-table.md) , а последовательность файлов в CAB-файле должна соответствовать последовательности файлов, указанной в столбце Sequence.</span><span class="sxs-lookup"><span data-stu-id="bf237-110">The file keys of the files stored inside of a cabinet file must match the entries in the File column of the [File table](file-table.md) and the sequence of files in the cabinet must match the file sequence specified in the Sequence column.</span></span> <span data-ttu-id="bf237-111">Дополнительные сведения см. [в разделе Использование ящиков и сжатых источников](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="bf237-111">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="bf237-112">Большие файлы можно разделить между двумя или более CAB-файлами.</span><span class="sxs-lookup"><span data-stu-id="bf237-112">Large files can be split between two or more cabinet files.</span></span> <span data-ttu-id="bf237-113">В одном CAB-файле может быть не более 15 файлов, охватывающих следующий CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="bf237-113">There can be no more than 15 files in any one cabinet file that spans to the next cabinet file.</span></span> <span data-ttu-id="bf237-114">Например, если у вас есть три CAB-файла, первый шкаф может иметь 15 файлов, которые охватывают второй CAB-файл, а второй CAB-файл может содержать 15 файлов, охватывающих третий CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="bf237-114">For example, if you have three cabinet files the first cabinet can have 15 files that span to the second cabinet file and the second cabinet file can have 15 files that span to the third cabinet file.</span></span>

<span data-ttu-id="bf237-115">Установщик извлекает файлы из CAB-файла, так как они необходимы для установки, и устанавливает их в том же порядке, в котором они хранятся в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="bf237-115">The installer extracts files from a cabinet as they are needed by the installation and installs them in the same order as they are stored in the cabinet file.</span></span> <span data-ttu-id="bf237-116">Требования к месту на диске для установки файла, хранящегося в CAB-файле, не отличаются от требований к установке несжатого файла.</span><span class="sxs-lookup"><span data-stu-id="bf237-116">The space requirements for installing a file stored in a cabinet are no different than for installing an uncompressed file.</span></span>

<span data-ttu-id="bf237-117">CAB-файл может находиться внутри или вне MSI-файла.</span><span class="sxs-lookup"><span data-stu-id="bf237-117">A cabinet file can be located inside or outside of the .msi file.</span></span> <span data-ttu-id="bf237-118">Начиная с установщик Windows 5,0, работающих в Windows 7 или Windows Server 2008 R2, установщик сохраняет все CAB, внедренные в MSI, перед кэшированием пакета установки.</span><span class="sxs-lookup"><span data-stu-id="bf237-118">Beginning with Windows Installer 5.0 running on Windows 7 or Windows Server 2008 R2 the installer saves any cabinets that are embedded in the .msi file before caching the installation package.</span></span>

<span data-ttu-id="bf237-119">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Чтобы сэкономить место на диске, установщик всегда удаляет все ящики, внедренные в MSI-файл, перед кэшированием пакета установки на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf237-119">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** To conserve disk space, the installer always removes any cabinets that are embedded in the .msi file before caching the installation package on the user's computer.</span></span>

 

 



