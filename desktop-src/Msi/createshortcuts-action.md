---
description: Действие Креатешорткутс управляет созданием ярлыков.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Действие Креатешорткутс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081370"
---
# <a name="createshortcuts-action"></a><span data-ttu-id="9065c-103">Действие Креатешорткутс</span><span class="sxs-lookup"><span data-stu-id="9065c-103">CreateShortcuts Action</span></span>

<span data-ttu-id="9065c-104">Действие Креатешорткутс управляет созданием ярлыков.</span><span class="sxs-lookup"><span data-stu-id="9065c-104">The CreateShortcuts action manages the creation of shortcuts.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9065c-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="9065c-105">Sequence Restrictions</span></span>

<span data-ttu-id="9065c-106">Действие Креатешорткутс должно следовать после действия [инсталлфилес](installfiles-action.md) и действия [ремовешорткутс](removeshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9065c-106">The CreateShortcuts action must come after the [InstallFiles](installfiles-action.md) action and the [RemoveShortcuts](removeshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9065c-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="9065c-107">ActionData Messages</span></span>



| <span data-ttu-id="9065c-108">Поле</span><span class="sxs-lookup"><span data-stu-id="9065c-108">Field</span></span> | <span data-ttu-id="9065c-109">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="9065c-109">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="9065c-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9065c-110">\[1\]</span></span> | <span data-ttu-id="9065c-111">Идентификатор созданного ярлыка.</span><span class="sxs-lookup"><span data-stu-id="9065c-111">Identifier of created shortcut.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9065c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9065c-112">Remarks</span></span>

<span data-ttu-id="9065c-113">Действие Креатешорткутс создает ярлыки файлов ключей компонентов компонентов, выбранных для установки или объявления.</span><span class="sxs-lookup"><span data-stu-id="9065c-113">The CreateShortcuts action creates shortcuts to the key files of components of features that are selected for installation or advertisement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9065c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="9065c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9065c-115">Таблица ярлыков</span><span class="sxs-lookup"><span data-stu-id="9065c-115">Shortcut Table</span></span>](shortcut-table.md)
</dt> <dt>

[<span data-ttu-id="9065c-116">Таблица Мсишорткутпроперти</span><span class="sxs-lookup"><span data-stu-id="9065c-116">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
</dt> </dl>

 

 



