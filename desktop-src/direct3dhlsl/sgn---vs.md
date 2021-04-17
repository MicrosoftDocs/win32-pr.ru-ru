---
title: СГН — VS
description: Вычисление знака входных данных.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412184"
---
# <a name="sgn---vs"></a><span data-ttu-id="4f93e-103">СГН — VS</span><span class="sxs-lookup"><span data-stu-id="4f93e-103">sgn - vs</span></span>

<span data-ttu-id="4f93e-104">Вычисление знака входных данных.</span><span class="sxs-lookup"><span data-stu-id="4f93e-104">Computes the sign of the input.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f93e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f93e-105">Syntax</span></span>



| <span data-ttu-id="4f93e-106">СГН DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="4f93e-106">sgn dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="4f93e-107">где</span><span class="sxs-lookup"><span data-stu-id="4f93e-107">where</span></span>

-   <span data-ttu-id="4f93e-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="4f93e-108">dst is the destination register.</span></span>
-   <span data-ttu-id="4f93e-109">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="4f93e-109">src0 is a source register.</span></span>
-   <span data-ttu-id="4f93e-110">src1 — это временный регистр, содержащий промежуточные результаты.</span><span class="sxs-lookup"><span data-stu-id="4f93e-110">src1 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="4f93e-111">После выполнения, содержимое не определено.</span><span class="sxs-lookup"><span data-stu-id="4f93e-111">Following execution, contents are undefined.</span></span>
-   <span data-ttu-id="4f93e-112">src2 — это временный регистр, содержащий промежуточные результаты.</span><span class="sxs-lookup"><span data-stu-id="4f93e-112">src2 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="4f93e-113">После выполнения, содержимое не определено.</span><span class="sxs-lookup"><span data-stu-id="4f93e-113">Following execution, contents are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f93e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f93e-114">Remarks</span></span>



| <span data-ttu-id="4f93e-115">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="4f93e-115">Vertex shader versions</span></span> | <span data-ttu-id="4f93e-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="4f93e-116">1\_1</span></span> | <span data-ttu-id="4f93e-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f93e-117">2\_0</span></span> | <span data-ttu-id="4f93e-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4f93e-118">2\_x</span></span> | <span data-ttu-id="4f93e-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4f93e-119">2\_sw</span></span> | <span data-ttu-id="4f93e-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f93e-120">3\_0</span></span> | <span data-ttu-id="4f93e-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4f93e-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4f93e-122">сгн</span><span class="sxs-lookup"><span data-stu-id="4f93e-122">sgn</span></span>                    |      | <span data-ttu-id="4f93e-123">x</span><span class="sxs-lookup"><span data-stu-id="4f93e-123">x</span></span>    | <span data-ttu-id="4f93e-124">x</span><span class="sxs-lookup"><span data-stu-id="4f93e-124">x</span></span>    | <span data-ttu-id="4f93e-125">x</span><span class="sxs-lookup"><span data-stu-id="4f93e-125">x</span></span>     | <span data-ttu-id="4f93e-126">x</span><span class="sxs-lookup"><span data-stu-id="4f93e-126">x</span></span>    | <span data-ttu-id="4f93e-127">x</span><span class="sxs-lookup"><span data-stu-id="4f93e-127">x</span></span>     |



 

<span data-ttu-id="4f93e-128">Эта инструкция работает, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4f93e-128">This instruction works as shown below.</span></span>


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



<span data-ttu-id="4f93e-129">src1 и src2 должны быть разными [временными регистрами](dx9-graphics-reference-asm-vs-registers-temporary.md).</span><span class="sxs-lookup"><span data-stu-id="4f93e-129">src1 and src2 must be different [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f93e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4f93e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f93e-131">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="4f93e-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




