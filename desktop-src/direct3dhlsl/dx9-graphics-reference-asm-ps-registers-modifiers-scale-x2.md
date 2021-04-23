---
title: Масштаб исходного регистра x 2
description: Умножьте значение на два, прежде чем использовать его в инструкции.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983741"
---
# <a name="source-register-scale-x-2"></a><span data-ttu-id="45c40-103">Масштаб исходного регистра x 2</span><span class="sxs-lookup"><span data-stu-id="45c40-103">Source Register Scale x 2</span></span>

<span data-ttu-id="45c40-104">Умножьте значение на два, прежде чем использовать его в инструкции.</span><span class="sxs-lookup"><span data-stu-id="45c40-104">Multiply the value by two before using it in the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="45c40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45c40-105">Syntax</span></span>


```
register_x2
```



## <a name="register"></a><span data-ttu-id="45c40-106">Регистрация</span><span class="sxs-lookup"><span data-stu-id="45c40-106">Register</span></span>

<span data-ttu-id="45c40-107">Исходный регистр.</span><span class="sxs-lookup"><span data-stu-id="45c40-107">Source register.</span></span> <span data-ttu-id="45c40-108">Дополнительные сведения о типах регистров см. в описании [ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ регистров PS 1 1 PS 1 2](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="45c40-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="45c40-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="45c40-109">Remarks</span></span>

<span data-ttu-id="45c40-110">Содержимое регистра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="45c40-110">The contents of the register are not changed.</span></span> <span data-ttu-id="45c40-111">Модификатор применяется только к данным, считанным из регистра.</span><span class="sxs-lookup"><span data-stu-id="45c40-111">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="45c40-112">Этот модификатор является взаимоисключающим с [инверсией в исходном регистре](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), поэтому он не может быть применен к тому же регистру.</span><span class="sxs-lookup"><span data-stu-id="45c40-112">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

<span data-ttu-id="45c40-113">Этот модификатор доступен только для арифметических инструкций в версии 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="45c40-113">This modifier is only available to arithmetic instructions in version 1\_4.</span></span>

## <a name="example"></a><span data-ttu-id="45c40-114">Например, .</span><span class="sxs-lookup"><span data-stu-id="45c40-114">Example</span></span>

<span data-ttu-id="45c40-115">В этом примере показана текстура, преобразование данных в диапазон от-1 до + 1 и вычисление произведения точки.</span><span class="sxs-lookup"><span data-stu-id="45c40-115">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a><span data-ttu-id="45c40-116">См. также</span><span class="sxs-lookup"><span data-stu-id="45c40-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c40-117">Модификаторы исходных регистров исходного шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="45c40-117">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




