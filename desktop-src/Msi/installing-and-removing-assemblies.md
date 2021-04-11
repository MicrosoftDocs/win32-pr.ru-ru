---
description: При установке сборки в изолированное расположение для конкретного приложения оно должно быть указано в \_ столбце Application File таблицы мсиассембли.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Установка и удаление сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272803"
---
# <a name="installing-and-removing-assemblies"></a><span data-ttu-id="f2d83-103">Установка и удаление сборок</span><span class="sxs-lookup"><span data-stu-id="f2d83-103">Installing and Removing Assemblies</span></span>

<span data-ttu-id="f2d83-104">При установке сборки в изолированное расположение для конкретного приложения оно должно быть указано в \_ столбце Application file [таблицы мсиассембли](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2d83-104">When installing an assembly to an isolated location for a specific application, the application must be specified in the File\_Application column of the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="f2d83-105">Это поле является ключом в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2d83-105">This field is a key into the [File table](file-table.md).</span></span> <span data-ttu-id="f2d83-106">Установщик использует структуру каталогов, указанную в [таблице Directory](directory-table.md) , для установки сборки в тот же каталог, что и компонент, содержащий этот файл.</span><span class="sxs-lookup"><span data-stu-id="f2d83-106">The installer uses the directory structure that is specified in the [Directory table](directory-table.md) to install the assembly into the same directory as the component that contains this file.</span></span>

<span data-ttu-id="f2d83-107">При установке сборки в глобальный кэш сборок значение в \_ столбце Application file [таблицы мсиассембли](msiassembly-table.md) должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="f2d83-107">When installing an assembly to the global assembly cache, the value in the File\_Application column of the [MsiAssembly Table](msiassembly-table.md) must be Null.</span></span>

<span data-ttu-id="f2d83-108">В следующих разделах описывается установка Win32 и сборок среды CLR.</span><span class="sxs-lookup"><span data-stu-id="f2d83-108">The following sections describe the installation of Win32 and common language runtime assemblies:</span></span>

-   [<span data-ttu-id="f2d83-109">Установка сборок Win32</span><span class="sxs-lookup"><span data-stu-id="f2d83-109">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)
-   [<span data-ttu-id="f2d83-110">Установка сборок среды CLR</span><span class="sxs-lookup"><span data-stu-id="f2d83-110">Installation of Common Language Runtime Assemblies</span></span>](installation-of-common-language-runtime-assemblies.md)

 

 



