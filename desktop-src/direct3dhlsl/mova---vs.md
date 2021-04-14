---
title: МОВА — VS
description: Перемещение данных из регистра с плавающей запятой в регистр адресов a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983897"
---
# <a name="mova---vs"></a><span data-ttu-id="1a2af-103">МОВА — VS</span><span class="sxs-lookup"><span data-stu-id="1a2af-103">mova - vs</span></span>

<span data-ttu-id="1a2af-104">Перемещение данных из регистра с плавающей запятой в [регистр адресов](dx9-graphics-reference-asm-vs-registers-address.md)a0.</span><span class="sxs-lookup"><span data-stu-id="1a2af-104">Move data from a floating point register to the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a2af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a2af-105">Syntax</span></span>



| <span data-ttu-id="1a2af-106">МОВА DST, src</span><span class="sxs-lookup"><span data-stu-id="1a2af-106">mova dst, src</span></span> |
|---------------|



 

<span data-ttu-id="1a2af-107">где</span><span class="sxs-lookup"><span data-stu-id="1a2af-107">where</span></span>

-   <span data-ttu-id="1a2af-108">DST должен быть [регистром адресов](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span><span class="sxs-lookup"><span data-stu-id="1a2af-108">dst must be the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>
-   <span data-ttu-id="1a2af-109">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="1a2af-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a2af-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a2af-110">Remarks</span></span>



| <span data-ttu-id="1a2af-111">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="1a2af-111">Vertex shader versions</span></span> | <span data-ttu-id="1a2af-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="1a2af-112">1\_1</span></span> | <span data-ttu-id="1a2af-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1a2af-113">2\_0</span></span> | <span data-ttu-id="1a2af-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1a2af-114">2\_x</span></span> | <span data-ttu-id="1a2af-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1a2af-115">2\_sw</span></span> | <span data-ttu-id="1a2af-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1a2af-116">3\_0</span></span> | <span data-ttu-id="1a2af-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1a2af-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="1a2af-118">мова</span><span class="sxs-lookup"><span data-stu-id="1a2af-118">mova</span></span>                   |      | <span data-ttu-id="1a2af-119">x</span><span class="sxs-lookup"><span data-stu-id="1a2af-119">x</span></span>    | <span data-ttu-id="1a2af-120">x</span><span class="sxs-lookup"><span data-stu-id="1a2af-120">x</span></span>    | <span data-ttu-id="1a2af-121">x</span><span class="sxs-lookup"><span data-stu-id="1a2af-121">x</span></span>     | <span data-ttu-id="1a2af-122">x</span><span class="sxs-lookup"><span data-stu-id="1a2af-122">x</span></span>    | <span data-ttu-id="1a2af-123">x</span><span class="sxs-lookup"><span data-stu-id="1a2af-123">x</span></span>     |



 

<span data-ttu-id="1a2af-124">Перемещает данные с плавающей запятой в целочисленный регистр.</span><span class="sxs-lookup"><span data-stu-id="1a2af-124">Moves floating point data to an integer register.</span></span> <span data-ttu-id="1a2af-125">Значения преобразуются из плавающей запятой с помощью функции округления к ближайшему.</span><span class="sxs-lookup"><span data-stu-id="1a2af-125">The values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="1a2af-126">Регистр адреса — это единственный допустимый регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="1a2af-126">The address register is the only destination register allowed.</span></span>

<span data-ttu-id="1a2af-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="1a2af-127">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



<span data-ttu-id="1a2af-128">Для версий 2 \_ x и выше регистр адресов является вектором компонентов.</span><span class="sxs-lookup"><span data-stu-id="1a2af-128">For versions 2\_x and above, the address register is a component vector.</span></span> <span data-ttu-id="1a2af-129">Поэтому разрешена любая маска записи.</span><span class="sxs-lookup"><span data-stu-id="1a2af-129">Therefore, any write mask is allowed.</span></span>


```
mova a0.xz, r0
```



## <a name="related-topics"></a><span data-ttu-id="1a2af-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1a2af-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a2af-131">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="1a2af-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




