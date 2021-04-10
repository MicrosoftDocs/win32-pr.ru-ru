---
description: 'После завершения учета стоимости файлов у установщика будут все сведения, необходимые для обработки двух действий по обработке файлов: Дупликатефилес и Мовефилес.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Установка файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156631"
---
# <a name="file-installation"></a><span data-ttu-id="d40c2-103">Установка файла</span><span class="sxs-lookup"><span data-stu-id="d40c2-103">File Installation</span></span>

<span data-ttu-id="d40c2-104">После завершения [учета стоимости файлов](file-costing.md) у установщика будут все сведения, необходимые для обработки двух действий по обработке файлов: [дупликатефилес](duplicatefiles-action.md) и [мовефилес](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="d40c2-104">Once [file costing](file-costing.md) has been completed, the installer has all the information required to process the two file manipulation actions: [DuplicateFiles](duplicatefiles-action.md) and [MoveFiles](movefiles-action.md).</span></span>

<span data-ttu-id="d40c2-105">Используйте [действие дупликатефилес](duplicatefiles-action.md) , чтобы указать файлы, которые установщик должен дублировать в [таблице дупликатефиле](duplicatefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="d40c2-105">Use the [DuplicateFiles action](duplicatefiles-action.md) to specify the files the installer is to duplicate in the [DuplicateFile table](duplicatefile-table.md).</span></span> <span data-ttu-id="d40c2-106">Используйте [действие мовефилес](movefiles-action.md), чтобы определить, какие файлы нужно переместить, выполнив запрос к [таблице MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="d40c2-106">Use the [MoveFiles action](movefiles-action.md)to determine which files to move by querying the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="d40c2-107">Обратите внимание, что в поле Options [таблицы MoveFile](movefile-table.md) указывается, следует ли удалять исходный файл из текущего расположения.</span><span class="sxs-lookup"><span data-stu-id="d40c2-107">Note that the Options field of the [MoveFile table](movefile-table.md) specifies whether or not the original file is to be deleted from its current location.</span></span> <span data-ttu-id="d40c2-108">Файлы, перемещаемые или скопированные с помощью действия Мовефилес, не удаляются при удалении продукта.</span><span class="sxs-lookup"><span data-stu-id="d40c2-108">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

<span data-ttu-id="d40c2-109">[Действие инсталлфилес](installfiles-action.md) вызывается по завершении всех остальных операций обработки файлов.</span><span class="sxs-lookup"><span data-stu-id="d40c2-109">The [InstallFiles action](installfiles-action.md) is called once all other file manipulation operations have completed.</span></span> <span data-ttu-id="d40c2-110">Действие Инсталлфилес обрабатывает [таблицу мультимедиа](media-table.md), [файловую таблицу](file-table.md)и [таблицу Component](component-table.md) , чтобы определить, какие файлы будут скопированы из источника в место назначения.</span><span class="sxs-lookup"><span data-stu-id="d40c2-110">The InstallFiles action processes the [Media table](media-table.md), the [File table](file-table.md), and the [Component table](component-table.md) to determine which files will be copied from the source to the destination.</span></span>

<span data-ttu-id="d40c2-111">[Действие инсталлфилес](installfiles-action.md) создает структуру каталогов, необходимую для установки всех файлов.</span><span class="sxs-lookup"><span data-stu-id="d40c2-111">The [InstallFiles action](installfiles-action.md) creates the directory structure necessary to install all files.</span></span> <span data-ttu-id="d40c2-112">Если требуется установить явно пустую папку, для ее создания можно вызвать [действие креатефолдерс](createfolders-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d40c2-112">If an explicitly empty folder is required to be installed, the [CreateFolders action](createfolders-action.md) may be called to create it.</span></span>

 

 



