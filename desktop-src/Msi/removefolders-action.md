---
description: Действие Ремовефолдерс удаляет все папки, связанные с набором компонентов, которые будут удалены или запускаться из источника. Эти папки удаляются только в том случае, если они пусты. Если папка удалена, она отменяется регистрацией с соответствующим идентификатором компонента.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Действие Ремовефолдерс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265414"
---
# <a name="removefolders-action"></a><span data-ttu-id="26c93-105">Действие Ремовефолдерс</span><span class="sxs-lookup"><span data-stu-id="26c93-105">RemoveFolders Action</span></span>

<span data-ttu-id="26c93-106">Действие Ремовефолдерс удаляет все папки, связанные с набором компонентов, которые будут удалены или запускаться из источника.</span><span class="sxs-lookup"><span data-stu-id="26c93-106">The RemoveFolders action removes any folders linked to components set to be removed or run from source.</span></span> <span data-ttu-id="26c93-107">Эти папки удаляются только в том случае, если они пусты.</span><span class="sxs-lookup"><span data-stu-id="26c93-107">These folders are removed only if they are empty.</span></span> <span data-ttu-id="26c93-108">Если папка удалена, она отменяется регистрацией с соответствующим идентификатором компонента.</span><span class="sxs-lookup"><span data-stu-id="26c93-108">If a folder is removed, it is unregistered with the appropriate component identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="26c93-109">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="26c93-109">Sequence Restrictions</span></span>

<span data-ttu-id="26c93-110">Действие Ремовефолдерс должно быть получено после действия [ремовефилес](removefiles-action.md) или любого действия, которое может удалить файлы из папок.</span><span class="sxs-lookup"><span data-stu-id="26c93-110">The RemoveFolders action must come after the [RemoveFiles](removefiles-action.md) action or any action that may remove files from folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="26c93-111">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="26c93-111">ActionData Messages</span></span>



| <span data-ttu-id="26c93-112">Поле</span><span class="sxs-lookup"><span data-stu-id="26c93-112">Field</span></span> | <span data-ttu-id="26c93-113">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="26c93-113">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="26c93-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="26c93-114">\[1\]</span></span> | <span data-ttu-id="26c93-115">Идентификатор удаленной папки.</span><span class="sxs-lookup"><span data-stu-id="26c93-115">Identifier of removed folder.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="26c93-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26c93-116">Remarks</span></span>

<span data-ttu-id="26c93-117">Установщик не удаляет автоматически папки, созданные [действием креатефолдерс](createfolders-action.md) во время удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="26c93-117">The installer does not automatically remove the folders created by the [CreateFolders action](createfolders-action.md) during an uninstallation of the application.</span></span> <span data-ttu-id="26c93-118">Установщику необходимо удалить эти папки, разработав действие Ремовефолдерс в последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="26c93-118">The installer must be instructed to remove these folders by authoring the RemoveFolders action into the action sequence.</span></span>

<span data-ttu-id="26c93-119">Чтобы указать имя и расположение папки, используйте \_ столбец Directory [таблицы креатефолдер](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="26c93-119">To specify the name and location of the folder, use the Directory\_ column of the [CreateFolder table](createfolder-table.md).</span></span> <span data-ttu-id="26c93-120">Имя каждой папки в таблице Креатефолдер считается свойством, определяющим расположение папки.</span><span class="sxs-lookup"><span data-stu-id="26c93-120">Each folder name in the CreateFolder table is assumed to be a property defining the folder location.</span></span>

<span data-ttu-id="26c93-121">Чтобы указать компонент, владеющий папкой, используйте столбец ComponentId [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="26c93-121">To specify the component owning the folder, use the ComponentId column of the [Component table](component-table.md).</span></span>

 

 



