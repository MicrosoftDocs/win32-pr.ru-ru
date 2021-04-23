---
description: Каждый именованный канал имеет уникальное имя, которое отличает его от других именованных каналов в списке систем именованных объектов. Сервер канала задает имя канала при вызове функции Креатенамедпипе для создания одного или нескольких экземпляров именованного канала.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Имена каналов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684298"
---
# <a name="pipe-names"></a><span data-ttu-id="82e28-104">Имена каналов</span><span class="sxs-lookup"><span data-stu-id="82e28-104">Pipe Names</span></span>

<span data-ttu-id="82e28-105">Каждый именованный канал имеет уникальное имя, которое отличает его от других именованных каналов в списке именованных объектов системы.</span><span class="sxs-lookup"><span data-stu-id="82e28-105">Each named pipe has a unique name that distinguishes it from other named pipes in the system's list of named objects.</span></span> <span data-ttu-id="82e28-106">Сервер канала задает имя канала при вызове функции [**креатенамедпипе**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) для создания одного или нескольких экземпляров именованного канала.</span><span class="sxs-lookup"><span data-stu-id="82e28-106">A pipe server specifies a name for the pipe when it calls the [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) function to create one or more instances of a named pipe.</span></span> <span data-ttu-id="82e28-107">Клиенты канала указывают имя канала при вызове функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) или [**каллнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) для подключения к экземпляру именованного канала.</span><span class="sxs-lookup"><span data-stu-id="82e28-107">Pipe clients specify the pipe name when they call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function to connect to an instance of the named pipe.</span></span>

<span data-ttu-id="82e28-108">При указании имени канала в функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**ваитнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)или [**каллнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) используйте следующую форму:</span><span class="sxs-lookup"><span data-stu-id="82e28-108">Use the following form when specifying the name of a pipe in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea), or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function:</span></span>

<span data-ttu-id="82e28-109">\\\\*Имя сервера* \\ \\*PipeName* канала</span><span class="sxs-lookup"><span data-stu-id="82e28-109">\\\\*ServerName*\\pipe\\*PipeName*</span></span>

<span data-ttu-id="82e28-110">где *ServerName* — это либо имя удаленного компьютера, либо точка, чтобы указать локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="82e28-110">where *ServerName* is either the name of a remote computer or a period, to specify the local computer.</span></span> <span data-ttu-id="82e28-111">Строка имени канала, заданная параметром *PipeName* , может содержать любой символ, кроме обратной косой черты, включая цифры и специальные символы.</span><span class="sxs-lookup"><span data-stu-id="82e28-111">The pipe name string specified by *PipeName* can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="82e28-112">Длина строки имени канала может доставлять до 256 символов.</span><span class="sxs-lookup"><span data-stu-id="82e28-112">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="82e28-113">Имена каналов не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="82e28-113">Pipe names are not case-sensitive.</span></span>

<span data-ttu-id="82e28-114">Серверу канала не удается создать канал на другом компьютере, поэтому [**креатенамедпипе**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) должен использовать точку для имени сервера, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="82e28-114">The pipe server cannot create a pipe on another computer, so [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) must use a period for the server name, as shown in the following example.</span></span>

<span data-ttu-id="82e28-115">\\\\.\\ \\*PipeName* канала</span><span class="sxs-lookup"><span data-stu-id="82e28-115">\\\\.\\pipe\\*PipeName*</span></span>

<span data-ttu-id="82e28-116">Сервер канала может предоставить имя канала клиентам канала, чтобы они могли подключаться к каналу.</span><span class="sxs-lookup"><span data-stu-id="82e28-116">A pipe server can provide the pipe name to its pipe clients, so they can connect to the pipe.</span></span> <span data-ttu-id="82e28-117">Клиент канала обнаруживает имя канала из некоторого постоянного источника, например запись реестра, файл или другое приложение.</span><span class="sxs-lookup"><span data-stu-id="82e28-117">The pipe client discovers the pipe name from some persistent source, such as a registry entry, a file, or another application.</span></span> <span data-ttu-id="82e28-118">В противном случае клиенты должны иметь имя канала во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="82e28-118">Otherwise, the clients must know the pipe name at compile time.</span></span>

 

 
