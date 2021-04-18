---
description: Эти константы применяются к переменным эффектов.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: Константы D3D10_EFFECT_VARIABLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701188"
---
# <a name="d3d10_effect_variable-constants"></a><span data-ttu-id="31058-103">\_ \_ Константы ПЕРЕМЕННЫХ эффектов D3D10</span><span class="sxs-lookup"><span data-stu-id="31058-103">D3D10\_EFFECT\_VARIABLE Constants</span></span>

<span data-ttu-id="31058-104">Эти константы применяются к переменным эффектов.</span><span class="sxs-lookup"><span data-stu-id="31058-104">These constants apply to effect variables.</span></span>



| <span data-ttu-id="31058-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="31058-105">\#define</span></span>                                       | <span data-ttu-id="31058-106">Описание</span><span class="sxs-lookup"><span data-stu-id="31058-106">Description</span></span>  | <span data-ttu-id="31058-107">Значение</span><span class="sxs-lookup"><span data-stu-id="31058-107">Value</span></span>                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31058-108">\_Заметка \_ переменной влияния D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="31058-108">D3D10\_EFFECT\_VARIABLE\_ANNOTATION</span></span>            | <span data-ttu-id="31058-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="31058-109">1 << 0</span></span> | <span data-ttu-id="31058-110">Указывает, что это заметка или глобальная переменная.</span><span class="sxs-lookup"><span data-stu-id="31058-110">Indicates that this is an annotation or a global variable.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="31058-111">\_Переменная влияния \_ D3D10 \_ poold</span><span class="sxs-lookup"><span data-stu-id="31058-111">D3D10\_EFFECT\_VARIABLE\_POOLED</span></span>                | <span data-ttu-id="31058-112">1 << 1</span><span class="sxs-lookup"><span data-stu-id="31058-112">1 << 1</span></span> | <span data-ttu-id="31058-113">Указывает, что эта переменная или буфер константы находятся в пуле эффектов.</span><span class="sxs-lookup"><span data-stu-id="31058-113">Indicates that this variable or constant buffer resides in an effect pool.</span></span> <span data-ttu-id="31058-114">Если этот флаг не установлен, переменная размещается в отдельном или дочернем эффекте (отдельные эффекты возвращают значение false из [**ID3D10Effect:: Pool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool)).</span><span class="sxs-lookup"><span data-stu-id="31058-114">If this flag is not set, then the variable resides in a standalone effect or a child effect (standalone effects return false from [**ID3D10Effect::IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span></span> |
| <span data-ttu-id="31058-115">\_Переменная влияния \_ D3D10 \_ явная \_ \_ точка привязки</span><span class="sxs-lookup"><span data-stu-id="31058-115">D3D10\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT</span></span> | <span data-ttu-id="31058-116">1 << 2</span><span class="sxs-lookup"><span data-stu-id="31058-116">1 << 2</span></span> | <span data-ttu-id="31058-117">Указывает, что переменная была явно привязана с помощью ключевого слова Register.</span><span class="sxs-lookup"><span data-stu-id="31058-117">Indicates that the variable has been explicitly bound using the register keyword.</span></span>                                                                                                                                                                                 |



 

<span data-ttu-id="31058-118">Эти флаги определяются как макросы в d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="31058-118">These flags are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31058-119">См. также</span><span class="sxs-lookup"><span data-stu-id="31058-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31058-120">Константы эффектов (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="31058-120">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



