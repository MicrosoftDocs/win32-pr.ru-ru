---
description: Действие Креатефолдерс создает пустые папки для компонентов, которые установлены.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Действие Креатефолдерс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664667"
---
# <a name="createfolders-action"></a><span data-ttu-id="ea2e5-103">Действие Креатефолдерс</span><span class="sxs-lookup"><span data-stu-id="ea2e5-103">CreateFolders Action</span></span>

<span data-ttu-id="ea2e5-104">Действие Креатефолдерс создает пустые папки для компонентов, которые установлены.</span><span class="sxs-lookup"><span data-stu-id="ea2e5-104">The CreateFolders action creates empty folders for components that are set to be installed.</span></span> <span data-ttu-id="ea2e5-105">Установщик создает папки для компонентов, которые выполняются локально и запускаются из источника.</span><span class="sxs-lookup"><span data-stu-id="ea2e5-105">The installer creates folders both for components that run locally and run from source.</span></span> <span data-ttu-id="ea2e5-106">Вновь созданные папки регистрируются с соответствующим идентификатором компонента.</span><span class="sxs-lookup"><span data-stu-id="ea2e5-106">Newly created folders are registered with the appropriate component identifier.</span></span>

<span data-ttu-id="ea2e5-107">Действие Креатефолдерс запрашивает [таблицу креатефолдер](createfolder-table.md) и [таблицу Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ea2e5-107">The CreateFolders action queries the [CreateFolder table](createfolder-table.md) and the [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ea2e5-108">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="ea2e5-108">Sequence Restrictions</span></span>

<span data-ttu-id="ea2e5-109">Действие Креатефолдерс должно выполняться перед действием [инсталлфилес](installfiles-action.md) или перед любым действием, добавляющим файлы в папки.</span><span class="sxs-lookup"><span data-stu-id="ea2e5-109">The CreateFolders action must be executed either before the [InstallFiles](installfiles-action.md) action or before any action that adds files to folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ea2e5-110">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="ea2e5-110">ActionData Messages</span></span>



| <span data-ttu-id="ea2e5-111">Поле</span><span class="sxs-lookup"><span data-stu-id="ea2e5-111">Field</span></span> | <span data-ttu-id="ea2e5-112">Описание данных действия описание</span><span class="sxs-lookup"><span data-stu-id="ea2e5-112">Description of action data description</span></span> |
|-------|----------------------------------------|
| <span data-ttu-id="ea2e5-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ea2e5-113">\[1\]</span></span> | <span data-ttu-id="ea2e5-114">Идентификатор каталога папки.</span><span class="sxs-lookup"><span data-stu-id="ea2e5-114">Directory identifier of folder.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="ea2e5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea2e5-115">Remarks</span></span>

<span data-ttu-id="ea2e5-116">Установщик не удаляет папки, созданные действием Креатефолдерс, во время удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="ea2e5-116">The installer does not automatically remove folders created by the CreateFolders action during an uninstallation of the application.</span></span> <span data-ttu-id="ea2e5-117">Установщик удаляет только папки, если [действие ремовефолдерс](removefolders-action.md) включено в последовательность действий.</span><span class="sxs-lookup"><span data-stu-id="ea2e5-117">The installer only removes folders if the [RemoveFolders action](removefolders-action.md) is included in the action sequence.</span></span>

 

 



