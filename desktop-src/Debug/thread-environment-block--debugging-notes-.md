---
description: Блок среды потока (заметки об отладке)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Блок среды потока (заметки об отладке)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550589"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="c8a7e-103">Блок среды потока (заметки об отладке)</span><span class="sxs-lookup"><span data-stu-id="c8a7e-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="c8a7e-104">Блок среды потока ([**Структура Теб**](/windows/win32/api/winternl/ns-winternl-teb)) содержит сведения о контексте для потока.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="c8a7e-105">В следующих версиях Windows смещение 32-разрядного адреса ТЕБ в 64-бит ТЕБ равно 0.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="c8a7e-106">Это можно использовать для прямого доступа к 32-разрядному ТЕБ потока WOW64.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="c8a7e-107">Это может измениться в более поздних версиях Windows</span><span class="sxs-lookup"><span data-stu-id="c8a7e-107">This might change in later versions of Windows</span></span>



|  <span data-ttu-id="c8a7e-108">Платформа</span><span class="sxs-lookup"><span data-stu-id="c8a7e-108">Platform</span></span>     | <span data-ttu-id="c8a7e-109">Версия</span><span class="sxs-lookup"><span data-stu-id="c8a7e-109">Version</span></span>                |
|---------------|------------------------|
| <span data-ttu-id="c8a7e-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8a7e-110">Windows Vista</span></span> | <span data-ttu-id="c8a7e-111">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8a7e-111">Windows Server 2008</span></span>    |
| <span data-ttu-id="c8a7e-112">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8a7e-112">Windows 7</span></span>     | <span data-ttu-id="c8a7e-113">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8a7e-113">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="c8a7e-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c8a7e-114">Windows 8</span></span>     | <span data-ttu-id="c8a7e-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8a7e-115">Windows Server 2012</span></span>    |
| <span data-ttu-id="c8a7e-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c8a7e-116">Windows 8.1</span></span>   | <span data-ttu-id="c8a7e-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c8a7e-117">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c8a7e-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c8a7e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8a7e-119">Структуры отладки</span><span class="sxs-lookup"><span data-stu-id="c8a7e-119">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="c8a7e-120">**\_Контекст WOW64**</span><span class="sxs-lookup"><span data-stu-id="c8a7e-120">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
