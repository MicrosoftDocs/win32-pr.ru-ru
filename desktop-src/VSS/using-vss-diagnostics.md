---
description: Всдиагвиев и Вссажент — это средства, которые можно использовать для устранения неполадок приложений VSS. Примечание. Эти средства включены в пакет средств разработки программного обеспечения Microsoft Windows (SDK) для Windows Vista и более поздних версий.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Использование диагностики VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692390"
---
# <a name="using-vss-diagnostics"></a><span data-ttu-id="38940-103">Использование диагностики VSS</span><span class="sxs-lookup"><span data-stu-id="38940-103">Using VSS Diagnostics</span></span>

<span data-ttu-id="38940-104">Всдиагвиев и Вссажент — это средства, которые можно использовать для устранения неполадок приложений VSS.</span><span class="sxs-lookup"><span data-stu-id="38940-104">Vsdiagview and Vssagent are tools that you can use to troubleshoot VSS applications.</span></span>

> [!Note]  
> <span data-ttu-id="38940-105">Эти средства включены в пакет средств разработки программного обеспечения Microsoft Windows (SDK) для Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="38940-105">These tools are included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="38940-106">Вы можете скачать Windows SDK из [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="38940-106">You can download the Windows SDK from [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx).</span></span>

 

<span data-ttu-id="38940-107">В Windows SDK установки эти средства можно найти в `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (для 64-разрядной версии Windows) и `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (для 32-разрядной версии Windows).</span><span class="sxs-lookup"><span data-stu-id="38940-107">In the Windows SDK installation, these tools can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="gathering-data"></a><span data-ttu-id="38940-108">Идет сбор данных</span><span class="sxs-lookup"><span data-stu-id="38940-108">Gathering Data</span></span>

<span data-ttu-id="38940-109">Данные можно собирать с помощью команды Вссажент.</span><span class="sxs-lookup"><span data-stu-id="38940-109">You can gather data by using the Vssagent command.</span></span>

<span data-ttu-id="38940-110">**Сбор данных с помощью Вссажент**</span><span class="sxs-lookup"><span data-stu-id="38940-110">**To gather data using Vssagent**</span></span>

1.  <span data-ttu-id="38940-111">Чтобы собрать данные из командной строки, используйте команду Вссажент следующим образом:</span><span class="sxs-lookup"><span data-stu-id="38940-111">To gather data from the command line, use the Vssagent command as follows:</span></span>

    <span data-ttu-id="38940-112">**вссажент — сбор** *ксмлфиленаме \* \* *. XML**</span><span class="sxs-lookup"><span data-stu-id="38940-112">**vssagent -gather** *XmlFileName\*\*\*.xml*\*</span></span>

2.  <span data-ttu-id="38940-113">Чтобы просмотреть выходной файл, см. следующий раздел Просмотр данных.</span><span class="sxs-lookup"><span data-stu-id="38940-113">To view the output file, see the following Viewing Data section.</span></span>

## <a name="viewing-data"></a><span data-ttu-id="38940-114">Просмотр данных</span><span class="sxs-lookup"><span data-stu-id="38940-114">Viewing Data</span></span>

<span data-ttu-id="38940-115">Приложение Всдиагвиев можно использовать для просмотра данных, собранных с помощью команды Вссажент.</span><span class="sxs-lookup"><span data-stu-id="38940-115">The Vsdiagview application can be used to view data that was gathered by using the Vssagent command.</span></span> <span data-ttu-id="38940-116">Всдиагвиев отображает следующие сведения о компьютере:</span><span class="sxs-lookup"><span data-stu-id="38940-116">Vsdiagview displays the following information about the computer:</span></span>

-   <span data-ttu-id="38940-117">Сведения о компьютере, такие как версия операционной системы, общий объем доступной памяти и скорость ЦП</span><span class="sxs-lookup"><span data-stu-id="38940-117">Information about the computer, such as the operating system version, total available memory, and CPU speed</span></span>
-   <span data-ttu-id="38940-118">Имена и номера версий двоичных файлов VSS</span><span class="sxs-lookup"><span data-stu-id="38940-118">The names and version numbers of the VSS binaries</span></span>
-   <span data-ttu-id="38940-119">Имена и свойства дисков и устройств томов</span><span class="sxs-lookup"><span data-stu-id="38940-119">The names and properties of the disk and volume devices</span></span>
-   <span data-ttu-id="38940-120">Имена и свойства любых приложений COM+</span><span class="sxs-lookup"><span data-stu-id="38940-120">The names and properties of any COM+ applications</span></span>
-   <span data-ttu-id="38940-121">Имена журналов событий, которые можно использовать для диагностики проблем VSS</span><span class="sxs-lookup"><span data-stu-id="38940-121">The names of event logs that can be used for diagnosing VSS problems</span></span>
-   <span data-ttu-id="38940-122">Имена всех модулей записи VSS и обрабатываемых ими событий</span><span class="sxs-lookup"><span data-stu-id="38940-122">The names of any VSS writers and the events that they handle</span></span>
-   <span data-ttu-id="38940-123">Сведения о других файлах операционной системы</span><span class="sxs-lookup"><span data-stu-id="38940-123">Information about other operating system files</span></span>

<span data-ttu-id="38940-124">**Просмотр данных с помощью Всдиагвиев**</span><span class="sxs-lookup"><span data-stu-id="38940-124">**To view data using Vsdiagview**</span></span>

1.  <span data-ttu-id="38940-125">В меню Файл выберите **Открыть** , чтобы найти файл.</span><span class="sxs-lookup"><span data-stu-id="38940-125">In the File menu, choose **Open** to browse for a file.</span></span> <span data-ttu-id="38940-126">(Расположение по умолчанию — C: \\ вссдиаг.)</span><span class="sxs-lookup"><span data-stu-id="38940-126">(The default location is C:\\vssdiag.)</span></span>
2.  <span data-ttu-id="38940-127">Нажмите кнопку **Открыть** , чтобы просмотреть данные.</span><span class="sxs-lookup"><span data-stu-id="38940-127">Click **Open** to view the data.</span></span>

 

 



