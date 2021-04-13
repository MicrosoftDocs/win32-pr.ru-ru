---
title: таббедтаункновнелемент
description: таббедтаункновнелемент
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410797"
---
# <a name="tabbedtounknownelement"></a><span data-ttu-id="8f853-103">таббедтаункновнелемент</span><span class="sxs-lookup"><span data-stu-id="8f853-103">TabbedToUnknownElement</span></span>

## <a name="text"></a><span data-ttu-id="8f853-104">Текст</span><span class="sxs-lookup"><span data-stu-id="8f853-104">Text</span></span>

<span data-ttu-id="8f853-105">Переход к элементу за пределами целевого HWND.</span><span class="sxs-lookup"><span data-stu-id="8f853-105">Tabbing has gone to an element outside the target hwnd.</span></span>

## <a name="type"></a><span data-ttu-id="8f853-106">Тип</span><span class="sxs-lookup"><span data-stu-id="8f853-106">Type</span></span>

<span data-ttu-id="8f853-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="8f853-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="8f853-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8f853-108">Description</span></span>

<span data-ttu-id="8f853-109">Использование стандартной навигации с помощью клавиатуры (TAB или SHIFT + TAB) приводит к сдвигу фокуса за пределами HWND целевого объекта проверки.</span><span class="sxs-lookup"><span data-stu-id="8f853-109">Using standard keyboard navigation (Tab or Shift+Tab) causes focus to shift outside the HWND of the verification target.</span></span>

<span data-ttu-id="8f853-110">Аккчеккер перемещает дерево элементов в HWND верхнего уровня для выбранного целевого объекта проверки перед выполнением каких-либо задач проверки.</span><span class="sxs-lookup"><span data-stu-id="8f853-110">AccChecker moves up the element tree to the top-level HWND for the chosen verification target before running any verification tasks.</span></span> <span data-ttu-id="8f853-111">Это сокращает количество ложных ошибок, создаваемых, если HWND, выбранный для проверки, является частью более сложной клиентской области.</span><span class="sxs-lookup"><span data-stu-id="8f853-111">This reduces the number of spurious errors generated if an HWND chosen for verification is part of a more complex client area.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="8f853-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="8f853-112">Possible causes</span></span>

-   <span data-ttu-id="8f853-113">Целью проверки не требуется реализация с вкладками для обеспечения полной функциональности.</span><span class="sxs-lookup"><span data-stu-id="8f853-113">The verification target doesn't require a tabbing implementation to provide full functionality.</span></span>
-   <span data-ttu-id="8f853-114">Взаимодействие с пользователем во время проверки, например перемещение фокуса на нецелевой HWND, мешает процессу проверки.</span><span class="sxs-lookup"><span data-stu-id="8f853-114">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>

 

 




