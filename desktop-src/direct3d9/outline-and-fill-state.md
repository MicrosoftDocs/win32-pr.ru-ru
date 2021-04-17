---
description: Примитивы, не имеющие текстур, визуализируются с цветом, указанным в материалах, или с цветами, заданными для вершин, если таковые имеются.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Состояние структуры и заливки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710579"
---
# <a name="outline-and-fill-state-direct3d-9"></a><span data-ttu-id="f31ae-103">Состояние структуры и заливки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f31ae-103">Outline and Fill State (Direct3D 9)</span></span>

<span data-ttu-id="f31ae-104">Примитивы, не имеющие текстур, визуализируются с цветом, указанным в материалах, или с цветами, заданными для вершин, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="f31ae-104">Primitives that have no textures are rendered with the color specified by their material, or with the colors specified for the vertices, if any.</span></span> <span data-ttu-id="f31ae-105">Можно выбрать метод для заполнения этих данных, указав значение, определенное перечисляемым типом [**D3DFILLMODE**](./d3dfillmode.md) для \_ состояния отрисовки D3DRS филлмоде.</span><span class="sxs-lookup"><span data-stu-id="f31ae-105">You can select the method to fill them by specifying a value defined by the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type for the D3DRS\_FILLMODE render state.</span></span>

<span data-ttu-id="f31ae-106">Чтобы включить дизеринг, приложение должно передать \_ перечисленное значение D3DRS дисеренабле в качестве первого параметра в [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="f31ae-106">To enable dithering, your application must pass the D3DRS\_DITHERENABLE enumerated value as the first parameter to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span> <span data-ttu-id="f31ae-107">Необходимо установить для второго параметра **значение true** , чтобы включить дизеринг, и **false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="f31ae-107">It must set the second parameter to **TRUE** to enable dithering, and **FALSE** to disable it.</span></span>

<span data-ttu-id="f31ae-108">Иногда Рисование последнего пикселя в строке может привести к невозможности перекрытия окружающих примитивов.</span><span class="sxs-lookup"><span data-stu-id="f31ae-108">At times, drawing the last pixel in a line can cause unsightly overlap with surrounding primitives.</span></span> <span data-ttu-id="f31ae-109">Это можно контролировать с помощью \_ перечислимого значения D3DRS ластпиксел.</span><span class="sxs-lookup"><span data-stu-id="f31ae-109">You can control this using the D3DRS\_LASTPIXEL enumerated value.</span></span> <span data-ttu-id="f31ae-110">Однако не изменяйте этот параметр без некоторых обдумывания.</span><span class="sxs-lookup"><span data-stu-id="f31ae-110">However, do not alter this setting without some forethought.</span></span> <span data-ttu-id="f31ae-111">В некоторых случаях подавление отрисовки последнего пикселя может привести к некачественному зазору между примитивами.</span><span class="sxs-lookup"><span data-stu-id="f31ae-111">Under some conditions, suppressing the rendering of the last pixel can cause unsightly gaps between primitives.</span></span>

<span data-ttu-id="f31ae-112">Контуры объектов можно нарисовать, установив соответствующий шаблон рисования линии.</span><span class="sxs-lookup"><span data-stu-id="f31ae-112">Object outlines can be drawn by setting the appropriate line drawing pattern.</span></span> <span data-ttu-id="f31ae-113">Состояние рисования линии по умолчанию — Рисование сплошных линий.</span><span class="sxs-lookup"><span data-stu-id="f31ae-113">The default line drawing state is to draw solid lines.</span></span> <span data-ttu-id="f31ae-114">Дополнительные сведения см. [в разделе Поддержка рисования линий в D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) Render State.</span><span class="sxs-lookup"><span data-stu-id="f31ae-114">For more information, see [Line Drawing Support in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) render state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f31ae-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f31ae-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f31ae-116">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="f31ae-116">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
