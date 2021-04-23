---
title: Элементы управления без окон
description: Элементы управления без окон
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411418"
---
# <a name="windowless-controls"></a><span data-ttu-id="a276b-103">Элементы управления без окон</span><span class="sxs-lookup"><span data-stu-id="a276b-103">Windowless Controls</span></span>

<span data-ttu-id="a276b-104">Спецификация элементов управления ActiveX 96 включает определение элементов управления без окон.</span><span class="sxs-lookup"><span data-stu-id="a276b-104">The ActiveX Controls 96 specification includes a definition for windowless controls.</span></span> <span data-ttu-id="a276b-105">Такие элементы управления не работают в собственном окне и нуждаются в контейнере, предлагающем общее окно, в котором может нарисоваться элемент управления, см. пакет SDK для ActiveX.</span><span class="sxs-lookup"><span data-stu-id="a276b-105">Such controls do not operate in their own window and require a container to offer a shared window into which the control may draw, see the ActiveX SDK.</span></span> <span data-ttu-id="a276b-106">Элементы управления без окон предназначены для совместимости с старыми контейнерами элементов управления, создавая собственное окно в этой ситуации, контейнеры элементов управления без окон должны размещать Оконные элементы управления традиционным образом без проблем.</span><span class="sxs-lookup"><span data-stu-id="a276b-106">Windowless controls are designed to be compatible with older control containers by creating their own window in that situation, windowless control containers should host windowed controls in the traditional way with no problem.</span></span> <span data-ttu-id="a276b-107">Однако может быть полезно, чтобы контейнер мог отличать те элементы управления, которые могут работать в режиме без окон, поэтому определена соответствующая категория компонента.</span><span class="sxs-lookup"><span data-stu-id="a276b-107">It may however be useful for a container to distinguish those controls that can operate in a windowless mode, so an appropriate component category is defined.</span></span>

<span data-ttu-id="a276b-108">CATID-{1D06B600-3AE3-11cf-87B9-00AA006C8166} \_ ВИНДОВЛЕССОБЖЕКТ CATID</span><span class="sxs-lookup"><span data-stu-id="a276b-108">CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID\_WindowlessObject</span></span>

## <a name="related-topics"></a><span data-ttu-id="a276b-109">См. также</span><span class="sxs-lookup"><span data-stu-id="a276b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a276b-110">Категории компонентов</span><span class="sxs-lookup"><span data-stu-id="a276b-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




