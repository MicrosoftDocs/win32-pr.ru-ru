---
title: In-Context и функции-обработчики вне контекста
description: При регистрации функции-обработчика с помощью Сетвиневенсук клиенты указывают, находится ли функция обработчика в контексте или вне контекста. В этих терминах описывается расположение памяти функции-обработчика относительно адресного пространства сервера.
ms.assetid: 6876d74a-9c15-4f89-92ad-d072d9b528f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d96bff36f47b5e7fb0ad2e98d5a5347e2bc747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258787"
---
# <a name="in-context-and-out-of-context-hook-functions"></a><span data-ttu-id="f6b59-104">In-Context и функции-обработчики вне контекста</span><span class="sxs-lookup"><span data-stu-id="f6b59-104">In-Context and Out-of-Context Hook Functions</span></span>

<span data-ttu-id="f6b59-105">При регистрации функции-обработчика с помощью [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)клиенты указывают, находится ли функция обработчика *в контексте* или *вне контекста*.</span><span class="sxs-lookup"><span data-stu-id="f6b59-105">When registering a hook function with [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook), clients specify whether the hook function is *in-context* or *out-of-context*.</span></span> <span data-ttu-id="f6b59-106">В этих терминах описывается расположение памяти функции-обработчика относительно адресного пространства сервера.</span><span class="sxs-lookup"><span data-stu-id="f6b59-106">These terms describe the memory location of the hook function relative to the server's address space.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f6b59-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="f6b59-107">In this section</span></span>

-   [<span data-ttu-id="f6b59-108">Функции-обработчики в контексте</span><span class="sxs-lookup"><span data-stu-id="f6b59-108">In-Context Hook Functions</span></span>](in-context-hook-functions.md)
-   [<span data-ttu-id="f6b59-109">Меры предосторожности в контексте функции-ловушки</span><span class="sxs-lookup"><span data-stu-id="f6b59-109">In-Context Hook Function Precautions</span></span>](in-context-hook-function-precautions.md)
-   [<span data-ttu-id="f6b59-110">Функции-обработчики вне контекста</span><span class="sxs-lookup"><span data-stu-id="f6b59-110">Out-of-Context Hook Functions</span></span>](out-of-context-hook-functions.md)

 

 




