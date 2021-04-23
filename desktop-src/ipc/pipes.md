---
description: Создание, управление и использование каналов. Канал — это раздел общей памяти, используемый процессами для обмена данными. Процесс, создающий канал, является сервером канала. Процесс, который подключается к каналу, является клиентом канала.
ms.assetid: 7cb8cbe4-eec8-4dda-9cb7-8d37abcee6f4
title: Каналы (взаимодействие между процессами)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e84d3cb9354aca2cbab1e077c228070e62d6783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693304"
---
# <a name="pipes-interprocess-communications"></a><span data-ttu-id="46a1c-106">Каналы (взаимодействие между процессами)</span><span class="sxs-lookup"><span data-stu-id="46a1c-106">Pipes (Interprocess Communications)</span></span>

<span data-ttu-id="46a1c-107">*Канал* — это раздел общей памяти, используемый процессами для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="46a1c-107">A *pipe* is a section of shared memory that processes use for communication.</span></span> <span data-ttu-id="46a1c-108">Процесс, создающий канал, является *сервером канала*.</span><span class="sxs-lookup"><span data-stu-id="46a1c-108">The process that creates a pipe is the *pipe server*.</span></span> <span data-ttu-id="46a1c-109">Процесс, который подключается к каналу, является *клиентом канала*.</span><span class="sxs-lookup"><span data-stu-id="46a1c-109">A process that connects to a pipe is a *pipe client*.</span></span> <span data-ttu-id="46a1c-110">Один процесс записывает сведения в канал, а другой процесс считывает информацию из канала.</span><span class="sxs-lookup"><span data-stu-id="46a1c-110">One process writes information to the pipe, then the other process reads the information from the pipe.</span></span> <span data-ttu-id="46a1c-111">В этом обзоре описывается создание, управление и использование каналов.</span><span class="sxs-lookup"><span data-stu-id="46a1c-111">This overview describes how to create, manage, and use pipes.</span></span>

-   [<span data-ttu-id="46a1c-112">О каналах</span><span class="sxs-lookup"><span data-stu-id="46a1c-112">About Pipes</span></span>](about-pipes.md)
-   [<span data-ttu-id="46a1c-113">Использование каналов</span><span class="sxs-lookup"><span data-stu-id="46a1c-113">Using Pipes</span></span>](using-pipes.md)
-   [<span data-ttu-id="46a1c-114">Ссылка на канал</span><span class="sxs-lookup"><span data-stu-id="46a1c-114">Pipe Reference</span></span>](pipe-reference.md)

 

 



