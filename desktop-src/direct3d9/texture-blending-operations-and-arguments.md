---
description: Приложения связывают этап смешивания с каждой текстурой в наборе текущих текстур. Direct3D оценивает каждый этап смешения по порядку, начиная с первой текстуры в наборе и заканчивая восьмым.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Операции и аргументы смешения текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710647"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a><span data-ttu-id="e9cbf-104">Операции и аргументы смешения текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e9cbf-104">Texture Blending Operations and Arguments (Direct3D 9)</span></span>

<span data-ttu-id="e9cbf-105">Приложения связывают этап смешивания с каждой текстурой в наборе текущих текстур.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-105">Applications associate a blending stage with each texture in the set of current textures.</span></span> <span data-ttu-id="e9cbf-106">Direct3D оценивает каждый этап смешения по порядку, начиная с первой текстуры в наборе и заканчивая восьмым.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-106">Direct3D evaluates each blending stage in order, beginning with the first texture in the set and ending with the eighth.</span></span>

<span data-ttu-id="e9cbf-107">Direct3D применяет сведения из каждой текстуры в наборе текущих текстур к этапу смешения, который связан с ним.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-107">Direct3D applies the information from each texture in the set of current textures to the blending stage that is associated with it.</span></span> <span data-ttu-id="e9cbf-108">Приложения определяют, какие сведения из этапа текстуры используются путем вызова [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="e9cbf-108">Applications control what information from a texture stage is used by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api).</span></span> <span data-ttu-id="e9cbf-109">Можно задать отдельные операции для цвета и альфа-каналов, и каждая операция использует два аргумента.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-109">You can set separate operations for the color and alpha channels, and each operation uses two arguments.</span></span> <span data-ttu-id="e9cbf-110">Укажите операции с цветовым каналом, используя \_ состояние этапа D3DTSS колороп. Укажите операции Alpha с помощью D3DTSS \_ алфаоп.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-110">Specify color channel operations by using the D3DTSS\_COLOROP stage state; specify alpha operations by using D3DTSS\_ALPHAOP.</span></span> <span data-ttu-id="e9cbf-111">Оба состояния этапа используют значения из перечислимого типа [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="e9cbf-111">Both stage states use values from the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span>

<span data-ttu-id="e9cbf-112">Аргументы смешения текстур используют члены D3DTSS \_ COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 и D3DTSS \_ ALPHARG2 перечислимого типа [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="e9cbf-112">Texture blending arguments use the D3DTSS\_COLORARG1, D3DTSS\_COLORARG2, D3DTSS\_ALPHARG1, and D3DTSS\_ALPHARG2 members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="e9cbf-113">Соответствующие значения аргумента идентифицируются с помощью [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="e9cbf-113">The corresponding argument values are identified using [D3DTA](d3dta.md).</span></span>

> [!Note]  
> <span data-ttu-id="e9cbf-114">Можно отключить стадию текстуры и все последующие этапы смешения текстур в каскадном расположении, установив для этого этапа операцию D3DTOP \_ disable.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-114">You can disable a texture stage - and any subsequent texture blending stages in the cascade - by setting the color operation for that stage to D3DTOP\_DISABLE.</span></span> <span data-ttu-id="e9cbf-115">Отключение операции цветности также позволяет эффективно отключить операцию альфа.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-115">Disabling the color operation effectively disables the alpha operation as well.</span></span> <span data-ttu-id="e9cbf-116">Операции Alpha не могут быть отключены, если включены цветовые операции.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-116">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="e9cbf-117">Установка для операции Alpha значения D3DTOP \_ Disable, если включено смешение цветов, приводит к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-117">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

 

<span data-ttu-id="e9cbf-118">Чтобы определить поддерживаемые операции смешения текстур устройства, запросите элемент Текстурекапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="e9cbf-118">To determine the supported texture blending operations of a device, query the TextureCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9cbf-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e9cbf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9cbf-120">Смешение текстур</span><span class="sxs-lookup"><span data-stu-id="e9cbf-120">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
