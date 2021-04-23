---
description: Действие Мовефилес находит существующие файлы на компьютере пользователя и перемещает или копирует эти файлы в новое расположение.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Действие Мовефилес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913483"
---
# <a name="movefiles-action"></a><span data-ttu-id="afc8e-103">Действие Мовефилес</span><span class="sxs-lookup"><span data-stu-id="afc8e-103">MoveFiles Action</span></span>

<span data-ttu-id="afc8e-104">Действие Мовефилес находит существующие файлы на компьютере пользователя и перемещает или копирует эти файлы в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="afc8e-104">The MoveFiles action locates existing files on the user's computer and moves or copies those files to a new location.</span></span> <span data-ttu-id="afc8e-105">Действие Мовефилес запрашивает [таблицу MoveFile](movefile-table.md) и перемещает файлы, указанные в ней, если компонент, связанный с записями, указан для установки локально или выполняется из источника.</span><span class="sxs-lookup"><span data-stu-id="afc8e-105">The MoveFiles action queries the [MoveFile table](movefile-table.md) and moves files specified there if the component linked to the entries is specified to be install locally or is being run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="afc8e-106">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="afc8e-106">Sequence Restrictions</span></span>

<span data-ttu-id="afc8e-107">Действие Мовефилес должно следовать после действия [инсталлвалидате](installvalidate-action.md) и перед действием [инсталлфилес](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="afc8e-107">The MoveFiles action must come after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="afc8e-108">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="afc8e-108">ActionData Messages</span></span>



| <span data-ttu-id="afc8e-109">Поле</span><span class="sxs-lookup"><span data-stu-id="afc8e-109">Field</span></span> | <span data-ttu-id="afc8e-110">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="afc8e-110">Description of action data</span></span>                  |
|-------|---------------------------------------------|
| <span data-ttu-id="afc8e-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="afc8e-111">\[1\]</span></span> | <span data-ttu-id="afc8e-112">Идентификатор перемещенного файла.</span><span class="sxs-lookup"><span data-stu-id="afc8e-112">Identifier of moved file.</span></span>                   |
| <span data-ttu-id="afc8e-113">\[6\]</span><span class="sxs-lookup"><span data-stu-id="afc8e-113">\[6\]</span></span> | <span data-ttu-id="afc8e-114">Размер установленного файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="afc8e-114">Size of installed file in bytes.</span></span>            |
| <span data-ttu-id="afc8e-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="afc8e-115">\[9\]</span></span> | <span data-ttu-id="afc8e-116">Идентификатор каталога, содержащего перемещенный файл.</span><span class="sxs-lookup"><span data-stu-id="afc8e-116">Identifier of directory holding moved file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="afc8e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afc8e-117">Remarks</span></span>

<span data-ttu-id="afc8e-118">Таблица Мовефилес содержит столбец с именем Options, который указывает исходные файлы для перемещения или копирования.</span><span class="sxs-lookup"><span data-stu-id="afc8e-118">The MoveFiles table contain a column named "options" which specifies the source files to be moved or copied.</span></span> <span data-ttu-id="afc8e-119">Перемещенный исходный файл удаляется после его копирования в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="afc8e-119">A moved source file is deleted after it has been copied to a new location.</span></span> <span data-ttu-id="afc8e-120">Точный синтаксис см. в [таблице MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="afc8e-120">For the exact syntax, see the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="afc8e-121">Столбцы SourceFolder и DestFolder таблицы MoveFile — это имена свойств, значения которых должны разрешаться в полные пути.</span><span class="sxs-lookup"><span data-stu-id="afc8e-121">The SourceFolder and DestFolder columns of the MoveFile table are property names whose values are expected to resolve to fully qualified paths.</span></span> <span data-ttu-id="afc8e-122">Эти свойства могут быть любыми записями каталога в таблице [Directory](directory-table.md) , любым стандартным свойством папки (например,[**фаворитесфолдер**](favoritesfolder.md)) или свойством, заданным любой записью в таблице [аппсеарч](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="afc8e-122">These properties can be any of the directory entries in the [Directory](directory-table.md) table, any predefined folder property ([**FavoritesFolder**](favoritesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="afc8e-123">Эти свойства могут содержать полный путь, содержащий имя файла для определенного файла.</span><span class="sxs-lookup"><span data-stu-id="afc8e-123">These properties may contain a full path containing the file name to a specific file.</span></span> <span data-ttu-id="afc8e-124">Например, можно создать таблицу Аппсеарч для поиска определенного файла и задать для свойства полный путь к этому файлу.</span><span class="sxs-lookup"><span data-stu-id="afc8e-124">For example, the AppSearch table can be authored to search for a particular file and set a property to the full path to that file.</span></span> <span data-ttu-id="afc8e-125">В этом примере столбец SourceName в таблице MoveFile можно оставить пустым, чтобы указать, что значение в свойстве SourceFolder содержит полный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="afc8e-125">In this example, the SourceName column in the MoveFile table can be left blank to indicate that the value in the SourceFolder property contains a full file path.</span></span> <span data-ttu-id="afc8e-126">Точка с запятой — это разделитель списка для преобразований, источников и исправлений, который не следует использовать в именах файлов или путях.</span><span class="sxs-lookup"><span data-stu-id="afc8e-126">The semicolon is the list delimiter for transforms, sources, and patches and should not be used in file names or paths.</span></span>

<span data-ttu-id="afc8e-127">Действие Мовефилес не действует на записи в таблице MoveFile, в которых свойство SourceFolder или DestFolder не вычисляется как полный путь.</span><span class="sxs-lookup"><span data-stu-id="afc8e-127">The MoveFiles action does not act on entries in the MoveFile table in which either the SourceFolder or DestFolder property does not evaluate to a full path.</span></span>

<span data-ttu-id="afc8e-128">Действие Мовефилес пытается переместить или скопировать все файлы в исходном каталоге, соответствующие имени, заданному в столбце SourceName таблицы Мовефилес.</span><span class="sxs-lookup"><span data-stu-id="afc8e-128">The MoveFiles action attempts to move or copy all files in the source directory that match the name given in the SourceName column of the MoveFiles table.</span></span> <span data-ttu-id="afc8e-129">Имя в столбце SourceName может включать \* или?</span><span class="sxs-lookup"><span data-stu-id="afc8e-129">The name in the SourceName column can include either the \* or ?</span></span> <span data-ttu-id="afc8e-130">подстановочные знаки, которые позволяют перемещать или копировать группу файлов.</span><span class="sxs-lookup"><span data-stu-id="afc8e-130">wildcards which allow a group of files to be moved or copied.</span></span> <span data-ttu-id="afc8e-131">Например, столбец SourceName может содержать запись « \* . xls», а действие мовефилес перемещает или копирует каждую книгу Microsoft Excel из исходного каталога в место назначения.</span><span class="sxs-lookup"><span data-stu-id="afc8e-131">For example, the SourceName column may contain an entry of "\*.xls" and the MoveFiles action moves or copies every Microsoft Excel workbook from the source directory to the destination.</span></span>

<span data-ttu-id="afc8e-132">Имя, присваиваемое целевому файлу, можно указать в столбце Дестнаме таблицы MoveFile.</span><span class="sxs-lookup"><span data-stu-id="afc8e-132">The name to be given to the destination file can be specified in the DestName column of the MoveFile table.</span></span> <span data-ttu-id="afc8e-133">Имя файла назначения оставляет имя исходного файла, если этот столбец не задан.</span><span class="sxs-lookup"><span data-stu-id="afc8e-133">The destination file name retains the source file name if this column is left blank.</span></span>

<span data-ttu-id="afc8e-134">Если в столбце \* SourceName [таблицы MoveFile](movefile-table.md) указан подстановочный знак "", а имя целевого файла указано в столбце дестнаме, то все перемещенные или скопированные файлы сохранили имена в источниках.</span><span class="sxs-lookup"><span data-stu-id="afc8e-134">If a "\*" wildcard is entered in the SourceName column of the [MoveFile table](movefile-table.md) and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="afc8e-135">Файлы, перемещаемые или скопированные с помощью действия Мовефилес, не удаляются при удалении продукта.</span><span class="sxs-lookup"><span data-stu-id="afc8e-135">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

 

 



