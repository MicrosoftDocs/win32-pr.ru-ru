---
description: Блок среды потока (заметки об отладке)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Блок среды потока (заметки об отладке)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895910"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="585b5-103">Блок среды потока (заметки об отладке)</span><span class="sxs-lookup"><span data-stu-id="585b5-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="585b5-104">Блок среды потока ([**Структура Теб**](/windows/win32/api/winternl/ns-winternl-teb)) содержит сведения о контексте для потока.</span><span class="sxs-lookup"><span data-stu-id="585b5-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="585b5-105">В следующих версиях Windows смещение 32-разрядного адреса ТЕБ в 64-бит ТЕБ равно 0.</span><span class="sxs-lookup"><span data-stu-id="585b5-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="585b5-106">Это можно использовать для прямого доступа к 32-разрядному ТЕБ потока WOW64.</span><span class="sxs-lookup"><span data-stu-id="585b5-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="585b5-107">Это может измениться в более поздних версиях Windows</span><span class="sxs-lookup"><span data-stu-id="585b5-107">This might change in later versions of Windows</span></span>



|               |                        |
|---------------|------------------------|
| <span data-ttu-id="585b5-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="585b5-108">Windows Vista</span></span> | <span data-ttu-id="585b5-109">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="585b5-109">Windows Server 2008</span></span>    |
| <span data-ttu-id="585b5-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="585b5-110">Windows 7</span></span>     | <span data-ttu-id="585b5-111">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="585b5-111">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="585b5-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="585b5-112">Windows 8</span></span>     | <span data-ttu-id="585b5-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="585b5-113">Windows Server 2012</span></span>    |
| <span data-ttu-id="585b5-114">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="585b5-114">Windows 8.1</span></span>   | <span data-ttu-id="585b5-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="585b5-115">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="585b5-116">См. также</span><span class="sxs-lookup"><span data-stu-id="585b5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="585b5-117">Структуры отладки</span><span class="sxs-lookup"><span data-stu-id="585b5-117">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="585b5-118">**\_Контекст WOW64**</span><span class="sxs-lookup"><span data-stu-id="585b5-118">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
