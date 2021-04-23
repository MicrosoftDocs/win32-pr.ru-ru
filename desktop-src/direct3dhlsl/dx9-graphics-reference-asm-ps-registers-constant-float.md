---
title: Регистр постоянного float (Справочник по HLSL PS)
description: Входной регистр шейдера пикселей для константы с плавающей точкой 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413398"
---
# <a name="constant-float-register-hlsl-ps-reference"></a><span data-ttu-id="30139-103">Регистр постоянного float (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="30139-103">Constant float register (HLSL PS reference)</span></span>

<span data-ttu-id="30139-104">Входной регистр шейдера пикселей для константы с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="30139-104">Pixel shader input register for a 4D floating-point constant.</span></span>

<span data-ttu-id="30139-105">Их можно задать с помощью [DEF-PS](def---ps.md) или [**сетпикселшадерконстантф**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="30139-105">They can be set using [def - ps](def---ps.md) or [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="30139-106">Поведение констант шейдера изменилось между Direct3D 8 и Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="30139-106">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="30139-107">Для Direct3D 9 константы, заданные с помощью дефкс, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="30139-107">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="30139-108">Время существования константы, объявленной с помощью дефкс, ограничено выполнением только этого шейдера.</span><span class="sxs-lookup"><span data-stu-id="30139-108">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="30139-109">И наоборот, константы, заданные с помощью API-интерфейсов, Сетксксксшадерконстанткс инициализировать константы в глобальном пространстве.</span><span class="sxs-lookup"><span data-stu-id="30139-109">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="30139-110">Константы в глобальном пространстве не копируются в локальное пространство (видимую шейдеру) до тех пор, пока не будет вызван Сетксксксшадерконстантс.</span><span class="sxs-lookup"><span data-stu-id="30139-110">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="30139-111">Для Direct3D 8 константы, заданные с помощью дефкс или API, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="30139-111">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="30139-112">При каждом выполнении шейдера все константы используются текущим шейдером независимо от метода, используемого для их установки.</span><span class="sxs-lookup"><span data-stu-id="30139-112">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="examples"></a><span data-ttu-id="30139-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="30139-113">Examples</span></span>

<span data-ttu-id="30139-114">Ниже приведен пример объявления двух констант с плавающей запятой в шейдере.</span><span class="sxs-lookup"><span data-stu-id="30139-114">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="30139-115">Эти константы загружаются каждый раз при вызове [**сетпикселшадер**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) .</span><span class="sxs-lookup"><span data-stu-id="30139-115">These constants are loaded every time [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) is called.</span></span>

<span data-ttu-id="30139-116">Если вы устанавливаете постоянные значения с помощью API, то объявление шейдера не требуется.</span><span class="sxs-lookup"><span data-stu-id="30139-116">If you are setting constant values with the API, there is no shader declaration required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30139-117">См. также</span><span class="sxs-lookup"><span data-stu-id="30139-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30139-118">Регистры</span><span class="sxs-lookup"><span data-stu-id="30139-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 