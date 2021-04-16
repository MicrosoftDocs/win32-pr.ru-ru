---
description: Почтовый слот — это псеудофиле, который находится в памяти, и для доступа к нему используются стандартные файловые функции.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: О Маилслотс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664703"
---
# <a name="about-mailslots"></a><span data-ttu-id="82180-103">О Маилслотс</span><span class="sxs-lookup"><span data-stu-id="82180-103">About Mailslots</span></span>

<span data-ttu-id="82180-104">Почтовый слот — это псеудофиле, который находится в памяти, и для доступа к нему используются стандартные файловые функции.</span><span class="sxs-lookup"><span data-stu-id="82180-104">A mailslot is a pseudofile that resides in memory, and you use standard file functions to access it.</span></span> <span data-ttu-id="82180-105">Данные в сообщении слота могут быть в любой форме, но не могут быть больше 424 байт при передаче между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="82180-105">The data in a mailslot message can be in any form, but cannot be larger than 424 bytes when sent between computers.</span></span> <span data-ttu-id="82180-106">В отличие от файлов на диске, маилслотс являются временными.</span><span class="sxs-lookup"><span data-stu-id="82180-106">Unlike disk files, mailslots are temporary.</span></span> <span data-ttu-id="82180-107">Когда все дескрипторы слота закрываются, почтовый слот и все содержащиеся в нем данные удаляются.</span><span class="sxs-lookup"><span data-stu-id="82180-107">When all handles to a mailslot are closed, the mailslot and all the data it contains are deleted.</span></span>

<span data-ttu-id="82180-108">*Сервер слота* — это процесс, который создает и владеет слотом сообщений.</span><span class="sxs-lookup"><span data-stu-id="82180-108">A *mailslot server* is a process that creates and owns a mailslot.</span></span> <span data-ttu-id="82180-109">Когда сервер создает почтовый слот, он получает обработчик слота.</span><span class="sxs-lookup"><span data-stu-id="82180-109">When the server creates a mailslot, it receives a mailslot handle.</span></span> <span data-ttu-id="82180-110">Этот обработчик следует использовать, когда процесс считывает сообщения из слота сообщений.</span><span class="sxs-lookup"><span data-stu-id="82180-110">This handle must be used when a process reads messages from the mailslot.</span></span> <span data-ttu-id="82180-111">Только процесс, создающий почтовый слот или получивший маркер другим механизмом (например, наследованием), может считывать из слота сообщений.</span><span class="sxs-lookup"><span data-stu-id="82180-111">Only the process that creates a mailslot or has obtained the handle by some other mechanism (such as inheritance) can read from the mailslot.</span></span> <span data-ttu-id="82180-112">Все маилслотс являются локальными для процесса, который их создает.</span><span class="sxs-lookup"><span data-stu-id="82180-112">All mailslots are local to the process that creates them.</span></span> <span data-ttu-id="82180-113">Процессу не удается создать удаленный почтовый слот.</span><span class="sxs-lookup"><span data-stu-id="82180-113">A process cannot create a remote mailslot.</span></span>

<span data-ttu-id="82180-114">*Клиент слота* — это процесс, записывающий сообщение в почтовый слот.</span><span class="sxs-lookup"><span data-stu-id="82180-114">A *mailslot client* is a process that writes a message to a mailslot.</span></span> <span data-ttu-id="82180-115">Любой процесс, имеющий имя слота сообщений, может разместить в нем сообщение.</span><span class="sxs-lookup"><span data-stu-id="82180-115">Any process that has the name of a mailslot can put a message there.</span></span> <span data-ttu-id="82180-116">Новые сообщения следуют всем существующим сообщениям в слоте сообщений.</span><span class="sxs-lookup"><span data-stu-id="82180-116">New messages follow any existing messages in the mailslot.</span></span>

<span data-ttu-id="82180-117">Маилслотс может рассылать сообщения внутри домена.</span><span class="sxs-lookup"><span data-stu-id="82180-117">Mailslots can broadcast messages within a domain.</span></span> <span data-ttu-id="82180-118">Если несколько процессов в домене создают почтовый слот с одним и тем же именем, то каждое сообщение, адресованное этому слоту и отправленное в домен, получается участвующими процессами.</span><span class="sxs-lookup"><span data-stu-id="82180-118">If several processes in a domain each create a mailslot using the same name, every message that is addressed to that mailslot and sent to the domain is received by the participating processes.</span></span> <span data-ttu-id="82180-119">Поскольку один процесс может управлять как обработчиком слота сервера, так и полученным при открытии слотом сообщений для операции записи, приложения могут легко реализовать простой механизм передачи сообщений в домене.</span><span class="sxs-lookup"><span data-stu-id="82180-119">Because one process can control both a server mailslot handle and the client handle retrieved when the mailslot is opened for a write operation, applications can easily implement a simple message-passing facility within a domain.</span></span>

<span data-ttu-id="82180-120">Для отправки сообщений размером более 424 байт между компьютерами используйте [именованные каналы](named-pipes.md) или [сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2) .</span><span class="sxs-lookup"><span data-stu-id="82180-120">To send messages that are larger than 424 bytes between computers, use [named pipes](named-pipes.md) or [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82180-121">См. также</span><span class="sxs-lookup"><span data-stu-id="82180-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82180-122">Имена слотов</span><span class="sxs-lookup"><span data-stu-id="82180-122">Mailslot Names</span></span>](mailslot-names.md)
</dt> <dt>

[<span data-ttu-id="82180-123">Операции с слотом</span><span class="sxs-lookup"><span data-stu-id="82180-123">Mailslot Operations</span></span>](mailslot-operations.md)
</dt> </dl>

 

 
