---
title: Регистр текстурной координаты (Справочник по HLSL PS)
description: Входной регистр шейдера пикселей, содержащий координаты текстуры.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104983916"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a><span data-ttu-id="9cd6c-103">Регистр текстурной координаты (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="9cd6c-103">Texture coordinate register (HLSL PS reference)</span></span>

<span data-ttu-id="9cd6c-104">Входной регистр шейдера пикселей, содержащий координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-104">Pixel shader input register containing texture coordinates.</span></span>



| <span data-ttu-id="9cd6c-105">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="9cd6c-105">Pixel shader versions</span></span>       | <span data-ttu-id="9cd6c-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="9cd6c-106">1\_1</span></span> | <span data-ttu-id="9cd6c-107">1\_2</span><span class="sxs-lookup"><span data-stu-id="9cd6c-107">1\_2</span></span> | <span data-ttu-id="9cd6c-108">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9cd6c-108">1\_3</span></span> | <span data-ttu-id="9cd6c-109">1\_4</span><span class="sxs-lookup"><span data-stu-id="9cd6c-109">1\_4</span></span> | <span data-ttu-id="9cd6c-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9cd6c-110">2\_0</span></span> | <span data-ttu-id="9cd6c-111">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9cd6c-111">2\_sw</span></span> | <span data-ttu-id="9cd6c-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9cd6c-112">2\_x</span></span> | <span data-ttu-id="9cd6c-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9cd6c-113">3\_0</span></span> | <span data-ttu-id="9cd6c-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9cd6c-114">3\_sw</span></span> |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="9cd6c-115">Регистр координаты текстуры</span><span class="sxs-lookup"><span data-stu-id="9cd6c-115">Texture Coordinate Register</span></span> |      |      |      |      | <span data-ttu-id="9cd6c-116">x</span><span class="sxs-lookup"><span data-stu-id="9cd6c-116">x</span></span>    | <span data-ttu-id="9cd6c-117">x</span><span class="sxs-lookup"><span data-stu-id="9cd6c-117">x</span></span>     | <span data-ttu-id="9cd6c-118">x</span><span class="sxs-lookup"><span data-stu-id="9cd6c-118">x</span></span>    | <span data-ttu-id="9cd6c-119">x</span><span class="sxs-lookup"><span data-stu-id="9cd6c-119">x</span></span>    | <span data-ttu-id="9cd6c-120">x</span><span class="sxs-lookup"><span data-stu-id="9cd6c-120">x</span></span>     |



 

<span data-ttu-id="9cd6c-121">Регистр координат текстуры содержит данные о координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-121">A texture coordinate register contains texture coordinate data.</span></span> <span data-ttu-id="9cd6c-122">Перед использованием регистра координат текстуры его необходимо объявить объявлением шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-122">Before a texture coordinate register is used, it must be declared by a pixel shader declaration.</span></span> <span data-ttu-id="9cd6c-123">Дополнительные сведения об объявлении регистра текстуры см. в разделе [дкл-(SM2, SM3-PS ASM)](dcl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="9cd6c-123">For details about how to declare a texture register, see [dcl - (sm2, sm3 - ps asm)](dcl---ps.md).</span></span>

<span data-ttu-id="9cd6c-124">Кроме того, ниже приведены некоторые другие свойства регистров координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-124">In addition, here are some other properties of texture coordinate registers.</span></span>

-   <span data-ttu-id="9cd6c-125">Существует восемь регистров координат текстуры шейдера пикселей, t0 в T7.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-125">There are eight pixel-shader texture coordinate registers, t0 to t7.</span></span>
-   <span data-ttu-id="9cd6c-126">Это регистры только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-126">These are read-only registers.</span></span>
-   <span data-ttu-id="9cd6c-127">Они содержат значения RGBA из четырех компонентов, перебираемые из входных вершин.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-127">They contain four-component RGBA values iterated from input vertices.</span></span>
-   <span data-ttu-id="9cd6c-128">Они содержат высокую точность, высокие значения динамических диапазонов данных, которые интерполируются из данных вершин.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-128">They contain high precision, high dynamic range data values interpolated from the vertex data.</span></span> <span data-ttu-id="9cd6c-129">Значения создаются с интерполяцией с правильной перспективой.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-129">Values are generated with perspective-correct interpolation.</span></span> <span data-ttu-id="9cd6c-130">Данные являются точностью с плавающей запятой и подписываются.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-130">Data is floating-point precision, and is signed.</span></span>
-   <span data-ttu-id="9cd6c-131">В одной инструкции существует максимум один.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-131">There is a maximum of one in a single instruction.</span></span>
-   <span data-ttu-id="9cd6c-132">При нескольких операциях чтения регистра координат текстуры в шейдере должна использоваться идентичная [маска записи регистра назначения](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="9cd6c-132">Multiple reads of a texture coordinate register within a shader must use identical [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="9cd6c-133">Необязательный модификатор частичной точности \[ \_ PP \] применяется к зависимым операциям чтения.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-133">The optional partial precision modifier \[\_pp\] applies to dependent reads.</span></span> <span data-ttu-id="9cd6c-134">Это связано с тем, что частичная точность влияет на арифметические операции, в которых используется регистр текстурной координаты.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-134">This is because partial precision affects arithmetic operations involving the texture coordinate register.</span></span> <span data-ttu-id="9cd6c-135">Он не влияет на точность инструкций по адресу текстуры, так как не влияет на итераторы координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="9cd6c-135">It will not affect the precision of texture address instructions because it does not affect the texture coordinate iterators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cd6c-136">См. также</span><span class="sxs-lookup"><span data-stu-id="9cd6c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cd6c-137">Регистры</span><span class="sxs-lookup"><span data-stu-id="9cd6c-137">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




