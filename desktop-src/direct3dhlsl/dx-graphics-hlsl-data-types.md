---
title: Типы данных (HLSL)
description: HLSL поддерживает множество различных встроенных типов данных. В этой таблице показано, какие типы следует использовать для определения переменных шейдера.
ms.assetid: e4b7738d-e865-4151-a204-0a5b88a913b3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cee02e38180b903b235c32ebc2c7ca486777b20
ms.sourcegitcommit: 316ce582d9b972634a0521e0380e054e9cbb5bae
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "104997982"
---
# <a name="data-types-hlsl"></a><span data-ttu-id="e4ef4-104">Типы данных (HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4ef4-104">Data Types (HLSL)</span></span>

<span data-ttu-id="e4ef4-105">HLSL поддерживает множество различных встроенных типов данных.</span><span class="sxs-lookup"><span data-stu-id="e4ef4-105">HLSL supports many different intrinsic data types.</span></span> <span data-ttu-id="e4ef4-106">В этой таблице показано, какие типы следует использовать для определения переменных шейдера.</span><span class="sxs-lookup"><span data-stu-id="e4ef4-106">This table shows which types to use to define shader variables.</span></span>



|                                                                                                                         |                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="e4ef4-107">Использовать этот встроенный тип</span><span class="sxs-lookup"><span data-stu-id="e4ef4-107">Use This Intrinsic Type</span></span>                                                                                                 | <span data-ttu-id="e4ef4-108">Определение переменной шейдера</span><span class="sxs-lookup"><span data-stu-id="e4ef4-108">To Define This Shader Variable</span></span>             |
| [<span data-ttu-id="e4ef4-109">Функцией</span><span class="sxs-lookup"><span data-stu-id="e4ef4-109">Scalar</span></span>](dx-graphics-hlsl-scalar.md)                                                                                   | <span data-ttu-id="e4ef4-110">Скаляр в одном компоненте</span><span class="sxs-lookup"><span data-stu-id="e4ef4-110">One-component scalar</span></span>                       |
| <span data-ttu-id="e4ef4-111">[Вектор](dx-graphics-hlsl-vector.md), [Матрица](dx-graphics-hlsl-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="e4ef4-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span></span>                                            | <span data-ttu-id="e4ef4-112">Вектор или матрица с несколькими компонентами</span><span class="sxs-lookup"><span data-stu-id="e4ef4-112">Multiple-component vector or matrix</span></span>        |
| <span data-ttu-id="e4ef4-113">[Образец](dx-graphics-hlsl-sampler.md), [текстура](dx-graphics-hlsl-texture.md) или [буфер](dx-graphics-hlsl-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="e4ef4-113">[Sampler](dx-graphics-hlsl-sampler.md), [Texture](dx-graphics-hlsl-texture.md) or [Buffer](dx-graphics-hlsl-buffer.md)</span></span>   | <span data-ttu-id="e4ef4-114">Образец, текстура или объект buffer</span><span class="sxs-lookup"><span data-stu-id="e4ef4-114">Sampler, texture, or buffer object</span></span>         |
| <span data-ttu-id="e4ef4-115">[Структура](dx-graphics-hlsl-struct.md), [определяемая пользователем](dx-graphics-hlsl-user-defined.md)</span><span class="sxs-lookup"><span data-stu-id="e4ef4-115">[Struct](dx-graphics-hlsl-struct.md), [User Defined](dx-graphics-hlsl-user-defined.md)</span></span>                                | <span data-ttu-id="e4ef4-116">Пользовательская структура или typedef</span><span class="sxs-lookup"><span data-stu-id="e4ef4-116">Custom structure or typedef</span></span>                |
| <span data-ttu-id="e4ef4-117">Array</span><span class="sxs-lookup"><span data-stu-id="e4ef4-117">Array</span></span>                                                                                   | <span data-ttu-id="e4ef4-118">Объявленные литеральные скалярные выражения, содержащие большинство других типов</span><span class="sxs-lookup"><span data-stu-id="e4ef4-118">Literal scalar expressions declared containing most other types</span></span>                       |
| [<span data-ttu-id="e4ef4-119">Объект State</span><span class="sxs-lookup"><span data-stu-id="e4ef4-119">State Object</span></span>](dx-graphics-hlsl-state-object.md) | <span data-ttu-id="e4ef4-120">HLSL представления объектов состояния</span><span class="sxs-lookup"><span data-stu-id="e4ef4-120">HLSL representations of state objects</span></span> |


 

<span data-ttu-id="e4ef4-121">Чтобы лучше понять, как использовать векторы и матрицы в HLSL, вам может потребоваться ознакомиться с этой информацией о том, как HLSL использует математические функции [для каждого компонента](dx-graphics-hlsl-per-component-math.md) .</span><span class="sxs-lookup"><span data-stu-id="e4ef4-121">To help you better understand how to use vectors and matrices in HLSL, you may want to read this background information on how HLSL uses [per-component](dx-graphics-hlsl-per-component-math.md) math.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4ef4-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e4ef4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4ef4-123">Переменные (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4ef4-123">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 




