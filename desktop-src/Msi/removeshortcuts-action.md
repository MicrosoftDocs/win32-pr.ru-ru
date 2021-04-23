---
description: Действие Ремовешорткутс управляет удалением объявленного ярлыка, компонент которого выбран для удаления, или необъявленный ярлык, компонент которого выбран для удаления. Дополнительные сведения см. в таблице ярлыков.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Действие Ремовешорткутс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650899"
---
# <a name="removeshortcuts-action"></a><span data-ttu-id="2510e-104">Действие Ремовешорткутс</span><span class="sxs-lookup"><span data-stu-id="2510e-104">RemoveShortcuts Action</span></span>

<span data-ttu-id="2510e-105">Действие Ремовешорткутс управляет удалением объявленного ярлыка, компонент которого выбран для удаления, или необъявленный ярлык, компонент которого выбран для удаления.</span><span class="sxs-lookup"><span data-stu-id="2510e-105">The RemoveShortcuts action manages the removal of an advertised shortcut whose feature is selected for uninstallation or a nonadvertised shortcut whose component is selected for uninstallation.</span></span> <span data-ttu-id="2510e-106">Дополнительные сведения см. в [таблице ярлыков](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="2510e-106">For more information, see the [Shortcut Table](shortcut-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2510e-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="2510e-107">Sequence Restrictions</span></span>

<span data-ttu-id="2510e-108">Действие Ремовешорткутс должно следовать перед действием [креатешорткутс](createshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2510e-108">The RemoveShortcuts action must come before the [CreateShortcuts](createshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2510e-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="2510e-109">ActionData Messages</span></span>



| <span data-ttu-id="2510e-110">Поле</span><span class="sxs-lookup"><span data-stu-id="2510e-110">Field</span></span> | <span data-ttu-id="2510e-111">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="2510e-111">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="2510e-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2510e-112">\[1\]</span></span> | <span data-ttu-id="2510e-113">Идентификатор удаленного ярлыка.</span><span class="sxs-lookup"><span data-stu-id="2510e-113">Identifier of removed shortcut.</span></span> |



 

 

 



