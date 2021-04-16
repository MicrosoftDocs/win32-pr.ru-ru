---
description: Методы курсора мыши позволяют приложению указывать цветовой курсор, предоставляя поверхность, которая содержит изображение.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Работа с курсорами мыши (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495564"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a><span data-ttu-id="6fa76-103">Работа с курсорами мыши (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6fa76-103">Working with Mouse Cursors (Direct3D 9)</span></span>

<span data-ttu-id="6fa76-104">Методы курсора мыши позволяют приложению указывать цветовой курсор, предоставляя поверхность, которая содержит изображение.</span><span class="sxs-lookup"><span data-stu-id="6fa76-104">The mouse cursor methods enable the application to specify a color cursor by providing a surface that contains an image.</span></span> <span data-ttu-id="6fa76-105">Система гарантирует, что этот курсор будет обновляться с половиной скорости дисплея или более, если частота кадров приложения замедлена.</span><span class="sxs-lookup"><span data-stu-id="6fa76-105">The system will ensure that this cursor will be updated at half the display rate or more if the application's frame rate is slow.</span></span> <span data-ttu-id="6fa76-106">Однако курсор никогда не будет обновляться чаще, чем частота обновления дисплея.</span><span class="sxs-lookup"><span data-stu-id="6fa76-106">However, the cursor will never be updated more frequently than the display refresh rate.</span></span>

<span data-ttu-id="6fa76-107">Расположение курсора мыши привязано к системному курсору, соответствующим образом масштабируется для режима пространственного разрешения экрана, но его можно напрямую переместить в приложении.</span><span class="sxs-lookup"><span data-stu-id="6fa76-107">The mouse cursor position is tied to the system cursor, appropriately scaled for the current display mode spatial resolution, but it can be moved explicitly by the application.</span></span> <span data-ttu-id="6fa76-108">Это аналогично поведению системного курсора мыши, поддерживаемого API Win32.</span><span class="sxs-lookup"><span data-stu-id="6fa76-108">This is analogous to the behavior of the Win32 API - supported system mouse cursor.</span></span> <span data-ttu-id="6fa76-109">Дополнительные сведения об использовании курсора мыши в приложении Direct3D см. в следующих справочных разделах.</span><span class="sxs-lookup"><span data-stu-id="6fa76-109">For more information about how to use a mouse cursor in your Direct3D application, see the following reference topics.</span></span>

-   [<span data-ttu-id="6fa76-110">**IDirect3DDevice9::ShowCursor**</span><span class="sxs-lookup"><span data-stu-id="6fa76-110">**IDirect3DDevice9::ShowCursor**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [<span data-ttu-id="6fa76-111">**IDirect3DDevice9::SetCursorPosition**</span><span class="sxs-lookup"><span data-stu-id="6fa76-111">**IDirect3DDevice9::SetCursorPosition**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [<span data-ttu-id="6fa76-112">**IDirect3DDevice9::SetCursorProperties**</span><span class="sxs-lookup"><span data-stu-id="6fa76-112">**IDirect3DDevice9::SetCursorProperties**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

<span data-ttu-id="6fa76-113">Direct3D гарантирует, что мышь поддерживается либо с помощью аппаратных реализаций, либо с помощью времени выполнения Direct3D, выполняющего блиттинг операции аппаратного ускорения при вызове [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)повторно.</span><span class="sxs-lookup"><span data-stu-id="6fa76-113">Direct3D ensures that the mouse is supported either by hardware implementations or by the Direct3D run time that performs hardware-accelerated blitting operations when calling [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fa76-114">См. также</span><span class="sxs-lookup"><span data-stu-id="6fa76-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fa76-115">Советы по программированию</span><span class="sxs-lookup"><span data-stu-id="6fa76-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
