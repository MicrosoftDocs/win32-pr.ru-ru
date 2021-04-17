---
title: Отзывы
description: В режиме обратной связи каждый объект-примитив, который должен быть растровым, создает блок значений, которые копируются в массив обратной связи.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- режим обратной связи, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674558"
---
# <a name="feedback-mode"></a><span data-ttu-id="e780f-104">Режим обратной связи</span><span class="sxs-lookup"><span data-stu-id="e780f-104">Feedback mode</span></span>

<span data-ttu-id="e780f-105">В режиме обратной связи каждый объект-примитив, который должен быть растровым, создает блок значений, которые копируются в массив обратной связи.</span><span class="sxs-lookup"><span data-stu-id="e780f-105">In feedback mode, each primitive to be rasterized generates a block of values that is copied into the feedback array.</span></span> <span data-ttu-id="e780f-106">Укажите этот массив с помощью [**глфидбаккбуффер**](glfeedbackbuffer.md), который необходимо вызвать перед переводом OpenGL в режим обратной связи.</span><span class="sxs-lookup"><span data-stu-id="e780f-106">Supply this array with [**glFeedbackBuffer**](glfeedbackbuffer.md), which you must call before putting OpenGL into feedback mode.</span></span> <span data-ttu-id="e780f-107">Каждый блок значений начинается с кода, указывающего на тип-примитив, за которым следуют значения, описывающие вершины примитива и связанные данные.</span><span class="sxs-lookup"><span data-stu-id="e780f-107">Each block of values begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="e780f-108">Записи также записываются для точечных рисунков и пиксельных прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="e780f-108">Entries are also written for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="e780f-109">Не гарантируется, что значения будут записываться в массив обратной связи до тех пор, пока не будет вызван [**глрендермоде**](glrendermode.md) для получения из режима обратной связи OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e780f-109">Values are not guaranteed to be written into the feedback array until you call [**glRenderMode**](glrendermode.md) to take OpenGL out of feedback mode.</span></span> <span data-ttu-id="e780f-110">[**Глпасссраугх**](glpassthrough.md) можно использовать для предоставления маркера, возвращаемого в режиме обратной связи, как если бы он был примитивом.</span><span class="sxs-lookup"><span data-stu-id="e780f-110">You can use [**glPassThrough**](glpassthrough.md) to supply a marker that is returned in feedback mode as if it were a primitive.</span></span>

 

 




