---
description: Действие Унрегистерфонтс удаляет сведения о регистрации установленных шрифтов из системы.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Действие Унрегистерфонтс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674430"
---
# <a name="unregisterfonts-action"></a><span data-ttu-id="2d0aa-103">Действие Унрегистерфонтс</span><span class="sxs-lookup"><span data-stu-id="2d0aa-103">UnregisterFonts Action</span></span>

<span data-ttu-id="2d0aa-104">Действие Унрегистерфонтс удаляет сведения о регистрации установленных шрифтов из системы.</span><span class="sxs-lookup"><span data-stu-id="2d0aa-104">The UnregisterFonts action removes registration information about installed fonts from the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2d0aa-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="2d0aa-105">Sequence Restrictions</span></span>

<span data-ttu-id="2d0aa-106">Действие [ремовефилес](removefiles-action.md) должно быть вызвано после унрегистерфонтс.</span><span class="sxs-lookup"><span data-stu-id="2d0aa-106">The [RemoveFiles](removefiles-action.md) action must be called after UnregisterFonts.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2d0aa-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="2d0aa-107">ActionData Messages</span></span>



| <span data-ttu-id="2d0aa-108">Поле</span><span class="sxs-lookup"><span data-stu-id="2d0aa-108">Field</span></span> | <span data-ttu-id="2d0aa-109">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="2d0aa-109">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="2d0aa-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2d0aa-110">\[1\]</span></span> | <span data-ttu-id="2d0aa-111">Файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="2d0aa-111">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="2d0aa-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d0aa-112">Remarks</span></span>

<span data-ttu-id="2d0aa-113">Действие Унрегистерфонтс выполняется, если файл, указанный в \_ столбце file [таблицы Font](font-table.md) , относится к удаляемому компоненту.</span><span class="sxs-lookup"><span data-stu-id="2d0aa-113">The UnregisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being uninstalled.</span></span>

 

 



