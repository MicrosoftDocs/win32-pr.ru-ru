---
description: Действие Ремоведупликатефилес удаляет файлы, установленные действием Дупликатефилес.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Действие Ремоведупликатефилес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809491"
---
# <a name="removeduplicatefiles-action"></a><span data-ttu-id="80dc2-103">Действие Ремоведупликатефилес</span><span class="sxs-lookup"><span data-stu-id="80dc2-103">RemoveDuplicateFiles Action</span></span>

<span data-ttu-id="80dc2-104">Действие Ремоведупликатефилес удаляет файлы, установленные действием [дупликатефилес](duplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="80dc2-104">The RemoveDuplicateFiles action deletes files installed by the [DuplicateFiles](duplicatefiles-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="80dc2-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="80dc2-105">Sequence Restrictions</span></span>

<span data-ttu-id="80dc2-106">Действие Ремоведупликатефилес должно быть выполнено после действия [инсталлвалидате](installvalidate-action.md) и перед действием [инсталлфилес](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="80dc2-106">The RemoveDuplicateFiles action must occur after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="80dc2-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="80dc2-107">ActionData Messages</span></span>



| <span data-ttu-id="80dc2-108">Поле</span><span class="sxs-lookup"><span data-stu-id="80dc2-108">Field</span></span> | <span data-ttu-id="80dc2-109">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="80dc2-109">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="80dc2-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="80dc2-110">\[1\]</span></span> | <span data-ttu-id="80dc2-111">Идентификатор удаленного файла.</span><span class="sxs-lookup"><span data-stu-id="80dc2-111">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="80dc2-112">\[9\]</span><span class="sxs-lookup"><span data-stu-id="80dc2-112">\[9\]</span></span> | <span data-ttu-id="80dc2-113">Идентификатор каталога, содержащего удаленный файл.</span><span class="sxs-lookup"><span data-stu-id="80dc2-113">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="80dc2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80dc2-114">Remarks</span></span>

<span data-ttu-id="80dc2-115">Чтобы удалить файл, дублирующийся с помощью действия [дупликатефилес](duplicatefiles-action.md) , используя действие ремоведупликатефилес, необходимо выбрать компонент, связанный с записью файла в таблице дупликатефиле, для удаления.</span><span class="sxs-lookup"><span data-stu-id="80dc2-115">To delete a file duplicated with the [DuplicateFiles action](duplicatefiles-action.md) using the RemoveDuplicateFiles action, the component associated with the file's entry in the DuplicateFile table must be selected for removal.</span></span>

<span data-ttu-id="80dc2-116">Используйте столбец DestFolder [таблицы дупликатефиле](duplicatefile-table.md) , чтобы указать имя свойства, значение которого определяет целевую папку.</span><span class="sxs-lookup"><span data-stu-id="80dc2-116">Use the DestFolder column of the [DuplicateFile table](duplicatefile-table.md) to specify the property name whose value identifies the destination folder.</span></span>

 

 



