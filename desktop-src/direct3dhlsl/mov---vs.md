---
title: MOV – VS
description: Перемещение данных с плавающей запятой между регистрами.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784989"
---
# <a name="mov---vs"></a><span data-ttu-id="fa865-103">MOV – VS</span><span class="sxs-lookup"><span data-stu-id="fa865-103">mov - vs</span></span>

<span data-ttu-id="fa865-104">Перемещение данных с плавающей запятой между регистрами.</span><span class="sxs-lookup"><span data-stu-id="fa865-104">Move floating-point data between registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa865-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa865-105">Syntax</span></span>



| <span data-ttu-id="fa865-106">MOV DST, src</span><span class="sxs-lookup"><span data-stu-id="fa865-106">mov dst, src</span></span> |
|--------------|



 

<span data-ttu-id="fa865-107">где</span><span class="sxs-lookup"><span data-stu-id="fa865-107">where</span></span>

-   <span data-ttu-id="fa865-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="fa865-108">dst is the destination register.</span></span>
-   <span data-ttu-id="fa865-109">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="fa865-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa865-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa865-110">Remarks</span></span>



| <span data-ttu-id="fa865-111">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="fa865-111">Vertex shader versions</span></span> | <span data-ttu-id="fa865-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="fa865-112">1\_1</span></span> | <span data-ttu-id="fa865-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fa865-113">2\_0</span></span> | <span data-ttu-id="fa865-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fa865-114">2\_x</span></span> | <span data-ttu-id="fa865-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fa865-115">2\_sw</span></span> | <span data-ttu-id="fa865-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fa865-116">3\_0</span></span> | <span data-ttu-id="fa865-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fa865-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="fa865-118">функцию</span><span class="sxs-lookup"><span data-stu-id="fa865-118">mov</span></span>                    | <span data-ttu-id="fa865-119">x</span><span class="sxs-lookup"><span data-stu-id="fa865-119">x</span></span>    | <span data-ttu-id="fa865-120">x</span><span class="sxs-lookup"><span data-stu-id="fa865-120">x</span></span>    | <span data-ttu-id="fa865-121">x</span><span class="sxs-lookup"><span data-stu-id="fa865-121">x</span></span>    | <span data-ttu-id="fa865-122">x</span><span class="sxs-lookup"><span data-stu-id="fa865-122">x</span></span>     | <span data-ttu-id="fa865-123">x</span><span class="sxs-lookup"><span data-stu-id="fa865-123">x</span></span>    | <span data-ttu-id="fa865-124">x</span><span class="sxs-lookup"><span data-stu-id="fa865-124">x</span></span>     |



 

<span data-ttu-id="fa865-125">Может использоваться для данных с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="fa865-125">Can be used for floating point data.</span></span> <span data-ttu-id="fa865-126">Для версии VS \_ 1 \_ можно также использовать для записи регистра адресов.</span><span class="sxs-lookup"><span data-stu-id="fa865-126">For version vs\_1\_1, it can also be used to write the address register.</span></span> <span data-ttu-id="fa865-127">При использовании для обновления регистров адресов значения преобразуются из плавающей запятой с помощью функции округления к ближайшему.</span><span class="sxs-lookup"><span data-stu-id="fa865-127">When used to update address registers, the values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="fa865-128">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="fa865-128">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a><span data-ttu-id="fa865-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fa865-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa865-130">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="fa865-130">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




