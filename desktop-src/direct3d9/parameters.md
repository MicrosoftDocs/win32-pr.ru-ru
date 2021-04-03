---
description: Параметры — это переменные эффектов.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Параметры (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140707"
---
# <a name="parameters-direct3d-9"></a><span data-ttu-id="6ecd2-103">Параметры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6ecd2-103">Parameters (Direct3D 9)</span></span>

<span data-ttu-id="6ecd2-104">Параметры — это переменные эффектов.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-104">Parameters are effect variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ecd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ecd2-105">Syntax</span></span>

<span data-ttu-id="6ecd2-106">*идентификатор типа использования* \[ : *выражение семантических* \] \[ < *заметок* > \] \[ =   \] ;</span><span class="sxs-lookup"><span data-stu-id="6ecd2-106">*usage type ID* \[: *semantic*\] \[<*annotation(s)*>\] \[= *expression*\];</span></span>

<span data-ttu-id="6ecd2-107">Параметры можно считывать из приложения и записывать в него с помощью [**ID3DXEffect**](id3dxeffect.md) или [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="6ecd2-107">Parameters can be read from and written to by the application with [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>

<span data-ttu-id="6ecd2-108">На параметры можно ссылаться в функциях и в методах (в частности, в правой части назначений состояний).</span><span class="sxs-lookup"><span data-stu-id="6ecd2-108">Parameters can be referenced in functions and in techniques (specifically, in the right side of state assignments).</span></span>



| <span data-ttu-id="6ecd2-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="6ecd2-109">Item</span></span>                                                                                 | <span data-ttu-id="6ecd2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6ecd2-110">Description</span></span>                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ecd2-111"><span id="usage"></span><span id="USAGE"></span>*Загрузка*</span><span class="sxs-lookup"><span data-stu-id="6ecd2-111"><span id="usage"></span><span id="USAGE"></span>*usage*</span></span><br/>                   | <span data-ttu-id="6ecd2-112">Область действия параметра.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-112">Scope of the parameter.</span></span> <span data-ttu-id="6ecd2-113">См. раздел [использование и литералы (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="6ecd2-113">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span><br/>                                                             |
| <span data-ttu-id="6ecd2-114"><span id="type"></span><span id="TYPE"></span>*Тип*</span><span class="sxs-lookup"><span data-stu-id="6ecd2-114"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                      | <span data-ttu-id="6ecd2-115">Любая допустимая [ссылка для типа HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6ecd2-115">Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span><br/>                                                                        |
| <span data-ttu-id="6ecd2-116"><span id="ID"></span><span id="id"></span>*УДОСТОВЕРЕНИЯ*</span><span class="sxs-lookup"><span data-stu-id="6ecd2-116"><span id="ID"></span><span id="id"></span>*ID*</span></span><br/>                            | <span data-ttu-id="6ecd2-117">Уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-117">A unique name.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="6ecd2-118"><span id="semantic"></span><span id="SEMANTIC"></span>*семантическ*</span><span class="sxs-lookup"><span data-stu-id="6ecd2-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semantic*</span></span><br/>          | <span data-ttu-id="6ecd2-119">Тег, следующий за правилами идентификаторов, который обычно указывает на использование параметра.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-119">A tag following identifier rules that typically indicates the usage of the parameter.</span></span> <span data-ttu-id="6ecd2-120">Должен быть определенным типом.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-120">Must be a particular type.</span></span><br/>                                     |
| <span data-ttu-id="6ecd2-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*Примечания*</span><span class="sxs-lookup"><span data-stu-id="6ecd2-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*annotations*</span></span><br/> | <span data-ttu-id="6ecd2-122">Ноль или более частей пользовательской информации.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-122">Zero or more pieces of user-specific information.</span></span> <span data-ttu-id="6ecd2-123">Может быть любым типом.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-123">May be any type.</span></span> <span data-ttu-id="6ecd2-124">См. раздел [Добавление сведений, чтобы параметры вступили в действие с заметками](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="6ecd2-124">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/> |
| <span data-ttu-id="6ecd2-125"><span id="expression"></span><span id="EXPRESSION"></span>*выражение*</span><span class="sxs-lookup"><span data-stu-id="6ecd2-125"><span id="expression"></span><span id="EXPRESSION"></span>*expression*</span></span><br/>    | <span data-ttu-id="6ecd2-126">Инициализирует значение параметра.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-126">Initializes the parameter's value.</span></span> <span data-ttu-id="6ecd2-127">См. раздел [выражения (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="6ecd2-127">See [Expressions (Direct3D 9)](expressions.md).</span></span><br/>                                                                  |



 

<span data-ttu-id="6ecd2-128">Параметры могут быть инициализированы любой допустимой [ссылкой](../direct3dhlsl/dx-graphics-hlsl-reference.md) на выражение HLSL, которое сокращается до литерального значения.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-128">Parameters can be initialized to any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) expression that reduces to a literal value.</span></span>

<span data-ttu-id="6ecd2-129">Значения параметров не изменяются при выполнении назначения состояния или вызовах функций.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-129">Parameter values are not changed by the execution of state assignment or function calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ecd2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6ecd2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ecd2-131">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="6ecd2-131">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
