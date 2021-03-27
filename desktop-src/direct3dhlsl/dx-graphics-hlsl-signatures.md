---
title: Сигнатуры
description: Сигнатура шейдера — это список параметров, которые либо являются входными, либо выводяти из функции шейдера.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996795"
---
# <a name="signatures"></a><span data-ttu-id="52c1c-103">Сигнатуры</span><span class="sxs-lookup"><span data-stu-id="52c1c-103">Signatures</span></span>

<span data-ttu-id="52c1c-104">Сигнатура шейдера — это список параметров, которые либо являются входными, либо выводяти из функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="52c1c-104">A shader signature is a list of the parameters that are either input to or output from a shader function.</span></span> <span data-ttu-id="52c1c-105">В Direct3D 10 смежные этапы эффективно совместно используют массив регистров, где шейдер выходных данных (или стадия конвейера) записывает данные в определенные места в массиве Register, и входной шейдер должен считываться из тех же расположений.</span><span class="sxs-lookup"><span data-stu-id="52c1c-105">In Direct3D 10, adjacent stages effectively share a register array, where the output shader (or pipeline stage) writes data to specific locations in the register array and the input shader must read from the same locations.</span></span> <span data-ttu-id="52c1c-106">API использует подписи шейдера для привязки выходных данных шейдера с входными данными без издержек семантического разрешения.</span><span class="sxs-lookup"><span data-stu-id="52c1c-106">The API uses shader signatures to bind shader outputs with inputs without the overhead of semantic resolution.</span></span>

<span data-ttu-id="52c1c-107">В Direct3D 10 входные подписи формируются из объявления ввода шейдера, а выходная подпись формируется из объявления вывода шейдера.</span><span class="sxs-lookup"><span data-stu-id="52c1c-107">In Direct3D 10, input signatures are generated from a shader-input declaration and the output signature is generated from a shader-output declaration.</span></span> <span data-ttu-id="52c1c-108">Говорят, что входная сигнатура совместима с выходной сигнатурой, когда выходная подпись является строго подмножеством (типом аргумента и порядком совпадений) входной сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="52c1c-108">An input signature is said to be compatible with an output signature when the output signature is a strict subset (argument type and order match) of the input signature.</span></span> <span data-ttu-id="52c1c-109">Самый простой способ добиться этого — связать соответствующие входные и выходные данные шейдера с тем же типом структуры.</span><span class="sxs-lookup"><span data-stu-id="52c1c-109">The most straightforward way to achieve this is to link corresponding shader inputs and outputs by the same structure type.</span></span>

<span data-ttu-id="52c1c-110">Ниже приведен пример совместимых подписей.</span><span class="sxs-lookup"><span data-stu-id="52c1c-110">Here is an example of compatible signatures.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



<span data-ttu-id="52c1c-111">Ниже приведен пример несовместимых подписей. порядок параметров во входной подписи не соответствует порядку в выходной подписи.</span><span class="sxs-lookup"><span data-stu-id="52c1c-111">Here is an example of incompatible signatures; the order of parameters in the input signature does not match the order in the output signature.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



<span data-ttu-id="52c1c-112">Псинворкс является совместимым подмножеством Всаут (первые две записи соответствуют типу и порядку с первыми двумя записями в Всаут).</span><span class="sxs-lookup"><span data-stu-id="52c1c-112">PSInWorks is a compatible subset of VSOut (the first two entries match both type and order with the first two entries in VSOut).</span></span> <span data-ttu-id="52c1c-113">Однако Псинфаилс несовместима, так как порядок не соответствует Всаут.</span><span class="sxs-lookup"><span data-stu-id="52c1c-113">However, PSInFails is incompatible because the ordering does not match with VSOut.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52c1c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="52c1c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52c1c-115">Функции</span><span class="sxs-lookup"><span data-stu-id="52c1c-115">Functions</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




