---
description: Ваше приложение может использовать буфер трафарета для создания двух- или трехмерных изображений в трехмерной сцене.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Компоновка (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692038"
---
# <a name="compositing-direct3d-9"></a><span data-ttu-id="726db-103">Компоновка (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="726db-103">Compositing (Direct3D 9)</span></span>

<span data-ttu-id="726db-104">Ваше приложение может использовать буфер трафарета для создания двух- или трехмерных изображений в трехмерной сцене.</span><span class="sxs-lookup"><span data-stu-id="726db-104">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="726db-105">Маска в буфере трафарета используется для ограждения области, которая является поверхностью однобуферной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="726db-105">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="726db-106">Сохраненную двухмерную информацию, такую как текст или точечные рисунки, затем можно записать в огороженную область.</span><span class="sxs-lookup"><span data-stu-id="726db-106">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="726db-107">Кроме того, ваше приложение может отрисовывать дополнительные трехмерные примитивы в замаскированный трафаретом регион поверхности однобуферной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="726db-107">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="726db-108">Приложение даже может отрисовывать всю сцену.</span><span class="sxs-lookup"><span data-stu-id="726db-108">It can even render an entire scene.</span></span>

<span data-ttu-id="726db-109">Игры часто предполагают компоновку нескольких трехмерных сцен.</span><span class="sxs-lookup"><span data-stu-id="726db-109">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="726db-110">Так, в симуляторах вождения, как правило, показано отражение в зеркале заднего вида.</span><span class="sxs-lookup"><span data-stu-id="726db-110">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="726db-111">В нем отражается происходящее за водителем в трехмерном формате.</span><span class="sxs-lookup"><span data-stu-id="726db-111">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="726db-112">Это вторая трехмерная сцена, скомпонованная с передним обзором водителя.</span><span class="sxs-lookup"><span data-stu-id="726db-112">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

## <a name="related-topics"></a><span data-ttu-id="726db-113">См. также</span><span class="sxs-lookup"><span data-stu-id="726db-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="726db-114">Методы буфера шаблона</span><span class="sxs-lookup"><span data-stu-id="726db-114">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



