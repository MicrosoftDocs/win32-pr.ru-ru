---
description: Интерфейс ID3DXEffectCompiler компилирует результат из функции или шейдера вершин.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Интерфейс ID3DXEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354343"
---
# <a name="id3dxeffectcompiler-interface"></a><span data-ttu-id="ee2b4-103">Интерфейс ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="ee2b4-103">ID3DXEffectCompiler interface</span></span>

<span data-ttu-id="ee2b4-104">Интерфейс **ID3DXEffectCompiler** компилирует результат из функции или шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="ee2b4-104">The **ID3DXEffectCompiler** interface compiles an effect from a function or from a vertex shader.</span></span>

## <a name="members"></a><span data-ttu-id="ee2b4-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="ee2b4-105">Members</span></span>

<span data-ttu-id="ee2b4-106">Интерфейс **ID3DXEffectCompiler** наследует от [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="ee2b4-106">The **ID3DXEffectCompiler** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="ee2b4-107">**ID3DXEffectCompiler** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ee2b4-107">**ID3DXEffectCompiler** also has these types of members:</span></span>

-   [<span data-ttu-id="ee2b4-108">Методы</span><span class="sxs-lookup"><span data-stu-id="ee2b4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ee2b4-109">Методы</span><span class="sxs-lookup"><span data-stu-id="ee2b4-109">Methods</span></span>

<span data-ttu-id="ee2b4-110">Интерфейс **ID3DXEffectCompiler** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ee2b4-110">The **ID3DXEffectCompiler** interface has these methods.</span></span>



| <span data-ttu-id="ee2b4-111">Метод</span><span class="sxs-lookup"><span data-stu-id="ee2b4-111">Method</span></span>                                                      | <span data-ttu-id="ee2b4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ee2b4-112">Description</span></span>                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee2b4-113">**компилиффект**</span><span class="sxs-lookup"><span data-stu-id="ee2b4-113">**CompileEffect**</span></span>](id3dxeffectcompiler--compileeffect.md) | <span data-ttu-id="ee2b4-114">Компиляция результата.</span><span class="sxs-lookup"><span data-stu-id="ee2b4-114">Compile an effect.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="ee2b4-115">**компилешадер**</span><span class="sxs-lookup"><span data-stu-id="ee2b4-115">**CompileShader**</span></span>](id3dxeffectcompiler--compileshader.md) | <span data-ttu-id="ee2b4-116">Компилирует шейдер из действия, содержащего одну или несколько функций.</span><span class="sxs-lookup"><span data-stu-id="ee2b4-116">Compiles a shader from an effect that contains one or more functions.</span></span><br/>                                                            |
| [<span data-ttu-id="ee2b4-117">**Знак ". Literal"**</span><span class="sxs-lookup"><span data-stu-id="ee2b4-117">**GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)       | <span data-ttu-id="ee2b4-118">Возвращает состояние литерала параметра.</span><span class="sxs-lookup"><span data-stu-id="ee2b4-118">Gets a literal status of a parameter.</span></span> <span data-ttu-id="ee2b4-119">Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.</span><span class="sxs-lookup"><span data-stu-id="ee2b4-119">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/>      |
| [<span data-ttu-id="ee2b4-120">**сетлитерал**</span><span class="sxs-lookup"><span data-stu-id="ee2b4-120">**SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)       | <span data-ttu-id="ee2b4-121">Переключает состояние литерала для параметра.</span><span class="sxs-lookup"><span data-stu-id="ee2b4-121">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="ee2b4-122">Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.</span><span class="sxs-lookup"><span data-stu-id="ee2b4-122">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee2b4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee2b4-123">Remarks</span></span>

<span data-ttu-id="ee2b4-124">Интерфейс ID3DXEffectCompiler получается путем вызова [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)или [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span><span class="sxs-lookup"><span data-stu-id="ee2b4-124">The ID3DXEffectCompiler interface is obtained by calling [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md), or [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span></span>

<span data-ttu-id="ee2b4-125">Тип LPD3DXEFFECTCOMPILER определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ee2b4-125">The LPD3DXEFFECTCOMPILER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a><span data-ttu-id="ee2b4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ee2b4-126">Requirements</span></span>



| <span data-ttu-id="ee2b4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ee2b4-127">Requirement</span></span> | <span data-ttu-id="ee2b4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ee2b4-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee2b4-129">Header</span><span class="sxs-lookup"><span data-stu-id="ee2b4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ee2b4-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee2b4-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ee2b4-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee2b4-131">Library</span></span><br/> | <dl> <span data-ttu-id="ee2b4-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee2b4-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ee2b4-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee2b4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee2b4-134">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="ee2b4-134">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ee2b4-135">Интерфейсы эффектов</span><span class="sxs-lookup"><span data-stu-id="ee2b4-135">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ee2b4-136">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="ee2b4-136">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="ee2b4-137">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="ee2b4-137">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="ee2b4-138">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="ee2b4-138">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




