---
description: Описание функций, используемых при работе с маилслотс, клиентами и серверами.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Операции с слотом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712063"
---
# <a name="mailslot-operations"></a><span data-ttu-id="c664c-103">Операции с слотом</span><span class="sxs-lookup"><span data-stu-id="c664c-103">Mailslot Operations</span></span>

<span data-ttu-id="c664c-104">При работе с маилслотс клиенты и серверы должны использовать только функции, описанные в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="c664c-104">When working with mailslots, clients and servers should use only the functions discussed in the following tables.</span></span> <span data-ttu-id="c664c-105">Не используйте другие функции, даже если они принимают дескрипторы файлов или имена файлов в качестве параметров, так как они не предназначены для работы с маилслотс.</span><span class="sxs-lookup"><span data-stu-id="c664c-105">Do not use other functions, even if they accept file handles or file names as parameters, as they are not designed to work with mailslots.</span></span>

## <a name="mailslot-server-functions"></a><span data-ttu-id="c664c-106">Функции сервера слота</span><span class="sxs-lookup"><span data-stu-id="c664c-106">Mailslot Server Functions</span></span>

<span data-ttu-id="c664c-107">Серверы слота имеют эксклюзивное использование трех функций, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c664c-107">Mailslot servers have exclusive use of three functions, as shown in the following table.</span></span>



| <span data-ttu-id="c664c-108">Функция</span><span class="sxs-lookup"><span data-stu-id="c664c-108">Function</span></span>                                   | <span data-ttu-id="c664c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c664c-109">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c664c-110">**креатемаилслот**</span><span class="sxs-lookup"><span data-stu-id="c664c-110">**CreateMailslot**</span></span>](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | <span data-ttu-id="c664c-111">Создает почтовый слот и возвращает маркер в виде слота.</span><span class="sxs-lookup"><span data-stu-id="c664c-111">Creates a mailslot and returns a mailslot handle.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="c664c-112">**жетмаилслотинфо**</span><span class="sxs-lookup"><span data-stu-id="c664c-112">**GetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | <span data-ttu-id="c664c-113">Извлекает максимальный размер сообщения, Размер слота, размер следующего сообщения в слоте, количество сообщений в слоте и время, в течение которого операция чтения может ожидать сообщения.</span><span class="sxs-lookup"><span data-stu-id="c664c-113">Retrieves the maximum message size, the mailslot size, the size of the next message in the mailslot, the number of messages in the mailslot, and the amount of time a read operation can wait for a message.</span></span> |
| [<span data-ttu-id="c664c-114">**сетмаилслотинфо**</span><span class="sxs-lookup"><span data-stu-id="c664c-114">**SetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | <span data-ttu-id="c664c-115">Изменяет время ожидания чтения для слота сообщений.</span><span class="sxs-lookup"><span data-stu-id="c664c-115">Changes the read time-out for a mailslot.</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="c664c-116">В качестве серверов слота также используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="c664c-116">The following functions are also used by mailslot servers.</span></span>



| <span data-ttu-id="c664c-117">Функция</span><span class="sxs-lookup"><span data-stu-id="c664c-117">Function</span></span>                                                         | <span data-ttu-id="c664c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c664c-118">Description</span></span>                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="c664c-119">**дупликатехандле**</span><span class="sxs-lookup"><span data-stu-id="c664c-119">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | <span data-ttu-id="c664c-120">Дублирует обработчик слота.</span><span class="sxs-lookup"><span data-stu-id="c664c-120">Duplicates the mailslot handle.</span></span>                     |
| <span data-ttu-id="c664c-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **реадфиликс**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span><span class="sxs-lookup"><span data-stu-id="c664c-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span></span> | <span data-ttu-id="c664c-122">Извлекает сообщения из слота сообщений.</span><span class="sxs-lookup"><span data-stu-id="c664c-122">Retrieves messages from a mailslot.</span></span>                 |
| [<span data-ttu-id="c664c-123">**Функции getFileTime**</span><span class="sxs-lookup"><span data-stu-id="c664c-123">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="c664c-124">Извлекает дату и время создания почтового слота.</span><span class="sxs-lookup"><span data-stu-id="c664c-124">Retrieves the date and time a mailslot was created.</span></span> |
| [<span data-ttu-id="c664c-125">**сетфилетиме**</span><span class="sxs-lookup"><span data-stu-id="c664c-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="c664c-126">Задает дату и время создания почтового слота.</span><span class="sxs-lookup"><span data-stu-id="c664c-126">Sets the date and time a mailslot was created.</span></span>      |
| [<span data-ttu-id="c664c-127">**жесандлеинформатион**</span><span class="sxs-lookup"><span data-stu-id="c664c-127">**GetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | <span data-ttu-id="c664c-128">Извлекает свойства обработчика слота сообщений.</span><span class="sxs-lookup"><span data-stu-id="c664c-128">Retrieves properties of the mailslot handle.</span></span>        |
| [<span data-ttu-id="c664c-129">**сесандлеинформатион**</span><span class="sxs-lookup"><span data-stu-id="c664c-129">**SetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | <span data-ttu-id="c664c-130">Задает свойства обработчика слота.</span><span class="sxs-lookup"><span data-stu-id="c664c-130">Sets properties of the mailslot handle.</span></span>             |



 

## <a name="mailslot-client-functions"></a><span data-ttu-id="c664c-131">Клиентские функции слота</span><span class="sxs-lookup"><span data-stu-id="c664c-131">Mailslot Client Functions</span></span>

<span data-ttu-id="c664c-132">При взаимодействии с слотом клиентский процесс использует следующие функции.</span><span class="sxs-lookup"><span data-stu-id="c664c-132">A client process uses the following functions when interacting with a mailslot.</span></span>



| <span data-ttu-id="c664c-133">Функция</span><span class="sxs-lookup"><span data-stu-id="c664c-133">Function</span></span>                                                             | <span data-ttu-id="c664c-134">Описание</span><span class="sxs-lookup"><span data-stu-id="c664c-134">Description</span></span>                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="c664c-135">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="c664c-135">**CloseHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | <span data-ttu-id="c664c-136">Закрывает обработчик слота для клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="c664c-136">Closes a mailslot handle for a client process.</span></span>  |
| [<span data-ttu-id="c664c-137">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="c664c-137">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | <span data-ttu-id="c664c-138">Создает обработчик в слоте для клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="c664c-138">Creates a mailslot handle for a client process.</span></span> |
| [<span data-ttu-id="c664c-139">**дупликатехандле**</span><span class="sxs-lookup"><span data-stu-id="c664c-139">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | <span data-ttu-id="c664c-140">Дублирует обработчик слота.</span><span class="sxs-lookup"><span data-stu-id="c664c-140">Duplicates a mailslot handle.</span></span>                   |
| <span data-ttu-id="c664c-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **вритефиликс**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span><span class="sxs-lookup"><span data-stu-id="c664c-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span></span> | <span data-ttu-id="c664c-142">Записывает данные в почтовый слот.</span><span class="sxs-lookup"><span data-stu-id="c664c-142">Writes data to a mailslot.</span></span>                      |



 

 

 
