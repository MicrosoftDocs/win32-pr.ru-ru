---
description: Direct3D использует форму фильтрации линейной текстуры с именем билинейной Filtering.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Линейная фильтрация текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537598"
---
# <a name="linear-texture-filtering-direct3d-9"></a><span data-ttu-id="9b410-103">Линейная фильтрация текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9b410-103">Linear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="9b410-104">Direct3D использует форму фильтрации линейной текстуры с именем билинейной Filtering.</span><span class="sxs-lookup"><span data-stu-id="9b410-104">Direct3D uses a form of linear texture filtering called bilinear filtering.</span></span> <span data-ttu-id="9b410-105">Как и при использовании [выборки с ближайшими точками (Direct3D 9)](nearest-point-sampling.md), билинейнойная фильтрация в первую очередь рассчитывает адрес шаг текселя, который обычно не является целым числом.</span><span class="sxs-lookup"><span data-stu-id="9b410-105">Like [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md), bilinear texture filtering first computes a texel address, which is usually not an integer address.</span></span> <span data-ttu-id="9b410-106">Затем билинейной Filter находит шаг текселя, чей целочисленный адрес ближе всего к вычисленному.</span><span class="sxs-lookup"><span data-stu-id="9b410-106">Bilinear filtering then finds the texel whose integer address is closest to the computed address.</span></span> <span data-ttu-id="9b410-107">Кроме того, модуль визуализации Direct3D вычисляет взвешенное среднее значение пикселей текстуры, расположенное непосредственно над, снизу, слева от и справа от ближайшего пункта выборки.</span><span class="sxs-lookup"><span data-stu-id="9b410-107">In addition, the Direct3D rendering module computes a weighted average of the texels that are immediately above, below, to the left of, and to the right of the nearest sample point.</span></span>

<span data-ttu-id="9b410-108">Выберите фильтр текстур билинейной, вызвав метод [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) .</span><span class="sxs-lookup"><span data-stu-id="9b410-108">Select bilinear texture filtering by invoking the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="9b410-109">Задайте для первого параметра значение целочисленного индекса (0-7) текстуры, для которой выбирается метод фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="9b410-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="9b410-110">Передайте D3DSAMP \_ магфилтер, D3DSAMP \_ МИНФИЛТЕР или D3DSAMP \_ мипфилтер во второй параметр, чтобы задать фильтр увеличения, минификации или функции текстурирования.</span><span class="sxs-lookup"><span data-stu-id="9b410-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="9b410-111">Передайте \_ линейное D3DTEXF в третьем параметре.</span><span class="sxs-lookup"><span data-stu-id="9b410-111">Pass D3DTEXF\_LINEAR in the third parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b410-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9b410-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b410-113">Фильтрация текстур</span><span class="sxs-lookup"><span data-stu-id="9b410-113">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
