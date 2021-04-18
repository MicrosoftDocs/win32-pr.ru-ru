---
description: Следуйте приведенным ниже рекомендациям, чтобы создать установщик Windowsную установку, в которой отображается окно сообщения, предлагающее пользователю вставить диск.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Создание сообщений с приглашением на диск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650726"
---
# <a name="authoring-disk-prompt-messages"></a><span data-ttu-id="129ff-103">Создание сообщений с приглашением на диск</span><span class="sxs-lookup"><span data-stu-id="129ff-103">Authoring Disk Prompt Messages</span></span>

<span data-ttu-id="129ff-104">Следуйте приведенным ниже рекомендациям, чтобы создать установщик Windowsную установку, в которой отображается окно сообщения, предлагающее пользователю вставить диск.</span><span class="sxs-lookup"><span data-stu-id="129ff-104">Use the following guidelines to author a Windows Installer installation that displays a message box prompting the user to insert a disk.</span></span>

<span data-ttu-id="129ff-105">**Отображение окна сообщения, предлагающего пользователю вставить диск**</span><span class="sxs-lookup"><span data-stu-id="129ff-105">**To display a message box prompting the user to insert a disk**</span></span>

1.  <span data-ttu-id="129ff-106">Используйте возможности установщика, чтобы задать строку свойства [**DiskPrompt**](diskprompt.md) в таблице [свойств](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="129ff-106">Use the authoring capabilities of the installer to set the [**DiskPrompt**](diskprompt.md) property string in the [Property](property-table.md) table.</span></span> <span data-ttu-id="129ff-107">Оно должно включать имя устанавливаемого продукта и параметр заполнителя в строке для заголовка, напечатанного на диске.</span><span class="sxs-lookup"><span data-stu-id="129ff-107">This should include the name of the product being installed and a placeholder parameter within the string for the title printed on the disk.</span></span> <span data-ttu-id="129ff-108">Например, для Microsoft Publisher свойство **DiskPrompt** может иметь значение «Microsoft Publisher: Disk \[ 1 \] », где \[ 1 \] — это заполнитель для названия диска.</span><span class="sxs-lookup"><span data-stu-id="129ff-108">For example, for Microsoft Publisher the **DiskPrompt** property could be "Microsoft Publisher: Disk \[1\]", where \[1\] is the placeholder for the disk title.</span></span>
2.  <span data-ttu-id="129ff-109">Введите заголовки каждого из дисков, которые будут запрашиваться, в отдельные строки столбца DiskPrompt таблицы [Media](media-table.md) .</span><span class="sxs-lookup"><span data-stu-id="129ff-109">Enter the titles of each of the disks being prompted for into separate rows of the DiskPrompt column of the [Media](media-table.md) table.</span></span> <span data-ttu-id="129ff-110">Например, первая и только запись в таблицу Media может иметь значение «1 – install».</span><span class="sxs-lookup"><span data-stu-id="129ff-110">For example, the first and only entry into the Media table could be "1–Install."</span></span>
3.  <span data-ttu-id="129ff-111">Во время действия [инсталлфилес](installfiles-action.md) значение из столбца DiskPrompt таблицы [Media](media-table.md) заменяется на заполнитель в строке свойства [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="129ff-111">During the [InstallFiles](installfiles-action.md) action the value from the DiskPrompt column of the [Media](media-table.md) table is substituted for the placeholder in the string of the [**DiskPrompt**](diskprompt.md) property.</span></span>
4.  <span data-ttu-id="129ff-112">Сообщение, отображаемое окном сообщения, создается из встроенной строки шаблона в [таблице ошибок](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="129ff-112">The message displayed by the message box is created from a built-in template string in the [Error table](error-table.md).</span></span> <span data-ttu-id="129ff-113">Это ошибка 1302, и строка шаблона: "Вставьте диск: \[ 2 \] ", а \[ 2 \] — заполнитель для свойства [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="129ff-113">This is Error 1302 and the template string is: "Please insert the disk: \[2\]", and the \[2\] represents a placeholder for the [**DiskPrompt**](diskprompt.md) property.</span></span>

<span data-ttu-id="129ff-114">В примере отображается следующее сообщение для пользователя: "Вставьте диск: Microsoft Publisher: Disk 1 — Install".</span><span class="sxs-lookup"><span data-stu-id="129ff-114">The example displays the following message to the user: "Please insert the disk: Microsoft Publisher: Disk 1 – Install."</span></span>

<span data-ttu-id="129ff-115">Обратите внимание, что сообщения с приглашением на диск отображаются всеми [уровнями пользовательского интерфейса](user-interface-levels.md) , кроме None.</span><span class="sxs-lookup"><span data-stu-id="129ff-115">Note that disk prompt messages get displayed by all [User Interface Levels](user-interface-levels.md) except None.</span></span>

 

 



