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
ms.openlocfilehash: c4cb8f6fd15db857daa3005c99381d437a5289f6
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129651"
---
# <a name="data-types-hlsl"></a><span data-ttu-id="c1a41-104">Типы данных (HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1a41-104">Data Types (HLSL)</span></span>

<span data-ttu-id="c1a41-105">HLSL поддерживает множество различных встроенных типов данных.</span><span class="sxs-lookup"><span data-stu-id="c1a41-105">HLSL supports many different intrinsic data types.</span></span> <span data-ttu-id="c1a41-106">В этой таблице показано, какие типы следует использовать для определения переменных шейдера.</span><span class="sxs-lookup"><span data-stu-id="c1a41-106">This table shows which types to use to define shader variables.</span></span>



| <span data-ttu-id="c1a41-107">Использовать этот встроенный тип</span><span class="sxs-lookup"><span data-stu-id="c1a41-107">Use this intrinsic type</span></span>                                                                                                                         | <span data-ttu-id="c1a41-108">Определение переменной шейдера</span><span class="sxs-lookup"><span data-stu-id="c1a41-108">To define this shader variable</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="c1a41-109">скалярная</span><span class="sxs-lookup"><span data-stu-id="c1a41-109">Scalar</span></span>](dx-graphics-hlsl-scalar.md)                                                                                   | <span data-ttu-id="c1a41-110">Скаляр в одном компоненте</span><span class="sxs-lookup"><span data-stu-id="c1a41-110">One-component scalar</span></span>                       |
| <span data-ttu-id="c1a41-111">[Вектор](dx-graphics-hlsl-vector.md), [Матрица](dx-graphics-hlsl-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="c1a41-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span></span>                                            | <span data-ttu-id="c1a41-112">Вектор или матрица с несколькими компонентами</span><span class="sxs-lookup"><span data-stu-id="c1a41-112">Multiple-component vector or matrix</span></span>        |
| <span data-ttu-id="c1a41-113">[Образец](dx-graphics-hlsl-sampler.md), [текстура](dx-graphics-hlsl-texture.md) или [буфер](dx-graphics-hlsl-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="c1a41-113">[Sampler](dx-graphics-hlsl-sampler.md), [Texture](dx-graphics-hlsl-texture.md) or [Buffer](dx-graphics-hlsl-buffer.md)</span></span>   | <span data-ttu-id="c1a41-114">Образец, текстура или объект buffer</span><span class="sxs-lookup"><span data-stu-id="c1a41-114">Sampler, texture, or buffer object</span></span>         |
| <span data-ttu-id="c1a41-115">[Структура](dx-graphics-hlsl-struct.md), [определяемая пользователем](dx-graphics-hlsl-user-defined.md)</span><span class="sxs-lookup"><span data-stu-id="c1a41-115">[Struct](dx-graphics-hlsl-struct.md), [User Defined](dx-graphics-hlsl-user-defined.md)</span></span>                                | <span data-ttu-id="c1a41-116">Пользовательская структура или typedef</span><span class="sxs-lookup"><span data-stu-id="c1a41-116">Custom structure or typedef</span></span>                |
| <span data-ttu-id="c1a41-117">Array</span><span class="sxs-lookup"><span data-stu-id="c1a41-117">Array</span></span>                                                                                   | <span data-ttu-id="c1a41-118">Объявленные литеральные скалярные выражения, содержащие большинство других типов</span><span class="sxs-lookup"><span data-stu-id="c1a41-118">Literal scalar expressions declared containing most other types</span></span>                       |
| [<span data-ttu-id="c1a41-119">Объект State</span><span class="sxs-lookup"><span data-stu-id="c1a41-119">State Object</span></span>](dx-graphics-hlsl-state-object.md) | <span data-ttu-id="c1a41-120">HLSL представления объектов состояния</span><span class="sxs-lookup"><span data-stu-id="c1a41-120">HLSL representations of state objects</span></span> |


 

<span data-ttu-id="c1a41-121">Чтобы лучше понять, как использовать векторы и матрицы в HLSL, вам может потребоваться ознакомиться с этой информацией о том, как HLSL использует математические функции [для каждого компонента](dx-graphics-hlsl-per-component-math.md) .</span><span class="sxs-lookup"><span data-stu-id="c1a41-121">To help you better understand how to use vectors and matrices in HLSL, you may want to read this background information on how HLSL uses [per-component](dx-graphics-hlsl-per-component-math.md) math.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1a41-122">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c1a41-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1a41-123">Переменные (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1a41-123">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 




