---
description: Функции виртуальной памяти управляют страницами памяти. Функции используют размер страницы на текущем компьютере для округления указанных размеров и адресов.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Выделение виртуальной памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345372"
---
# <a name="allocating-virtual-memory"></a><span data-ttu-id="f0b5a-104">Выделение виртуальной памяти</span><span class="sxs-lookup"><span data-stu-id="f0b5a-104">Allocating Virtual Memory</span></span>

<span data-ttu-id="f0b5a-105">Функции виртуальной памяти управляют страницами памяти.</span><span class="sxs-lookup"><span data-stu-id="f0b5a-105">The virtual memory functions manipulate pages of memory.</span></span> <span data-ttu-id="f0b5a-106">Функции используют размер страницы на текущем компьютере для округления указанных размеров и адресов.</span><span class="sxs-lookup"><span data-stu-id="f0b5a-106">The functions use the size of a page on the current computer to round off specified sizes and addresses.</span></span>

<span data-ttu-id="f0b5a-107">Функция [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) выполняет одну из следующих операций:</span><span class="sxs-lookup"><span data-stu-id="f0b5a-107">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function performs one of the following operations:</span></span>

-   <span data-ttu-id="f0b5a-108">Резервирует одну или несколько бесплатных страниц.</span><span class="sxs-lookup"><span data-stu-id="f0b5a-108">Reserves one or more free pages.</span></span>
-   <span data-ttu-id="f0b5a-109">Фиксирует одну или несколько зарезервированных страниц.</span><span class="sxs-lookup"><span data-stu-id="f0b5a-109">Commits one or more reserved pages.</span></span>
-   <span data-ttu-id="f0b5a-110">Резервирует и фиксирует одну или несколько свободных страниц.</span><span class="sxs-lookup"><span data-stu-id="f0b5a-110">Reserves and commits one or more free pages.</span></span>

<span data-ttu-id="f0b5a-111">Можно указать начальный адрес зарезервированных или зафиксированных страниц или разрешить системе определять адрес.</span><span class="sxs-lookup"><span data-stu-id="f0b5a-111">You can specify the starting address of the pages to be reserved or committed, or you can allow the system to determine the address.</span></span> <span data-ttu-id="f0b5a-112">Функция округляет указанный адрес до соответствующей границы страницы.</span><span class="sxs-lookup"><span data-stu-id="f0b5a-112">The function rounds the specified address to the appropriate page boundary.</span></span> <span data-ttu-id="f0b5a-113">Зарезервированные страницы недоступны, но зафиксированные страницы могут быть распределены по **страницам \_ ReadWrite**, **\_ ReadOnly** или Page без доступа к **\_ данным** .</span><span class="sxs-lookup"><span data-stu-id="f0b5a-113">Reserved pages are not accessible, but committed pages can be allocated with **PAGE\_READWRITE**, **PAGE\_READONLY**, or **PAGE\_NOACCESS** access.</span></span> <span data-ttu-id="f0b5a-114">При фиксации страниц плата за память выделяется из общего размера файлов ОЗУ и подкачки на диске, но каждая страница инициализируется и загружается в физическую память только при первой попытке чтения или записи на эту страницу.</span><span class="sxs-lookup"><span data-stu-id="f0b5a-114">When pages are committed, memory charges are allocated from the overall size of RAM and paging files on disk, but each page is initialized and loaded into physical memory only at the first attempt to read from or write to that page.</span></span> <span data-ttu-id="f0b5a-115">Для доступа к памяти, зафиксированной функцией [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) , можно использовать ссылки на обычные указатели.</span><span class="sxs-lookup"><span data-stu-id="f0b5a-115">You can use normal pointer references to access memory committed by the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function.</span></span>

 

 
