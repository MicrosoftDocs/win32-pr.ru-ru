---
description: Функция является стандартным блоком для шейдера, созданного на высоком уровне языка. Если вы предпочитаете писать шейдеры на языке C, а не на языке ассемблера, вам потребуется написать функции.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Синтаксис функции Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536833"
---
# <a name="effect-function-syntax-direct3d-9"></a><span data-ttu-id="5aa9d-104">Синтаксис функции Effect (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5aa9d-104">Effect Function Syntax (Direct3D 9)</span></span>

<span data-ttu-id="5aa9d-105">Функция является стандартным блоком для шейдера, созданного на высоком уровне языка.</span><span class="sxs-lookup"><span data-stu-id="5aa9d-105">A function is the building block for a shader created in the high-level language.</span></span> <span data-ttu-id="5aa9d-106">Если вы предпочитаете писать шейдеры на языке C, а не на языке ассемблера, вам потребуется написать функции.</span><span class="sxs-lookup"><span data-stu-id="5aa9d-106">If you prefer to write shaders in a C-style language instead of in assembly language, you will want to write functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa9d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5aa9d-107">Syntax</span></span>


```
type id ( [ parameters ] )  
    { body }
```



<span data-ttu-id="5aa9d-108">Функции не изменяют значения параметров в результате.</span><span class="sxs-lookup"><span data-stu-id="5aa9d-108">Functions do not change parameter values in an effect.</span></span>

-   <span data-ttu-id="5aa9d-109">Type — любая допустимая [ссылка для типа HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa9d-109">type - Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span>
-   <span data-ttu-id="5aa9d-110">ID — уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="5aa9d-110">id - A unique name.</span></span>
-   <span data-ttu-id="5aa9d-111">Parameters — параметры функции.</span><span class="sxs-lookup"><span data-stu-id="5aa9d-111">parameters - Function parameters.</span></span>
-   <span data-ttu-id="5aa9d-112">Body — текст функции.</span><span class="sxs-lookup"><span data-stu-id="5aa9d-112">body - The body of the function.</span></span>

<span data-ttu-id="5aa9d-113">Функции основаны на высоком уровне языка.</span><span class="sxs-lookup"><span data-stu-id="5aa9d-113">Functions are built from the high-level language.</span></span> <span data-ttu-id="5aa9d-114">См. [Справочник по HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="5aa9d-114">See [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aa9d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="5aa9d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa9d-116">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="5aa9d-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
