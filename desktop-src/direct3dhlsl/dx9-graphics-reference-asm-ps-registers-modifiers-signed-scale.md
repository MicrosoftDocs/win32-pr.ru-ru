---
title: Масштабирование, подписанное исходным регистром
description: Вычитает 0,5 из каждого канала и масштабирует результат по 2,0. Имя bx2 берется из смещения и масштаба-2, которое представляет собой выполняемую операцию.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259104"
---
# <a name="source-register-signed-scaling"></a><span data-ttu-id="ebcfc-104">Масштабирование, подписанное исходным регистром</span><span class="sxs-lookup"><span data-stu-id="ebcfc-104">Source Register Signed Scaling</span></span>

<span data-ttu-id="ebcfc-105">Вычитает 0,5 из каждого канала и масштабирует результат по 2,0.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-105">Subtracts 0.5 from each channel and scales the result by 2.0.</span></span> <span data-ttu-id="ebcfc-106">Имя bx2 берется из смещения и масштаба-2, которое представляет собой выполняемую операцию.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-106">The name bx2 comes from bias and scale-times-two, which is the operation it performs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebcfc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebcfc-107">Syntax</span></span>


```
source register_bx2
```



## <a name="register"></a><span data-ttu-id="ebcfc-108">Регистрация</span><span class="sxs-lookup"><span data-stu-id="ebcfc-108">Register</span></span>

<span data-ttu-id="ebcfc-109">Исходный регистр.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-109">Source Register.</span></span> <span data-ttu-id="ebcfc-110">Дополнительные сведения о типах регистров см. в описании [ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ регистров PS 1 1 PS 1 2](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-110">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ebcfc-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="ebcfc-111">Remarks</span></span>

<span data-ttu-id="ebcfc-112">Эта операция обычно используется для расширения данных с \[ 0,0 до 1,0 \] 1,0 до \[ 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="ebcfc-112">This operation is commonly used to expand data from \[0.0 to 1.0\] to \[-1.0 to 1.0\].</span></span> <span data-ttu-id="ebcfc-113">Этот модификатор предназначен для использования с арифметическими инструкциями.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-113">This modifier is designed for use with the arithmetic instructions.</span></span> <span data-ttu-id="ebcfc-114">Этот модификатор обычно используется в качестве входных данных для инструкции продукта с точкой ([DP3-PS](dp3---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="ebcfc-114">This modifier is commonly used on inputs to the dot product instruction ([dp3 - ps](dp3---ps.md)).</span></span> <span data-ttu-id="ebcfc-115">Использование \_ bx2 для данных за пределами диапазона от 0 до 1 может привести к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-115">Using \_bx2 on data outside the range 0 to 1 may produce undefined results.</span></span>

<span data-ttu-id="ebcfc-116">Операция масштабирования со знаком применяется к данным, считанным из регистра до выполнения следующей инструкции.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-116">The signed scaling operation is applied to the data read from the register before the next instruction is run.</span></span> <span data-ttu-id="ebcfc-117">Операция применяется ко всем четырем цветовым каналам (RGBA) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ebcfc-117">The operation is applied to all four color channels (RGBA) as follows:</span></span>


```
y = 2(x - 0.5)
```



<span data-ttu-id="ebcfc-118">Содержимое регистра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-118">The contents of the register are not changed.</span></span> <span data-ttu-id="ebcfc-119">Модификатор применяется только к данным, считанным из регистра.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-119">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="ebcfc-120">Этот модификатор является взаимоисключающим с [инверсией исходного регистра](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , поэтому он не может быть применен к тому же регистру.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-120">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="ebcfc-121">Сведения о версии:</span><span class="sxs-lookup"><span data-stu-id="ebcfc-121">Version information:</span></span>

-   <span data-ttu-id="ebcfc-122">Для PS \_ 1 \_ 0 и PS \_ 1 \_ 1 можно использовать \_ bx2 на любом исходном реестре для получения инструкций по текстуре в форме texm3x2 \* и texm3x3 \* .</span><span class="sxs-lookup"><span data-stu-id="ebcfc-122">For ps\_1\_0 and ps\_1\_1, you can use \_bx2 on any source register for texture instructions of the form texm3x2\* and texm3x3\*.</span></span> <span data-ttu-id="ebcfc-123">\_bx2 не может использоваться ни в одной из других инструкций текстуры, таких как [texreg2ar-PS](texreg2ar---ps.md) или [texreg2gb-PS](texreg2gb---ps.md).</span><span class="sxs-lookup"><span data-stu-id="ebcfc-123">\_bx2 cannot be used on any of the other texture instructions such as [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md).</span></span>
-   <span data-ttu-id="ebcfc-124">Для PS \_ 1 \_ 2 и PS \_ 1 \_ 3 можно использовать \_ bx2 на любом исходном реестре для любой инструкции Да, \* Кроме: [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [тексбем-PS](texbem---ps.md) или [тексбемл-PS](texbeml---ps.md).</span><span class="sxs-lookup"><span data-stu-id="ebcfc-124">For ps\_1\_2 and ps\_1\_3, you can use \_bx2 on any source register for any tex\* instruction except: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) or [texbeml - ps](texbeml---ps.md).</span></span>

## <a name="example"></a><span data-ttu-id="ebcfc-125">Например, .</span><span class="sxs-lookup"><span data-stu-id="ebcfc-125">Example</span></span>

<span data-ttu-id="ebcfc-126">В этом примере показана текстура, преобразование данных в диапазон от-1 до + 1 и вычисление произведения точки.</span><span class="sxs-lookup"><span data-stu-id="ebcfc-126">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a><span data-ttu-id="ebcfc-127">См. также</span><span class="sxs-lookup"><span data-stu-id="ebcfc-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebcfc-128">Модификаторы исходных регистров исходного шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="ebcfc-128">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




