---
description: Действие Дупликатефилес дублирует файлы, установленные действием Инсталлфилес. Дубликаты файлов можно скопировать в тот же каталог с другим именем или в другой каталог с исходным именем.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Действие Дупликатефилес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650867"
---
# <a name="duplicatefiles-action"></a><span data-ttu-id="40f71-104">Действие Дупликатефилес</span><span class="sxs-lookup"><span data-stu-id="40f71-104">DuplicateFiles Action</span></span>

<span data-ttu-id="40f71-105">Действие Дупликатефилес дублирует файлы, установленные действием [инсталлфилес](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="40f71-105">The DuplicateFiles action duplicates files installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="40f71-106">Дубликаты файлов можно скопировать в тот же каталог с другим именем или в другой каталог с исходным именем.</span><span class="sxs-lookup"><span data-stu-id="40f71-106">The duplicate files can be copied to the same directory with a different name or to a different directory with the original name.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="40f71-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="40f71-107">Sequence Restrictions</span></span>

<span data-ttu-id="40f71-108">Действие Дупликатефилес должно следовать после [действия инсталлфилес](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="40f71-108">The DuplicateFiles action must come after the [InstallFiles action](installfiles-action.md).</span></span> <span data-ttu-id="40f71-109">Действие Дупликатефилес также должно быть после [действия патчфилес](patchfiles-action.md) , чтобы предотвратить дублирование неисправленной версии файла.</span><span class="sxs-lookup"><span data-stu-id="40f71-109">The DuplicateFiles Action must also come after the [PatchFiles action](patchfiles-action.md) to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="40f71-110">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="40f71-110">ActionData Messages</span></span>



| <span data-ttu-id="40f71-111">Поле</span><span class="sxs-lookup"><span data-stu-id="40f71-111">Field</span></span> | <span data-ttu-id="40f71-112">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="40f71-112">Description of action data</span></span>                       |
|-------|--------------------------------------------------|
| <span data-ttu-id="40f71-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="40f71-113">\[1\]</span></span> | <span data-ttu-id="40f71-114">Идентификатор повторяющегося файла.</span><span class="sxs-lookup"><span data-stu-id="40f71-114">Identifier of duplicated file.</span></span>                   |
| <span data-ttu-id="40f71-115">\[6\]</span><span class="sxs-lookup"><span data-stu-id="40f71-115">\[6\]</span></span> | <span data-ttu-id="40f71-116">Размер повторяющегося файла.</span><span class="sxs-lookup"><span data-stu-id="40f71-116">Size of duplicated file.</span></span>                         |
| <span data-ttu-id="40f71-117">\[9\]</span><span class="sxs-lookup"><span data-stu-id="40f71-117">\[9\]</span></span> | <span data-ttu-id="40f71-118">Идентификатор каталога, содержащего дублирующийся файл.</span><span class="sxs-lookup"><span data-stu-id="40f71-118">Identifier of directory holding duplicated file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="40f71-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40f71-119">Remarks</span></span>

<span data-ttu-id="40f71-120">Действие Дупликатефилес обрабатывает запись [таблицы дупликатефиле](duplicatefile-table.md) только в том случае, если компонент, связанный с этой записью, устанавливается локально.</span><span class="sxs-lookup"><span data-stu-id="40f71-120">The DuplicateFiles action processes a [DuplicateFile table](duplicatefile-table.md) entry only if the component linked to that entry is being installed locally.</span></span> <span data-ttu-id="40f71-121">Дополнительные сведения см. в разделе [Таблица Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="40f71-121">For more information, see [Component table](component-table.md).</span></span>

<span data-ttu-id="40f71-122">Строка в поле DestFolder представляет собой имя свойства, значение которого должно разрешаться в полный путь.</span><span class="sxs-lookup"><span data-stu-id="40f71-122">The string in the DestFolder field is a property name whose value is expected to resolve to a fully qualified path.</span></span> <span data-ttu-id="40f71-123">Это свойство может быть любой из записей каталога в таблице [Directory](directory-table.md) , все предварительно определенные свойства папки (например,[**коммонфилесфолдер**](commonfilesfolder.md)) или свойство, заданное любой записью в таблице [аппсеарч](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="40f71-123">This property can either be any of the directory entries in the [Directory](directory-table.md) table, any pre-defined folder property ([**CommonFilesFolder**](commonfilesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="40f71-124">Если значение свойства **DestFolder** не является допустимым путем, действие дупликатефилес не выполняет никаких действий для этой записи.</span><span class="sxs-lookup"><span data-stu-id="40f71-124">If the **DestFolder** property does not evaluate to a valid path the DuplicateFiles action does nothing for that entry.</span></span>

<span data-ttu-id="40f71-125">Если имя целевого файла в столбце Дестнаме таблицы Дупликатефиле остается пустым, имя целевого файла будет совпадать с именем исходного файла.</span><span class="sxs-lookup"><span data-stu-id="40f71-125">If the name of the destination file in the DestName column of the DuplicateFile table is left blank, the destination file name will be the same as the original file name.</span></span>

<span data-ttu-id="40f71-126">Файлы, установленные действием Дупликатефилес, удаляются действием [ремоведупликатефилес](removeduplicatefiles-action.md) при необходимости.</span><span class="sxs-lookup"><span data-stu-id="40f71-126">Files installed by the DuplicateFiles action are removed by the [RemoveDuplicateFiles](removeduplicatefiles-action.md) action when appropriate.</span></span>

 

 



