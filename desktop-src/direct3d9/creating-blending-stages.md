---
description: Этап наложения — это набор операций с текстурами и их аргументов, определяющих наложение текстур.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Создание стадий смешения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141599"
---
# <a name="creating-blending-stages-direct3d-9"></a><span data-ttu-id="cbd77-103">Создание стадий смешения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cbd77-103">Creating Blending Stages (Direct3D 9)</span></span>

<span data-ttu-id="cbd77-104">Этап наложения — это набор операций с текстурами и их аргументов, определяющих наложение текстур.</span><span class="sxs-lookup"><span data-stu-id="cbd77-104">A blending stage is a set of texture operations and their arguments that define how textures are blended.</span></span> <span data-ttu-id="cbd77-105">При выполнении этапа смешения приложения C++ вызывают метод [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="cbd77-105">When making a blending stage, C++ applications invoke the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="cbd77-106">Первый вызов задает выполняемую операцию.</span><span class="sxs-lookup"><span data-stu-id="cbd77-106">The first call specifies the operation that is performed.</span></span> <span data-ttu-id="cbd77-107">Два дополнительных вызова определяют аргументы, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="cbd77-107">Two additional invocations define the arguments to which the operation is applied.</span></span> <span data-ttu-id="cbd77-108">В следующем примере кода показано создание этапа смешения.</span><span class="sxs-lookup"><span data-stu-id="cbd77-108">The following code example illustrates the creation of a blending stage.</span></span>


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



<span data-ttu-id="cbd77-109">Данные шаг текселя в текстурах содержат значения цвета и альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cbd77-109">Texel data in textures contain color and alpha values.</span></span> <span data-ttu-id="cbd77-110">Приложения могут определять отдельные операции для цветов и альфа-значений на одном этапе смешения.</span><span class="sxs-lookup"><span data-stu-id="cbd77-110">Applications can define separate operations for both color and alpha values in a single blending stage.</span></span> <span data-ttu-id="cbd77-111">У каждой операции, цвета и альфа-канала есть собственные аргументы.</span><span class="sxs-lookup"><span data-stu-id="cbd77-111">Each operation, color, and alpha, has its own arguments.</span></span> <span data-ttu-id="cbd77-112">Дополнительные сведения см. в разделе [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="cbd77-112">For details, see [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

<span data-ttu-id="cbd77-113">Несмотря на то, что не входит в API Direct3D, в приложение можно вставить следующие макросы, чтобы сократить код, необходимый для создания стадий смешения текстур.</span><span class="sxs-lookup"><span data-stu-id="cbd77-113">Although not part of the Direct3D API, you can insert the following macros into your application to abbreviate the code required for creating texture blending stages.</span></span>


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a><span data-ttu-id="cbd77-114">См. также</span><span class="sxs-lookup"><span data-stu-id="cbd77-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd77-115">Смешение текстур</span><span class="sxs-lookup"><span data-stu-id="cbd77-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
