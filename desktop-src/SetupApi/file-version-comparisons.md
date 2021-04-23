---
description: Если \_ \_ во время операции копирования файла указан флаг "копия SP новее", то функции установки проверяют наличие существующей копии файла в целевом каталоге.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Сравнения версий файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9601dcef07afca81a3ffc64148b0c4f2492f935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664087"
---
# <a name="file-version-comparisons"></a><span data-ttu-id="32457-103">Сравнения версий файлов</span><span class="sxs-lookup"><span data-stu-id="32457-103">File Version Comparisons</span></span>

<span data-ttu-id="32457-104">Если \_ \_ во время операции копирования файла указан флаг "копия SP новее", то функции установки проверяют наличие существующей копии файла в целевом каталоге.</span><span class="sxs-lookup"><span data-stu-id="32457-104">If the SP\_COPY\_NEWER flag is specified during a file copy operation, the setup functions check for an existing copy of the file in the target directory.</span></span> <span data-ttu-id="32457-105">Если существующая копия найдена, функции сравнивают версии целевого и исходного файлов, чтобы определить, какой из них является более новым.</span><span class="sxs-lookup"><span data-stu-id="32457-105">If an existing copy is found, the functions compare the versions of the target and source file to determine which is newer.</span></span>

<span data-ttu-id="32457-106">Сведения о версии файла, используемые во время проверки версии, задаются в члене **двфилеверсионмс** и **двфилеверсионлс** структуры [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) , используемой функциями версии.</span><span class="sxs-lookup"><span data-stu-id="32457-106">The file version information used during version checks is that specified in the **dwFileVersionMS** and **dwFileVersionLS** members of a [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure, used by the version functions.</span></span> <span data-ttu-id="32457-107">Если в одном из файлов не указана версия ресурсов или они имеют одинаковые сведения о версии, исходный файл рассматривается как новый файл.</span><span class="sxs-lookup"><span data-stu-id="32457-107">If one of the files does not have version resources specified or if they have the same version information, the source file is treated as the newer file.</span></span>

 

 
