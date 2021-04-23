---
description: Установщик Windows предоставляет разработчикам пакетов возможность создавать внутренний пользовательский интерфейс с несколькими уровнями функциональности.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Уровни пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272780"
---
# <a name="user-interface-levels"></a><span data-ttu-id="c07c5-103">Уровни пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c07c5-103">User Interface Levels</span></span>

<span data-ttu-id="c07c5-104">Установщик Windows предоставляет разработчикам пакетов возможность создавать внутренний пользовательский интерфейс с несколькими уровнями функциональности.</span><span class="sxs-lookup"><span data-stu-id="c07c5-104">Windows Installer provides package developers the capability to author an internal user interface that has multiple levels of functionality.</span></span> <span data-ttu-id="c07c5-105">Так как внутренний пользовательский интерфейс должен быть создан автором пакета, поведение полного пользовательского интерфейса, сокращенного ПОЛЬЗОВАТЕЛЬСКОГО интерфейса, базового интерфейса пользователя и уровней None зависит от установочного пакета.</span><span class="sxs-lookup"><span data-stu-id="c07c5-105">Because the internal UI must be created by the author of the package, the behavior of the full UI, reduced UI, basic UI, and None levels depends on the installation package.</span></span> <span data-ttu-id="c07c5-106">В следующей таблице описаны функциональные возможности, обычно приписываемое на уровни пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c07c5-106">The following table describes the functionality commonly ascribed to UI levels.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c07c5-107">Уровень пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c07c5-107">UI Level</span></span></th>
<th><span data-ttu-id="c07c5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c07c5-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c07c5-109">Полный пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="c07c5-109">Full UI</span></span></td>
<td><span data-ttu-id="c07c5-110">Отображает модальные и немодальные диалоговые окна, созданные во внутреннем пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c07c5-110">Displays modal and modeless dialog boxes that have been authored into the internal UI.</span></span> <span data-ttu-id="c07c5-111">Отображение <a href="error-dialog.md">диалоговых окон созданные ошибки</a> .</span><span class="sxs-lookup"><span data-stu-id="c07c5-111">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c07c5-112">Для продолжения установки модальные диалоговые окна должны вводиться пользователем, и они задаются путем установки <a href="modal-dialog-style-bit.md">бита модального стиля диалогового окна</a> в столбце Attributes (атрибуты) в таблице <a href="dialog-table.md">диалоговых окон</a> .</span><span class="sxs-lookup"><span data-stu-id="c07c5-112">Modal dialog boxes require user input before the installation can continue and are specified by setting the <a href="modal-dialog-style-bit.md">Modal Dialog Style Bit</a> in the Attributes column of the <a href="dialog-table.md">Dialog</a> table.</span></span> <span data-ttu-id="c07c5-113">Немодальное диалоговое окно не требует ввода данных пользователем для продолжения установки.</span><span class="sxs-lookup"><span data-stu-id="c07c5-113">A modeless dialog box does not require user input for the installation to continue.</span></span>
</blockquote>
<br/> <span data-ttu-id="c07c5-114">Весь пользовательский интерфейс обычно имеет <a href="user-interface-wizard-behavior.md">поведение мастера пользовательского интерфейса</a>.</span><span class="sxs-lookup"><span data-stu-id="c07c5-114">A full UI commonly exhibits <a href="user-interface-wizard-behavior.md">User Interface Wizard Behavior</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c07c5-115">Сокращенный пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="c07c5-115">Reduced UI</span></span></td>
<td><span data-ttu-id="c07c5-116">Отображает все немодальные диалоговые окна, созданные в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c07c5-116">Displays any modeless dialog boxes that have been authored into the UI.</span></span> <span data-ttu-id="c07c5-117">Не отображает созданные модальные диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="c07c5-117">Does not display any authored modal dialog boxes.</span></span> <span data-ttu-id="c07c5-118">Отображение <a href="error-dialog.md">диалоговых окон созданные ошибки</a> .</span><span class="sxs-lookup"><span data-stu-id="c07c5-118">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span> <span data-ttu-id="c07c5-119">Отображает сообщения о <a href="authoring-disk-prompt-messages.md">запросах к диску</a> .</span><span class="sxs-lookup"><span data-stu-id="c07c5-119">Displays <a href="authoring-disk-prompt-messages.md">Disk Prompt</a> messages.</span></span> <span data-ttu-id="c07c5-120">Отображает <a href="filesinuse-dialog.md">диалоговые окна филесинусе</a> .</span><span class="sxs-lookup"><span data-stu-id="c07c5-120">Displays <a href="filesinuse-dialog.md">FilesInUse Dialog</a> boxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c07c5-121">Базовый пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="c07c5-121">Basic UI</span></span></td>
<td><span data-ttu-id="c07c5-122">Отображает встроенные немодальные диалоговые окна, отображающие сообщения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="c07c5-122">Displays the built-in modeless dialog boxes that show progress messages.</span></span> <span data-ttu-id="c07c5-123">Отображение встроенных диалоговых окон ошибок.</span><span class="sxs-lookup"><span data-stu-id="c07c5-123">Displays built-in error dialog boxes.</span></span> <span data-ttu-id="c07c5-124">Не отображает ни одного созданного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="c07c5-124">Does not display any authored dialog boxes.</span></span> <span data-ttu-id="c07c5-125">Предлагает пользователям вставить диск, отображая диалоговое окно, содержащее значение свойства <a href="diskprompt.md"><strong>DiskPrompt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c07c5-125">Prompts users to insert a disk by displaying a dialog box containing the <a href="diskprompt.md"><strong>DiskPrompt</strong></a> property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c07c5-126">Нет</span><span class="sxs-lookup"><span data-stu-id="c07c5-126">None</span></span></td>
<td><span data-ttu-id="c07c5-127">Нет — автоматическая установка, которая не отображает пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c07c5-127">None means a silent installation that displays no UI.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c07c5-128">Уровень внутреннего пользовательского интерфейса можно задать с помощью [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="c07c5-128">The level of the internal UI can be set using [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="c07c5-129">Установщик задает для свойства [**duilevel**](uilevel.md) текущий уровень пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c07c5-129">The installer sets the [**UILevel**](uilevel.md) property to the current level of the UI.</span></span>

<span data-ttu-id="c07c5-130">Если задано свойство [**лимитуи**](limitui.md) , то уровень пользовательского интерфейса, используемый при установке пакета, ограничен базовым.</span><span class="sxs-lookup"><span data-stu-id="c07c5-130">If the [**LIMITUI**](limitui.md) property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span>

<span data-ttu-id="c07c5-131">Пример создания пользовательского интерфейса см. [в примере установки](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="c07c5-131">For an example of UI authoring, see [An Installation Example](an-installation-example.md).</span></span>

 

 




