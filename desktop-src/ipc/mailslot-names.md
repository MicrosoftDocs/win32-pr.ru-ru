---
description: Именование маилслотс и помещение сообщений в маилслотс.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Имена слотов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808416"
---
# <a name="mailslot-names"></a><span data-ttu-id="84e48-103">Имена слотов</span><span class="sxs-lookup"><span data-stu-id="84e48-103">Mailslot Names</span></span>

<span data-ttu-id="84e48-104">Когда процесс создает почтовый слот, имя слота должно иметь следующую форму.</span><span class="sxs-lookup"><span data-stu-id="84e48-104">When a process creates a mailslot, the mailslot name must have the following form.</span></span>

<span data-ttu-id="84e48-105">\\\\.\\ \\ \[ *имя пути к* \\ \]  слоту</span><span class="sxs-lookup"><span data-stu-id="84e48-105">\\\\.\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="84e48-106">Для имени почтового слота требуются следующие элементы: две обратные косые черты, чтобы начать имя, точку, обратную косую черту после точки, слово «почтовый слот» и обратную косую черту.</span><span class="sxs-lookup"><span data-stu-id="84e48-106">A mailslot name requires the following elements: two backslashes to begin the name, a period, a backslash following the period, the word "mailslot", and a trailing backslash.</span></span> <span data-ttu-id="84e48-107">В именах регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="84e48-107">Names are not case sensitive.</span></span> <span data-ttu-id="84e48-108">Имени слота может предшествовать путь, состоящий из имен одного или нескольких каталогов, разделенных символами обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="84e48-108">A mailslot name can be preceded by a path consisting of the names of one or more directories, separated by backslashes.</span></span> <span data-ttu-id="84e48-109">Например, если пользователь ожидает сообщения в теме налогов от Боба, Петров и Сью, то пользовательское почтовое сообщение может позволить пользователю создавать отдельные маилслотс для каждого отправителя, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="84e48-109">For example, if a user expects messages on the subject of taxes from Bob, Pete, and Sue, the user's mailslot application might allow the user to create individual mailslots for each sender, as shown here:</span></span><dl> <span data-ttu-id="84e48-110">\\\\.\\ \\ \\ bobsные комментарии налогов слотов \_</span><span class="sxs-lookup"><span data-stu-id="84e48-110">\\\\.\\mailslot\\taxes\\bobs\_comments</span></span>  
<span data-ttu-id="84e48-111">\\\\.\\ \\Комментарии о налогах на почтовый слот \\ \_</span><span class="sxs-lookup"><span data-stu-id="84e48-111">\\\\.\\mailslot\\taxes\\petes\_comments</span></span>  
<span data-ttu-id="84e48-112">\\\\.\\ \\ \\ скоростьные комментарии налогов слотов \_</span><span class="sxs-lookup"><span data-stu-id="84e48-112">\\\\.\\mailslot\\taxes\\sues\_comments</span></span>  
</dl>

<span data-ttu-id="84e48-113">Чтобы вставить сообщение в почтовый слот, процесс открывает почтовый слот по имени.</span><span class="sxs-lookup"><span data-stu-id="84e48-113">To put a message into a mailslot, a process opens a mailslot by name.</span></span> <span data-ttu-id="84e48-114">Для записи в почтовый слот на локальном компьютере процесс может использовать имя слота, имеющее ту же форму, что и для создания слота.</span><span class="sxs-lookup"><span data-stu-id="84e48-114">To write to a mailslot on the local computer, a process can use a mailslot name that has the same form used for creating a mailslot.</span></span> <span data-ttu-id="84e48-115">Эта ситуация, однако, довольно редки.</span><span class="sxs-lookup"><span data-stu-id="84e48-115">This situation, however, is relatively uncommon.</span></span> <span data-ttu-id="84e48-116">Чаще для записи в почтовый слот на определенном удаленном компьютере используется следующая форма:</span><span class="sxs-lookup"><span data-stu-id="84e48-116">More frequently, you would use the following form to write to a mailslot on a specific remote computer:</span></span>

<span data-ttu-id="84e48-117">\\\\*Имя компьютера* \\ \\ \[ *имя пути к* \\ \]  слоту</span><span class="sxs-lookup"><span data-stu-id="84e48-117">\\\\*ComputerName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="84e48-118">Чтобы разместить сообщение в каждом слоте указанного домена с заданным именем, используйте следующую форму:</span><span class="sxs-lookup"><span data-stu-id="84e48-118">To put a message into every mailslot in the specified domain with a given name, use the following form:</span></span>

<span data-ttu-id="84e48-119">\\\\*Имя_домена* \\ \\ \[ *имя пути к* \\ \]  слоту</span><span class="sxs-lookup"><span data-stu-id="84e48-119">\\\\*DomainName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="84e48-120">Чтобы разместить сообщение в каждом слоте с заданным именем в основном домене системы, используйте следующую форму:</span><span class="sxs-lookup"><span data-stu-id="84e48-120">To put a message into every mailslot with a given name in the system's primary domain, use the following form:</span></span>

<span data-ttu-id="84e48-121">\\\\\*\\\\ \[ *имя пути к* \\ \]  слоту</span><span class="sxs-lookup"><span data-stu-id="84e48-121">\\\\\*\\mailslot\\\[*path*\\\]*name*</span></span>

 

 



