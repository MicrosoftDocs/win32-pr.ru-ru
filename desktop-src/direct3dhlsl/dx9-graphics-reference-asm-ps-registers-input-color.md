---
title: Регистр цвета ввода
description: Входной регистр шейдера пикселей, содержащий цвет вершины.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411434"
---
# <a name="input-color-register"></a><span data-ttu-id="912dd-103">Регистр цвета ввода</span><span class="sxs-lookup"><span data-stu-id="912dd-103">Input Color Register</span></span>

<span data-ttu-id="912dd-104">Входной регистр шейдера пикселей, содержащий цвет вершины.</span><span class="sxs-lookup"><span data-stu-id="912dd-104">Pixel shader input register containing vertex color.</span></span>

## <a name="syntax"></a><span data-ttu-id="912dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="912dd-105">Syntax</span></span>


```
dcl v#.writeMask
```



<span data-ttu-id="912dd-106">где:</span><span class="sxs-lookup"><span data-stu-id="912dd-106">where:</span></span>

-   <span data-ttu-id="912dd-107">[дкл-(SM2, SM3-PS ASM)](dcl---ps.md) является инструкцией по объявлению регистра.</span><span class="sxs-lookup"><span data-stu-id="912dd-107">[dcl - (sm2, sm3 - ps asm)](dcl---ps.md) is a register declaration instruction.</span></span>
-   <span data-ttu-id="912dd-108">v является входным регистром и \# является номером регистра.</span><span class="sxs-lookup"><span data-stu-id="912dd-108">v is an input register and \# is the register number.</span></span> <span data-ttu-id="912dd-109">Количество допустимых регистров определяется версией шейдера.</span><span class="sxs-lookup"><span data-stu-id="912dd-109">The number of registers allowed is determined by the shader version.</span></span>
-   <span data-ttu-id="912dd-110">Вритемаск определяет, какие компоненты записываются (до четырех).</span><span class="sxs-lookup"><span data-stu-id="912dd-110">writeMask determines which components (up to four) are written.</span></span> <span data-ttu-id="912dd-111">Допустимые компоненты: (x, y, z, w) или (r, g, b, a).</span><span class="sxs-lookup"><span data-stu-id="912dd-111">Valid components are: (x,y,z,w) or (r,g,b,a).</span></span>

## <a name="remarks"></a><span data-ttu-id="912dd-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="912dd-112">Remarks</span></span>

<span data-ttu-id="912dd-113">Регистры цвета — это регистры только для чтения.</span><span class="sxs-lookup"><span data-stu-id="912dd-113">Color registers are read-only registers.</span></span> <span data-ttu-id="912dd-114">Каждый регистр содержит значения RGBA из четырех компонентов, перебираемые из входных вершин.</span><span class="sxs-lookup"><span data-stu-id="912dd-114">Each register contains four-component RGBA values iterated from input vertices.</span></span> <span data-ttu-id="912dd-115">Они имеют меньшую точность, чем большинство регистров, но гарантированно содержат 8 бит неподписанных данных в диапазоне (0, + 1).</span><span class="sxs-lookup"><span data-stu-id="912dd-115">They have lower precision than most registers, guaranteed to have 8 bits of unsigned data in the range (0, +1).</span></span> <span data-ttu-id="912dd-116">В одной инструкции нельзя использовать больше одного.</span><span class="sxs-lookup"><span data-stu-id="912dd-116">You cannot use more than one in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="912dd-117">См. также</span><span class="sxs-lookup"><span data-stu-id="912dd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="912dd-118">Регистры</span><span class="sxs-lookup"><span data-stu-id="912dd-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="912dd-119">реестр PS 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 регистры</span><span class="sxs-lookup"><span data-stu-id="912dd-119">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="912dd-120">\_ \_ регистры PS 2 0</span><span class="sxs-lookup"><span data-stu-id="912dd-120">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="912dd-121">\_ \_ регистры PS 2 x</span><span class="sxs-lookup"><span data-stu-id="912dd-121">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="912dd-122">\_ \_ регистры PS 3 0</span><span class="sxs-lookup"><span data-stu-id="912dd-122">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




