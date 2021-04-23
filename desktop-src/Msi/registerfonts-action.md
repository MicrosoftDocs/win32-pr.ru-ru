---
description: Действие Регистерфонтс регистрирует установленные шрифты в системе. Это действие сопоставляет имя шрифта в столбце Фонттитле таблицы Font с путем к установленному файлу шрифта.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Действие Регистерфонтс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650781"
---
# <a name="registerfonts-action"></a><span data-ttu-id="b1962-104">Действие Регистерфонтс</span><span class="sxs-lookup"><span data-stu-id="b1962-104">RegisterFonts Action</span></span>

<span data-ttu-id="b1962-105">Действие Регистерфонтс регистрирует установленные шрифты в системе.</span><span class="sxs-lookup"><span data-stu-id="b1962-105">The RegisterFonts action registers installed fonts with the system.</span></span> <span data-ttu-id="b1962-106">Это действие сопоставляет имя шрифта в столбце Фонттитле [таблицы Font](font-table.md) с путем к установленному файлу шрифта.</span><span class="sxs-lookup"><span data-stu-id="b1962-106">This action maps the font name in the FontTitle column of the [Font table](font-table.md) to the path of the font file installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b1962-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="b1962-107">Sequence Restrictions</span></span>

<span data-ttu-id="b1962-108">Действие [инсталлфилес](installfiles-action.md) должно быть вызвано до вызова действия регистерфонтс.</span><span class="sxs-lookup"><span data-stu-id="b1962-108">The [InstallFiles](installfiles-action.md) action must be called before calling the RegisterFonts action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b1962-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="b1962-109">ActionData Messages</span></span>



| <span data-ttu-id="b1962-110">Поле</span><span class="sxs-lookup"><span data-stu-id="b1962-110">Field</span></span> | <span data-ttu-id="b1962-111">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="b1962-111">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="b1962-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b1962-112">\[1\]</span></span> | <span data-ttu-id="b1962-113">Файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="b1962-113">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="b1962-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1962-114">Remarks</span></span>

<span data-ttu-id="b1962-115">Действие Регистерфонтс выполняется, если файл, указанный в \_ столбце file [таблицы Font](font-table.md) , относится к устанавливаемому компоненту.</span><span class="sxs-lookup"><span data-stu-id="b1962-115">The RegisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being installed.</span></span>

 

 



