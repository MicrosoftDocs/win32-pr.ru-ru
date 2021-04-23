---
description: Действие Вритеинивалуес записывает сведения о ini-файле, которые должны быть записаны приложением в свои ini-файлы.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Действие Вритеинивалуес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910667"
---
# <a name="writeinivalues-action"></a><span data-ttu-id="2d074-103">Действие Вритеинивалуес</span><span class="sxs-lookup"><span data-stu-id="2d074-103">WriteIniValues Action</span></span>

<span data-ttu-id="2d074-104">Действие Вритеинивалуес записывает сведения о ini-файле, которые должны быть записаны приложением в свои ini-файлы.</span><span class="sxs-lookup"><span data-stu-id="2d074-104">The WriteIniValues action writes the .ini file information that the application needs written to its .ini files.</span></span> <span data-ttu-id="2d074-105">Запись этих сведений наследуется [таблицей Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="2d074-105">The writing of this information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="2d074-106">Значение ini-файлов записывается, если соответствующий компонент настроен для установки локально или выполняется из источника.</span><span class="sxs-lookup"><span data-stu-id="2d074-106">An .ini value is written if the corresponding component has been set to be installed either locally or run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2d074-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="2d074-107">Sequence Restrictions</span></span>

<span data-ttu-id="2d074-108">Действие Инсталлвалидате должно следовать перед действием Вритеинивалуес.</span><span class="sxs-lookup"><span data-stu-id="2d074-108">The InstallValidate action must come before the WriteIniValues action.</span></span> <span data-ttu-id="2d074-109">Если в последовательности есть [действие ремовеинивалуес](removeinivalues-action.md) , оно должно быть перед действием вритеинивалуес.</span><span class="sxs-lookup"><span data-stu-id="2d074-109">If there is a [RemoveIniValues action](removeinivalues-action.md) in the sequence, then it must come before the WriteIniValues action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2d074-110">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="2d074-110">ActionData Messages</span></span>



| <span data-ttu-id="2d074-111">Поле</span><span class="sxs-lookup"><span data-stu-id="2d074-111">Field</span></span> | <span data-ttu-id="2d074-112">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="2d074-112">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="2d074-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2d074-113">\[1\]</span></span> | <span data-ttu-id="2d074-114">Идентификатор ini-файла.</span><span class="sxs-lookup"><span data-stu-id="2d074-114">Identifier of .ini file.</span></span>                |
| <span data-ttu-id="2d074-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2d074-115">\[2\]</span></span> | <span data-ttu-id="2d074-116">INI-файл в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="2d074-116">.ini file key in the following section.</span></span> |
| <span data-ttu-id="2d074-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="2d074-117">\[3\]</span></span> | <span data-ttu-id="2d074-118">Элемент удален из ini-файла.</span><span class="sxs-lookup"><span data-stu-id="2d074-118">Item removed from .ini file.</span></span>            |
| <span data-ttu-id="2d074-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="2d074-119">\[4\]</span></span> | <span data-ttu-id="2d074-120">Значение, удаленное из ini-файла.</span><span class="sxs-lookup"><span data-stu-id="2d074-120">Value removed from .ini file.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="2d074-121">См. также</span><span class="sxs-lookup"><span data-stu-id="2d074-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d074-122">Таблица Инифиле</span><span class="sxs-lookup"><span data-stu-id="2d074-122">IniFile table</span></span>](inifile-table.md)
</dt> </dl>

 

 



