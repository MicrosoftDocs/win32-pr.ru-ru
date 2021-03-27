---
title: '\_ \_ модификаторы исходного регистра PS 1 4 для текслд, текскрд'
description: '\_Текслд-PS \_ 1 4 и текскрд-PS с двумя инструкциями по адресу текстуры построителя текстуры версии 1 4 \_ имеют пользовательский синтаксис.'
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/27/2019
ms.locfileid: "104133374"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a><span data-ttu-id="7ed0b-103">\_ \_ модификаторы исходного регистра PS 1 4 для текслд, текскрд</span><span class="sxs-lookup"><span data-stu-id="7ed0b-103">ps\_1\_4 source register modifiers for texld, texcrd</span></span>

<span data-ttu-id="7ed0b-104">\_ [Текслд-PS \_ 1 \_ 4](texld---ps-1-4.md) и [текскрд-PS](texcrd---ps.md)с двумя инструкциями по адресу текстуры построителя текстуры версии 1 4 имеют пользовательский синтаксис.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-104">Two pixel shader version 1\_4 texture address instructions, [texld - ps\_1\_4](texld---ps-1-4.md) and [texcrd - ps](texcrd---ps.md), have custom syntax.</span></span> <span data-ttu-id="7ed0b-105">Эти инструкции поддерживают собственный набор модификаторов исходных регистров, селекторы исходного регистра и маски записи приемника, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-105">These instructions support their own set of source register modifiers, source register selectors, and destination-register write masks, as shown here.</span></span>

## <a name="source-register-modifiers-for-texld-and-texcrd"></a><span data-ttu-id="7ed0b-106">Модификаторы исходного регистра для текслд и текскрд</span><span class="sxs-lookup"><span data-stu-id="7ed0b-106">Source Register Modifiers for texld and texcrd</span></span>

<span data-ttu-id="7ed0b-107">Эти модификаторы обеспечивают возможность проецирования путем деления значений x и y на значения z или w.</span><span class="sxs-lookup"><span data-stu-id="7ed0b-107">These modifiers provide projective divide functionality by dividing the x and y values by either the z or w values.</span></span>



| <span data-ttu-id="7ed0b-108">Модификаторы исходного регистра</span><span class="sxs-lookup"><span data-stu-id="7ed0b-108">Source register modifiers</span></span> | <span data-ttu-id="7ed0b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7ed0b-109">Description</span></span>                | <span data-ttu-id="7ed0b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ed0b-110">Syntax</span></span>       |
|---------------------------|----------------------------|--------------|
| <span data-ttu-id="7ed0b-111">\_DZ</span><span class="sxs-lookup"><span data-stu-id="7ed0b-111">\_dz</span></span>                      | <span data-ttu-id="7ed0b-112">Разделить компоненты x, y по z</span><span class="sxs-lookup"><span data-stu-id="7ed0b-112">Divide x,y components by z</span></span> | <span data-ttu-id="7ed0b-113">регистрация \_ DZ</span><span class="sxs-lookup"><span data-stu-id="7ed0b-113">register\_dz</span></span> |
| <span data-ttu-id="7ed0b-114">\_db</span><span class="sxs-lookup"><span data-stu-id="7ed0b-114">\_db</span></span>                      | <span data-ttu-id="7ed0b-115">Разделить компоненты x, y по z</span><span class="sxs-lookup"><span data-stu-id="7ed0b-115">Divide x,y components by z</span></span> | <span data-ttu-id="7ed0b-116">регистрация \_ базы данных</span><span class="sxs-lookup"><span data-stu-id="7ed0b-116">register\_db</span></span> |
| <span data-ttu-id="7ed0b-117">\_dw</span><span class="sxs-lookup"><span data-stu-id="7ed0b-117">\_dw</span></span>                      | <span data-ttu-id="7ed0b-118">Деление компонентов x, y на w</span><span class="sxs-lookup"><span data-stu-id="7ed0b-118">Divide x,y components by w</span></span> | <span data-ttu-id="7ed0b-119">регистрация \_ хранилища данных</span><span class="sxs-lookup"><span data-stu-id="7ed0b-119">register\_dw</span></span> |
| <span data-ttu-id="7ed0b-120">\_Da</span><span class="sxs-lookup"><span data-stu-id="7ed0b-120">\_da</span></span>                      | <span data-ttu-id="7ed0b-121">Деление компонентов x, y на w</span><span class="sxs-lookup"><span data-stu-id="7ed0b-121">Divide x,y components by w</span></span> | <span data-ttu-id="7ed0b-122">регистрация \_ Da</span><span class="sxs-lookup"><span data-stu-id="7ed0b-122">register\_da</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="7ed0b-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ed0b-123">Remarks</span></span>

<span data-ttu-id="7ed0b-124">\_Модификатор DZ или \_ DB выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7ed0b-124">The \_dz or \_db modifier does the following:</span></span>


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



<span data-ttu-id="7ed0b-125">\_Модификатор DW или \_ Da выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7ed0b-125">The \_dw or \_da modifier does the following:</span></span>


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a><span data-ttu-id="7ed0b-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7ed0b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed0b-127">Модификаторы исходных регистров исходного шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="7ed0b-127">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




