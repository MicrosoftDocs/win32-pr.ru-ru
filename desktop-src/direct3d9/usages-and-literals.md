---
description: Использование аналогично области действия параметра, так как оно определяет область, в которой параметр является допустимым.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Использование и литералы (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710674"
---
# <a name="usages-and-literals-direct3d-9"></a><span data-ttu-id="ea1d1-103">Использование и литералы (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ea1d1-103">Usages and Literals (Direct3D 9)</span></span>

<span data-ttu-id="ea1d1-104">Использование аналогично области действия параметра, так как оно определяет область, в которой параметр является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-104">Usage is similar to a parameter's scope, because it defines the scope in which the parameter is valid.</span></span>



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1d1-105">Значение</span><span class="sxs-lookup"><span data-stu-id="ea1d1-105">Value</span></span>  | <span data-ttu-id="ea1d1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ea1d1-106">Description</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ea1d1-107">const</span><span class="sxs-lookup"><span data-stu-id="ea1d1-107">const</span></span>  | <span data-ttu-id="ea1d1-108">Параметр будет постоянным в области всех функций.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-108">The parameter will be constant within the scope of all functions.</span></span> <span data-ttu-id="ea1d1-109">(Обратите внимание, что такие параметры по-прежнему можно записать с помощью [**ID3DXEffect**](id3dxeffect.md) или [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), так как это происходит вне области действия всех функций.)</span><span class="sxs-lookup"><span data-stu-id="ea1d1-109">(Note that such parameters can still be written to with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), because this occurs outside the scope of all functions.)</span></span> |
| <span data-ttu-id="ea1d1-110">общие</span><span class="sxs-lookup"><span data-stu-id="ea1d1-110">shared</span></span> | <span data-ttu-id="ea1d1-111">Параметр будет совместно использоваться в пуле эффектов.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-111">The parameter will be shared in the effect pool.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="ea1d1-112">static</span><span class="sxs-lookup"><span data-stu-id="ea1d1-112">static</span></span> | <span data-ttu-id="ea1d1-113">Параметр будет невидимым для приложения, то есть к нему нельзя получить доступ из [**ID3DXEffect**](id3dxeffect.md) или [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="ea1d1-113">The parameter will be invisible to the application, that is, you cannot access them from [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>                                                                                                  |



 

<span data-ttu-id="ea1d1-114">Пометка параметра как литерала означает, что его значение никогда не изменится.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-114">Marking a parameter as literal indicates that its value will never change.</span></span> <span data-ttu-id="ea1d1-115">Это позволяет компилятору влияния выполнить дополнительные оптимизации.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-115">This enables the effect compiler to do extra optimization.</span></span>

<span data-ttu-id="ea1d1-116">Только необщие параметры верхнего уровня могут быть помечены как литералы.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-116">Only non-shared top-level parameters can be marked as literal.</span></span> <span data-ttu-id="ea1d1-117">Параметры могут быть помечены только как литерал с помощью [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="ea1d1-117">Parameters can only be marked as literal with [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span> <span data-ttu-id="ea1d1-118">Литеральные значения не могут быть заданы с помощью [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="ea1d1-118">Literal values cannot be set with [**ID3DXEffect**](id3dxeffect.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea1d1-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ea1d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea1d1-120">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="ea1d1-120">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



