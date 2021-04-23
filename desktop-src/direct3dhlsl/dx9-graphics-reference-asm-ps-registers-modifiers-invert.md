---
title: Инверсия исходного регистра
description: Выполняет вычисление (1 значение) для каждого канала указанного регистра.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983744"
---
# <a name="source-register-invert"></a><span data-ttu-id="ccf0c-103">Инверсия исходного регистра</span><span class="sxs-lookup"><span data-stu-id="ccf0c-103">Source Register Invert</span></span>

<span data-ttu-id="ccf0c-104">Выполняет вычисление (1 значение) для каждого канала указанного регистра.</span><span class="sxs-lookup"><span data-stu-id="ccf0c-104">Performs a (1 - value) calculation for each channel of the specified register.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf0c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccf0c-105">Syntax</span></span>


```
1 - register
```



## <a name="registers"></a><span data-ttu-id="ccf0c-106">Регистры</span><span class="sxs-lookup"><span data-stu-id="ccf0c-106">Registers</span></span>

<span data-ttu-id="ccf0c-107">Исходный регистр.</span><span class="sxs-lookup"><span data-stu-id="ccf0c-107">Source Register.</span></span> <span data-ttu-id="ccf0c-108">Дополнительные сведения о типах регистров см. в описании [ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ регистров PS 1 1 PS 1 2](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="ccf0c-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf0c-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="ccf0c-109">Remarks</span></span>

<span data-ttu-id="ccf0c-110">Содержимое регистра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="ccf0c-110">The contents of the register are not changed.</span></span> <span data-ttu-id="ccf0c-111">Модификатор применяется только к данным, считанным из регистра.</span><span class="sxs-lookup"><span data-stu-id="ccf0c-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="ccf0c-112">Операция инвертирования применяется ко всем четырем цветовым каналам (RGBA).</span><span class="sxs-lookup"><span data-stu-id="ccf0c-112">The invert operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="ccf0c-113">Этот модификатор можно использовать только с арифметическими инструкциями.</span><span class="sxs-lookup"><span data-stu-id="ccf0c-113">This modifier can be used only with arithmetic instructions.</span></span> <span data-ttu-id="ccf0c-114">Кроме того, этот модификатор нельзя сочетать с другой [маской записи регистра назначения](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="ccf0c-114">In addition, this modifier cannot be combined with the other [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="example"></a><span data-ttu-id="ccf0c-115">Например, .</span><span class="sxs-lookup"><span data-stu-id="ccf0c-115">Example</span></span>

<span data-ttu-id="ccf0c-116">В этом примере используется инверсия для создания дополнения для Register R1.</span><span class="sxs-lookup"><span data-stu-id="ccf0c-116">This example uses inversion to generate the complement of register r1.</span></span>


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a><span data-ttu-id="ccf0c-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ccf0c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccf0c-118">Модификаторы исходных регистров исходного шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="ccf0c-118">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




