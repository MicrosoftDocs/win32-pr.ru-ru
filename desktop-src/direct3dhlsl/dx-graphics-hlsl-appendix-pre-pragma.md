---
title: " Директива pragma"
description: Директива препроцессора, которая предоставляет зависящие от компьютера или операционные системы функции, сохраняя общую совместимость с языками C и C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- Директива pragma HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068998"
---
# <a name="pragma-directive"></a><span data-ttu-id="5d71f-104">\#Директива pragma</span><span class="sxs-lookup"><span data-stu-id="5d71f-104">\#pragma Directive</span></span>

<span data-ttu-id="5d71f-105">Директива препроцессора, которая предоставляет зависящие от компьютера или операционные системы функции, сохраняя общую совместимость с языками C и C++.</span><span class="sxs-lookup"><span data-stu-id="5d71f-105">Preprocessor directive that provides machine-specific or operating system-specific features while retaining overall compatibility with the C and C++ languages.</span></span>



| <span data-ttu-id="5d71f-106">\#*строка маркера* pragma</span><span class="sxs-lookup"><span data-stu-id="5d71f-106">\#pragma *token-string*</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="5d71f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d71f-107">Parameters</span></span>



| <span data-ttu-id="5d71f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="5d71f-108">Item</span></span>                                                                                    | <span data-ttu-id="5d71f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5d71f-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d71f-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*Строка токена*</span><span class="sxs-lookup"><span data-stu-id="5d71f-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="5d71f-111">Последовательность символов, которая предоставляет определенную инструкцию и аргументы компилятора.</span><span class="sxs-lookup"><span data-stu-id="5d71f-111">Series of characters that gives a specific compiler instruction and arguments.</span></span> <span data-ttu-id="5d71f-112">Этот параметр подлежит раскрытию макросов.</span><span class="sxs-lookup"><span data-stu-id="5d71f-112">This parameter is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d71f-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d71f-113">Remarks</span></span>

<span data-ttu-id="5d71f-114">Если компилятор обнаруживает прагма-директиву, которая не распознается, она выдает предупреждение, но компиляция будет продолжена.</span><span class="sxs-lookup"><span data-stu-id="5d71f-114">If the compiler finds a pragma it does not recognize, it issues a warning, but compilation continues.</span></span>

<span data-ttu-id="5d71f-115">Компилятор HLSL распознает следующие директивы pragma:</span><span class="sxs-lookup"><span data-stu-id="5d71f-115">The HLSL compiler recognizes the following pragmas:</span></span>

-   [<span data-ttu-id="5d71f-116">DEF</span><span class="sxs-lookup"><span data-stu-id="5d71f-116">def</span></span>](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [<span data-ttu-id="5d71f-117">message</span><span class="sxs-lookup"><span data-stu-id="5d71f-117">message</span></span>](message-pragma-directive--directx-hlsl-.md)
-   [<span data-ttu-id="5d71f-118">\_Матрица Pack</span><span class="sxs-lookup"><span data-stu-id="5d71f-118">pack\_matrix</span></span>](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [<span data-ttu-id="5d71f-119">warning</span><span class="sxs-lookup"><span data-stu-id="5d71f-119">warning</span></span>](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a><span data-ttu-id="5d71f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="5d71f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d71f-121">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d71f-121">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





