---
title: Совместное использование списков вывода
description: При создании контекста отрисовки он имеет свой собственный список отображения.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL в Windows, совместное использование списков вывода
- Общий доступ списки дисплеев OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332059"
---
# <a name="sharing-display-lists"></a><span data-ttu-id="f794c-105">Совместное использование списков вывода</span><span class="sxs-lookup"><span data-stu-id="f794c-105">Sharing Display Lists</span></span>

<span data-ttu-id="f794c-106">При создании контекста отрисовки он имеет свой собственный список отображения.</span><span class="sxs-lookup"><span data-stu-id="f794c-106">When you create a rendering context, it has its own display-list space.</span></span> <span data-ttu-id="f794c-107">Функция [**вглшарелистс**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) позволяет контексту отрисовки совместно использовать пространство списка другого контекста визуализации.</span><span class="sxs-lookup"><span data-stu-id="f794c-107">The [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) function enables a rendering context to share the display-list space of another rendering context.</span></span> <span data-ttu-id="f794c-108">Любое количество контекстов отрисовки может совместно использовать одно пространство отображения.</span><span class="sxs-lookup"><span data-stu-id="f794c-108">Any number of rendering contexts can share a single display-list space.</span></span>

 

 




