---
description: Действие Ремовефилес удаляет файлы, ранее установленные действием Инсталлфилес.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Действие Ремовефилес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663845"
---
# <a name="removefiles-action"></a><span data-ttu-id="fa5d1-103">Действие Ремовефилес</span><span class="sxs-lookup"><span data-stu-id="fa5d1-103">RemoveFiles Action</span></span>

<span data-ttu-id="fa5d1-104">Действие Ремовефилес удаляет файлы, ранее установленные действием [инсталлфилес](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="fa5d1-104">The RemoveFiles action removes files previously installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="fa5d1-105">Каждый из этих файлов называется ссылкой на запись в таблице [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fa5d1-105">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="fa5d1-106">Удаляются только те файлы с компонентами, которые разрешены в состояние *мсиинсталлстатеабсент* или *мсиинсталлстателокал* , если компонент установлен локально.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-106">Only those files with components resolved to either the *msiInstallStateAbsent* state or the *msiInstallStateLocal* state if the component is installed locally, are removed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fa5d1-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="fa5d1-107">Sequence Restrictions</span></span>

<span data-ttu-id="fa5d1-108">Перед вызовом Ремовефилес необходимо вызвать действие [инсталлвалидате](installvalidate-action.md) .</span><span class="sxs-lookup"><span data-stu-id="fa5d1-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveFiles.</span></span> <span data-ttu-id="fa5d1-109">Если используется действие [инсталлфилес](installfiles-action.md) , оно должно появиться после ремовефилес.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear after RemoveFiles.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fa5d1-110">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="fa5d1-110">ActionData Messages</span></span>



| <span data-ttu-id="fa5d1-111">Поле</span><span class="sxs-lookup"><span data-stu-id="fa5d1-111">Field</span></span> | <span data-ttu-id="fa5d1-112">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="fa5d1-112">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="fa5d1-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fa5d1-113">\[1\]</span></span> | <span data-ttu-id="fa5d1-114">Идентификатор удаленного файла.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-114">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="fa5d1-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="fa5d1-115">\[9\]</span></span> | <span data-ttu-id="fa5d1-116">Идентификатор каталога, содержащего удаленный файл.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-116">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fa5d1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa5d1-117">Remarks</span></span>

<span data-ttu-id="fa5d1-118">Таблицу [ремовефиле](removefile-table.md) можно опустить из базы данных установщика, если нет каких либо прочих файлов для удаления.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-118">The [RemoveFile](removefile-table.md) table can be omitted from the installer database if there are no miscellaneous files to remove.</span></span>

<span data-ttu-id="fa5d1-119">Действие Ремовефилес также может удалять файлы, определенные автором, которые не установлены действием Инсталлфилес.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-119">The RemoveFiles action can also remove author-specified files that are not installed by the InstallFiles action.</span></span> <span data-ttu-id="fa5d1-120">Эти файлы указаны в таблице [ремовефиле](removefile-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fa5d1-120">These files are specified in the [RemoveFile](removefile-table.md) table.</span></span> <span data-ttu-id="fa5d1-121">Каждый из этих файлов называется ссылкой на запись в таблице [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fa5d1-121">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="fa5d1-122">Эти файлы, компоненты которых разрешаются в любое активное состояние действия (то есть не в состоянии OFF или null), удаляются, если файл существует в указанном каталоге.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-122">Those files whose components are resolved to any active Action state (that is, not in the Off or Null state) are removed if the file exists in the specified directory.</span></span> <span data-ttu-id="fa5d1-123">Попытка удаления файлов, указанных в таблице Ремовефиле, выполняется при первой установке связанного компонента, во время переустановки и при удалении связанного компонента.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-123">The removal of files specified in the RemoveFile table is attempted when the linked component is first installed, during a reinstall, and again when the linked component is removed.</span></span>

<span data-ttu-id="fa5d1-124">Действие Ремовефилес также может удалять папки.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-124">The RemoveFiles action can also remove folders.</span></span> <span data-ttu-id="fa5d1-125">Пустая папка удаляется, если значение в столбце FileName таблицы Ремовефиле имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-125">An empty folder is removed if the value in the FileName column of the RemoveFile table is null.</span></span>

<span data-ttu-id="fa5d1-126">При удалении ранее установленных файлов действие Ремовефилес запрашивает те же поля в тех же таблицах, которые были запрошены действием [инсталлфилес](installfiles-action.md) , за исключением того, что [Таблица Media](media-table.md) не используется действием ремовефилес.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-126">When removing previously installed files, the RemoveFiles action queries the same fields in the same tables as those queried by the [InstallFiles](installfiles-action.md) action with the exception that the [Media table](media-table.md) is not used by the RemoveFiles action.</span></span>

<span data-ttu-id="fa5d1-127">Имя целевого файла можно указать в локализованном тексте в столбце FileName таблицы Ремовефиле.</span><span class="sxs-lookup"><span data-stu-id="fa5d1-127">The target file name can be specified in localized text in the FileName column of the RemoveFile table.</span></span>

 

 



