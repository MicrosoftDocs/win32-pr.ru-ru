---
title: Отрицательный Регистр исходного регистра
description: Выполняет отрицание (y-x) для всех компонентов регистрации.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067864"
---
# <a name="source-register-negate"></a><span data-ttu-id="ac346-103">Отрицательный Регистр исходного регистра</span><span class="sxs-lookup"><span data-stu-id="ac346-103">Source Register Negate</span></span>

<span data-ttu-id="ac346-104">Выполняет отрицание (y =-x) для всех компонентов регистрации.</span><span class="sxs-lookup"><span data-stu-id="ac346-104">Performs a negate (y = -x), on all register components.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac346-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac346-105">Syntax</span></span>


```
- register
```



## <a name="registers"></a><span data-ttu-id="ac346-106">Регистры</span><span class="sxs-lookup"><span data-stu-id="ac346-106">Registers</span></span>

<span data-ttu-id="ac346-107">Исходный регистр.</span><span class="sxs-lookup"><span data-stu-id="ac346-107">Source Register.</span></span> <span data-ttu-id="ac346-108">Дополнительные сведения о типах регистров см. в описании [ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ регистров PS 1 1 PS 1 2](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="ac346-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac346-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac346-109">Remarks</span></span>

<span data-ttu-id="ac346-110">Содержимое регистра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="ac346-110">The contents of the register are not changed.</span></span> <span data-ttu-id="ac346-111">Модификатор применяется только к данным, считанным из регистра.</span><span class="sxs-lookup"><span data-stu-id="ac346-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="ac346-112">Операция отрицания применяется ко всем четырем цветовым каналам (RGBA).</span><span class="sxs-lookup"><span data-stu-id="ac346-112">The negate operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="ac346-113">Эта операция выполняется после любого другого модификатора, присутствующего в том же аргументе.</span><span class="sxs-lookup"><span data-stu-id="ac346-113">This operation is performed after any other modifiers present on the same argument.</span></span>

<span data-ttu-id="ac346-114">Этот модификатор является взаимоисключающим с [инверсией исходного регистра](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , поэтому он не может быть применен к тому же регистру.</span><span class="sxs-lookup"><span data-stu-id="ac346-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="ac346-115">Этот модификатор предназначен для использования только с арифметическими инструкциями.</span><span class="sxs-lookup"><span data-stu-id="ac346-115">This modifier is for use only with arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="ac346-116">Например, .</span><span class="sxs-lookup"><span data-stu-id="ac346-116">Example</span></span>

<span data-ttu-id="ac346-117">В следующем примере показано, как использовать этот модификатор.</span><span class="sxs-lookup"><span data-stu-id="ac346-117">The following example shows how to use this modifier.</span></span>


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a><span data-ttu-id="ac346-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ac346-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac346-119">Модификаторы исходных регистров исходного шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="ac346-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




