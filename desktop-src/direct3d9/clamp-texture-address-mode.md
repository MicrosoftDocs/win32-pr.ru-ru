---
description: Режим адресации текстуры зажима, определяемый \_ ЭЛЕМЕНТОМ D3DTADDRESS в перечисленном ТИПЕ D3DTEXTUREADDRESS, заставляет Direct3D заменять координаты текстуры на \[ диапазон 0,0, 1,0 \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Режим адреса текстуры среза (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710784"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a><span data-ttu-id="8335c-103">Режим адреса текстуры среза (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8335c-103">Clamp Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="8335c-104">Режим адресации текстуры зажима, определяемый \_ ЭЛЕМЕНТОМ D3DTADDRESS в перечисленном типе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , заставляет Direct3D заменять координаты текстуры на \[ диапазон 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="8335c-104">The clamp texture address mode, identified by the D3DTADDRESS\_CLAMP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to clamp your texture coordinates to the \[0.0, 1.0\] range.</span></span> <span data-ttu-id="8335c-105">То есть, она применяет текстуру один раз, а затем смеарс цвет краевых пикселов.</span><span class="sxs-lookup"><span data-stu-id="8335c-105">That is, it applies the texture once, then smears the color of edge pixels.</span></span> <span data-ttu-id="8335c-106">Например, предположим, что приложение создает квадратный примитив и присваивает координаты текстуры (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) и (3.0, 0,0) вершинам примитива.</span><span class="sxs-lookup"><span data-stu-id="8335c-106">For example, suppose that your application creates a square primitive and assigns texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0) to the primitive's vertices.</span></span> <span data-ttu-id="8335c-107">Если задать для режима адресации текстуры D3DTADDRESSный \_ срез, то текстура будет применена один раз.</span><span class="sxs-lookup"><span data-stu-id="8335c-107">Setting the texture addressing mode to D3DTADDRESS\_CLAMP results in the texture being applied once.</span></span> <span data-ttu-id="8335c-108">Цвета пикселей вверху столбцов и в конце строк применяются к верхней и правой части примитива соответственно.</span><span class="sxs-lookup"><span data-stu-id="8335c-108">The pixel colors at the top of the columns and the end of the rows are extended to the top and right of the primitive respectively.</span></span>

<span data-ttu-id="8335c-109">На следующем рисунке показана прикрепленная текстура.</span><span class="sxs-lookup"><span data-stu-id="8335c-109">The following illustration shows a clamped texture.</span></span>

![изображение текстуры и прикрепленной текстуры](images/clamp.png)

## <a name="related-topics"></a><span data-ttu-id="8335c-111">См. также</span><span class="sxs-lookup"><span data-stu-id="8335c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8335c-112">Режимы адресации текстур</span><span class="sxs-lookup"><span data-stu-id="8335c-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
