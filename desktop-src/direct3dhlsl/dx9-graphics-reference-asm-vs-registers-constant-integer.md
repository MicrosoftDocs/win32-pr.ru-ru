---
title: Постоянный целочисленный регистр (Справочник по HLSL VS)
description: Постоянные целочисленные регистры используются только циклом-VS и представителя-vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984048"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a><span data-ttu-id="b6303-103">Постоянный целочисленный регистр (Справочник по HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="b6303-103">Constant Integer Register (HLSL VS reference)</span></span>

<span data-ttu-id="b6303-104">Постоянные целочисленные регистры используются только [циклом-VS](loop---vs.md) и [представителя-VS](rep---vs.md).</span><span class="sxs-lookup"><span data-stu-id="b6303-104">Constant integer registers are used only by [loop - vs](loop---vs.md) and [rep - vs](rep---vs.md).</span></span>

<span data-ttu-id="b6303-105">Их можно задать с помощью [дефи-VS](defi---vs.md) или [**сетвертексшадерконстанти**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="b6303-105">They can be set using [defi - vs](defi---vs.md) or [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span></span>

<span data-ttu-id="b6303-106">При использовании в качестве аргумента для инструкции [Loop-VS](loop---vs.md) :</span><span class="sxs-lookup"><span data-stu-id="b6303-106">When used as an argument to the [loop - vs](loop---vs.md) instruction:</span></span>

-   <span data-ttu-id="b6303-107">. x — это число итераций.</span><span class="sxs-lookup"><span data-stu-id="b6303-107">.x is the iteration count.</span></span> <span data-ttu-id="b6303-108">([представитель-VS](rep---vs.md) использует только этот компонент).</span><span class="sxs-lookup"><span data-stu-id="b6303-108">([rep - vs](rep---vs.md) uses only this component).</span></span>
-   <span data-ttu-id="b6303-109">. y — это начальное значение счетчика цикла.</span><span class="sxs-lookup"><span data-stu-id="b6303-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="b6303-110">. z — шаг приращения счетчика циклов.</span><span class="sxs-lookup"><span data-stu-id="b6303-110">.z is the increment step for the loop counter.</span></span>

<span data-ttu-id="b6303-111">Поведение констант шейдера изменилось между Direct3D 8 и Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b6303-111">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="b6303-112">Для Direct3D 9 константы, заданные с помощью дефкс, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="b6303-112">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="b6303-113">Время существования константы, объявленной с помощью дефкс, ограничено выполнением только этого шейдера.</span><span class="sxs-lookup"><span data-stu-id="b6303-113">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="b6303-114">И наоборот, константы, заданные с помощью API-интерфейсов, Сетксксксшадерконстанткс инициализировать константы в глобальном пространстве.</span><span class="sxs-lookup"><span data-stu-id="b6303-114">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="b6303-115">Константы в глобальном пространстве не копируются в локальное пространство (видимую шейдеру) до тех пор, пока не будет вызван Сетксксксшадерконстантс.</span><span class="sxs-lookup"><span data-stu-id="b6303-115">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="b6303-116">Для Direct3D 8 константы, заданные с помощью дефкс или API, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="b6303-116">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="b6303-117">При каждом выполнении шейдера все константы используются текущим шейдером независимо от метода, используемого для их установки.</span><span class="sxs-lookup"><span data-stu-id="b6303-117">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6303-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b6303-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6303-119">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="b6303-119">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 