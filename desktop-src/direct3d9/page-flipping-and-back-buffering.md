---
description: Перелистывание страниц — это ключ в мультимедиа, анимации и игровом программном обеспечении; Он аналогичен способу анимации с помощью бумаги.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Перелистывание страниц и обратная буферизация (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710595"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a><span data-ttu-id="6b4c5-103">Перелистывание страниц и обратная буферизация (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6b4c5-103">Page Flipping and Back Buffering (Direct3D 9)</span></span>

<span data-ttu-id="6b4c5-104">Перелистывание страниц — это ключ в мультимедиа, анимации и игровом программном обеспечении; Он аналогичен способу анимации с помощью бумаги.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-104">Page flipping is key in multimedia, animation, and game software; it is analogous to the way you can do animation with a pad of paper.</span></span> <span data-ttu-id="6b4c5-105">На каждой странице исполнитель немного изменяет рисунок, так что при быстром переворачивании между листами рисунок становится анимированным.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-105">On each page, the artist changes the figure slightly, so that when you flip rapidly between sheets, the drawing appears animated.</span></span>

<span data-ttu-id="6b4c5-106">Перелистывание страниц в программном обеспечении аналогично этому процессу.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-106">Page flipping in software is similar to this process.</span></span> <span data-ttu-id="6b4c5-107">Direct3D реализует функции зеркального отображения страниц через цепочку буферов, которая является свойством устройства.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-107">Direct3D implements page flipping functionality through a swap chain, which is a property of the device.</span></span> <span data-ttu-id="6b4c5-108">Сначала вы настроили ряд буферов Direct3D, которые будут отражаться на экране, так, как документ-исполнитель переворачивается на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-108">Initially, you set up a series of Direct3D buffers that flip to the screen in the way that the artist's paper flips to the next page.</span></span> <span data-ttu-id="6b4c5-109">Первый буфер называется передним буфером цвета.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-109">The first buffer is referred to as the color front buffer.</span></span> <span data-ttu-id="6b4c5-110">Буферы под ним называются обратными буферами.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-110">The buffers behind it are called back buffers.</span></span> <span data-ttu-id="6b4c5-111">Приложение записывает в задний буфер, а затем переворачивает передний буфер цвета, чтобы на экране появился задний буфер.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-111">Your application writes to a back buffer and then flips the color front buffer so that the back buffer appears on screen.</span></span> <span data-ttu-id="6b4c5-112">Пока система отображает образ, программное обеспечение снова записывается в задний буфер.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-112">While the system displays the image, your software is again writing to a back buffer.</span></span> <span data-ttu-id="6b4c5-113">Процесс выполняется до тех пор, пока вы выполняете анимацию, что позволяет эффективно анимировать изображения.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-113">The process continues as long as you are animating, enabling you to animate images efficiently.</span></span>

<span data-ttu-id="6b4c5-114">Direct3D упрощает настройку схем переворачивания страниц — из простой схемы с двойной буферизацией (цветный фоновый буфер с одним задним буфером) к более сложным схемам с дополнительными задними буферами.</span><span class="sxs-lookup"><span data-stu-id="6b4c5-114">Direct3D makes it easy to set up page flipping schemes - from a simple double-buffered scheme (a color front buffer with one back buffer) to more sophisticated schemes with additional back buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b4c5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="6b4c5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b4c5-116">Поверхности Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b4c5-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="6b4c5-117">Что такое цепочка подкачки? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6b4c5-117">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



