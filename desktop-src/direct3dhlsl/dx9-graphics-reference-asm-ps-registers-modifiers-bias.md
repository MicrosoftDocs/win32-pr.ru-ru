---
title: Смещение исходного регистра
description: Вычтите 0,5 из всех компонентов.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986847"
---
# <a name="source-register-bias"></a><span data-ttu-id="3cd55-103">Смещение исходного регистра</span><span class="sxs-lookup"><span data-stu-id="3cd55-103">Source Register Bias</span></span>

<span data-ttu-id="3cd55-104">Вычтите 0,5 из всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="3cd55-104">Subtract 0.5 from all components.</span></span>

## <a name="registers"></a><span data-ttu-id="3cd55-105">Регистры</span><span class="sxs-lookup"><span data-stu-id="3cd55-105">Registers</span></span>

<span data-ttu-id="3cd55-106">Исходный регистр.</span><span class="sxs-lookup"><span data-stu-id="3cd55-106">Source register.</span></span> <span data-ttu-id="3cd55-107">Дополнительные сведения о типах регистров см. в описании [ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ регистров PS 1 1 PS 1 2](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="3cd55-107">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd55-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="3cd55-108">Remarks</span></span>

<span data-ttu-id="3cd55-109">Содержимое регистра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="3cd55-109">The contents of the register are not changed.</span></span> <span data-ttu-id="3cd55-110">Модификатор применяется только к данным, считанным из регистра.</span><span class="sxs-lookup"><span data-stu-id="3cd55-110">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="3cd55-111">Этот сдвиг применяется ко всем четырем цветовым каналам (RGBA) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3cd55-111">The bias is applied to all four color channels (RGBA) as follows:</span></span>


```
output = (input - 0.5)
```



<span data-ttu-id="3cd55-112">Результатом является изменение данных, которые находятся в диапазоне от 0 до 1, в диапазоне от-0,5 до 0,5.</span><span class="sxs-lookup"><span data-stu-id="3cd55-112">The effect is to modify data that was in the range 0 to 1 to be in the range -0.5 to 0.5.</span></span> <span data-ttu-id="3cd55-113">Применение смещения к данным за пределами этого диапазона может привести к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="3cd55-113">Applying bias to data outside this range may produce undefined results.</span></span>

> [!Note]  
> <span data-ttu-id="3cd55-114">Этот модификатор является взаимоисключающим с [инверсией в исходном регистре](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), поэтому он не может быть применен к тому же регистру.</span><span class="sxs-lookup"><span data-stu-id="3cd55-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

 

<span data-ttu-id="3cd55-115">Этот модификатор предназначен для использования с арифметическими инструкциями.</span><span class="sxs-lookup"><span data-stu-id="3cd55-115">This modifier is for use with the arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="3cd55-116">Например, .</span><span class="sxs-lookup"><span data-stu-id="3cd55-116">Example</span></span>

<span data-ttu-id="3cd55-117">В этом примере выполняется та же операция, что и для D3DTOP \_ аддсигнед в DirectX 6,0 и 7,0 с несколькими синтаксисами текстуры.</span><span class="sxs-lookup"><span data-stu-id="3cd55-117">This example performs the same operation as D3DTOP\_ADDSIGNED in DirectX 6.0 and 7.0 multiple texture syntax.</span></span>


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a><span data-ttu-id="3cd55-118">См. также</span><span class="sxs-lookup"><span data-stu-id="3cd55-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cd55-119">Модификаторы исходных регистров исходного шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="3cd55-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




