---
title: Переименование скомпилированного файла ресурсов
description: По умолчанию при компиляции ресурсов версия-кандидат присваивает файлу скомпилированного ресурса (. res) базовое имя RC-файла и помещает его в тот же каталог, где находится RC-файл.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252828"
---
# <a name="renaming-the-compiled-resource-file"></a><span data-ttu-id="6401c-103">Переименование скомпилированного файла ресурсов</span><span class="sxs-lookup"><span data-stu-id="6401c-103">Renaming the Compiled Resource File</span></span>

<span data-ttu-id="6401c-104">По умолчанию при компиляции ресурсов версия-кандидат присваивает файлу скомпилированного ресурса (. res) базовое имя RC-файла и помещает его в тот же каталог, где находится RC-файл.</span><span class="sxs-lookup"><span data-stu-id="6401c-104">By default, when compiling resources, RC names the compiled resource (.res) file with the base name of the .rc file and places it in the same directory as the .rc file.</span></span> <span data-ttu-id="6401c-105">Затем необходимо вызвать CVTRES, чтобы преобразовать RES-файл в формат двоичного ресурса (. РБЖ), который может быть понят компоновщиком.</span><span class="sxs-lookup"><span data-stu-id="6401c-105">CVTRES must then be invoked to convert the .res file to a binary resource (.rbj) format which can be understood by the linker.</span></span> <span data-ttu-id="6401c-106">В следующем примере компилируется MyApp. RC и создается скомпилированный файл ресурсов с именем MyApp. res в том же каталоге, что и MyApp. rc:</span><span class="sxs-lookup"><span data-stu-id="6401c-106">The following example compiles MyApp.rc and creates a compiled resource file named MyApp.res in the same directory as MyApp.rc:</span></span>

<span data-ttu-id="6401c-107">**Версия-кандидат MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="6401c-107">**rc myapp.rc**</span></span>

<span data-ttu-id="6401c-108">Параметр **/FO** присваивает результирующему RES-файлу имя, которое отличается от имени соответствующего файла. rc.</span><span class="sxs-lookup"><span data-stu-id="6401c-108">The **/fo** option gives the resulting .res file a name that differs from the name of the corresponding .rc file.</span></span> <span data-ttu-id="6401c-109">Например, чтобы присвоить результирующему RES file имя NewFile. Res, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6401c-109">For example, to name the resulting .res file NewFile.res, use the following command:</span></span>

<span data-ttu-id="6401c-110">**Версия-кандидат: NewFile. RES MYAPP. RC**</span><span class="sxs-lookup"><span data-stu-id="6401c-110">**rc -fo newfile.res myapp.rc**</span></span>

<span data-ttu-id="6401c-111">Параметр **/FO** также может поместить RES-файл в другой каталог.</span><span class="sxs-lookup"><span data-stu-id="6401c-111">The **/fo** option can also place the .res file in a different directory.</span></span> <span data-ttu-id="6401c-112">Например, следующая команда помещает скомпилированный файл ресурсов MyApp. res в каталог C: \\ исходный \\ ресурс:</span><span class="sxs-lookup"><span data-stu-id="6401c-112">For example, the following command places the compiled resource file MyApp.res in the directory C:\\Source\\Resource:</span></span>

<span data-ttu-id="6401c-113">**RC-FO c: \\ исходный \\ ресурс \\ MyApp. RES MYAPP. RC**</span><span class="sxs-lookup"><span data-stu-id="6401c-113">**rc -fo c:\\source\\resource\\myapp.res myapp.rc**</span></span>

 

 




