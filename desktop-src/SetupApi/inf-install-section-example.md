---
description: Раздел Установка INF-файла определяет шаги процедуры установки.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Пример раздела установки INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663904"
---
# <a name="inf-install-section-example"></a><span data-ttu-id="e3dd7-103">Пример раздела установки INF-файла</span><span class="sxs-lookup"><span data-stu-id="e3dd7-103">INF Install Section Example</span></span>

<span data-ttu-id="e3dd7-104">Раздел **Установка** INF-файла определяет шаги процедуры установки.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-104">The **Install** section of an INF File defines the steps of the installation procedure.</span></span> <span data-ttu-id="e3dd7-105">Каждая строка раздела **установки** состоит из двух частей.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-105">Each line of an **Install** section has two parts.</span></span> <span data-ttu-id="e3dd7-106">В левой части знака равенства (=) находится ключ.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-106">On the left of the equals sign (=) is the key.</span></span> <span data-ttu-id="e3dd7-107">В правой части — это список из одного или нескольких заголовков разделов.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-107">On the right hand side, is a list of one or more section titles.</span></span> <span data-ttu-id="e3dd7-108">Ключ задает тип разделов, которые перечислены справа.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-108">The key specifies the type of the sections that are listed on the right.</span></span> <span data-ttu-id="e3dd7-109">Описание формата этого раздела см. в разделе "разделы и директивы INF-файлов" пакета средств разработки драйверов для Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-109">For a description of this section's format see the "INF File Sections and Directives" of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="e3dd7-110">Ниже приведен пример раздела **Install** .</span><span class="sxs-lookup"><span data-stu-id="e3dd7-110">The following is an example of an **Install** section.</span></span>

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

<span data-ttu-id="e3dd7-111">В этом примере для ключа **copyfiles** заданы значения "Files" и "ProgramFiles".</span><span class="sxs-lookup"><span data-stu-id="e3dd7-111">In this example the **CopyFiles** key is set to the values "DataFiles" and "ProgramFiles".</span></span> <span data-ttu-id="e3dd7-112">Этот параметр задает два раздела **копий файлов** в INF-файле, которые содержат имена исходных файлов, используемых операциями копирования.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-112">This specifies two **Copy Files** sections in the INF file that contain the names of the source files used by copying operations.</span></span> <span data-ttu-id="e3dd7-113">Место назначения для скопированных файлов задается в разделе **дестинатиондирс** в INF-файле.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-113">The destination for the copied files would be specified in a **DestinationDirs** section in the INF file.</span></span>

<span data-ttu-id="e3dd7-114">Ключу **делфилес** присваивается значение «олдфилес».</span><span class="sxs-lookup"><span data-stu-id="e3dd7-114">The **Delfiles** key is given the value "OldFiles".</span></span> <span data-ttu-id="e3dd7-115">Здесь указывается раздел **Удаление файлов** , содержащий сведения, относящиеся к операциям удаления файлов.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-115">This specifies a **Delete Files** section that contains information relevant to file deletion operations.</span></span>

<span data-ttu-id="e3dd7-116">Ключ **упдатеинис** указывает разделы **Update ini-файла** , содержащие сведения об обновлении записей в ini-файле.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-116">The **UpdateInis** key specifies **Update INI File** sections that contain information about updating entries in the INI file.</span></span>

<span data-ttu-id="e3dd7-117">Ключи **аддрег** и **делрег** указывают разделы реестра **Add** и **Delete** , содержащие сведения о добавлении или удалении данных реестра.</span><span class="sxs-lookup"><span data-stu-id="e3dd7-117">The **AddReg** and **DelReg** keys specify **Add Registry** and **Delete Registry** sections that contain information about adding or deleting registry information.</span></span>

 

 



