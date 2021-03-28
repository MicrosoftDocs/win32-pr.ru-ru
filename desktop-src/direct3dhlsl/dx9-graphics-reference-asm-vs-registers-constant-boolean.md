---
title: Константный логический регистр (HLSL VS)
description: Этот регистр представляет собой коллекцию битов, используемых в статических инструкциях по управлению потоком (например, если bool-VS-else-VS-endif-VS).
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984036"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a><span data-ttu-id="d9203-103">Константный логический регистр (HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="d9203-103">Constant Boolean register (HLSL VS reference)</span></span>

<span data-ttu-id="d9203-104">Этот регистр представляет собой коллекцию битов, используемых в инструкциях статического управления потоком (например, [Если bool-VS](if-bool---vs.md)  -  [else-VS](else---vs.md)  -  [endif-VS](endif---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="d9203-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - vs](if-bool---vs.md) - [else - vs](else---vs.md) - [endif - vs](endif---vs.md)).</span></span> <span data-ttu-id="d9203-105">Это 16 из них, поэтому шейдер может иметь 16 независимых условий ветвления.</span><span class="sxs-lookup"><span data-stu-id="d9203-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="d9203-106">Их можно задать с помощью [дефб-VS](defb---vs.md) или [**сетвертексшадерконстантб**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="d9203-106">They can be set using [defb - vs](defb---vs.md) or [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span></span>

<span data-ttu-id="d9203-107">Поведение констант шейдера изменилось между Direct3D 8 и Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d9203-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="d9203-108">Для Direct3D 9 константы, заданные с помощью дефкс, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="d9203-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="d9203-109">Время существования константы, объявленной с помощью дефкс, ограничено выполнением только этого шейдера.</span><span class="sxs-lookup"><span data-stu-id="d9203-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="d9203-110">И наоборот, константы, заданные с помощью API-интерфейсов, Сетксксксшадерконстанткс инициализировать константы в глобальном пространстве.</span><span class="sxs-lookup"><span data-stu-id="d9203-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="d9203-111">Константы в глобальном пространстве не копируются в локальное пространство (видимую шейдеру) до тех пор, пока не будет вызван Сетксксксшадерконстантс.</span><span class="sxs-lookup"><span data-stu-id="d9203-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="d9203-112">Для Direct3D 8 константы, заданные с помощью дефкс или API, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="d9203-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="d9203-113">При каждом выполнении шейдера все константы используются текущим шейдером независимо от метода, используемого для их установки.</span><span class="sxs-lookup"><span data-stu-id="d9203-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9203-114">См. также</span><span class="sxs-lookup"><span data-stu-id="d9203-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9203-115">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="d9203-115">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 