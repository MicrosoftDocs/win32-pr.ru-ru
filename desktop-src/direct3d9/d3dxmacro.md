---
description: Описывает определения препроцессора, используемые объектом Effect.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: Структура D3DXMACRO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703916"
---
# <a name="d3dxmacro-structure"></a><span data-ttu-id="34898-103">Структура D3DXMACRO</span><span class="sxs-lookup"><span data-stu-id="34898-103">D3DXMACRO structure</span></span>

<span data-ttu-id="34898-104">Описывает определения препроцессора, используемые объектом Effect.</span><span class="sxs-lookup"><span data-stu-id="34898-104">Describes preprocessor definitions used by an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="34898-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34898-105">Syntax</span></span>


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a><span data-ttu-id="34898-106">Члены</span><span class="sxs-lookup"><span data-stu-id="34898-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="34898-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="34898-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="34898-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34898-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34898-109">Имя препроцессора.</span><span class="sxs-lookup"><span data-stu-id="34898-109">Preprocessor name.</span></span>

</dd> <dt>

<span data-ttu-id="34898-110">**Определение**</span><span class="sxs-lookup"><span data-stu-id="34898-110">**Definition**</span></span>
</dt> <dd>

<span data-ttu-id="34898-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34898-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34898-112">Имя определения.</span><span class="sxs-lookup"><span data-stu-id="34898-112">Definition name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34898-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34898-113">Remarks</span></span>

<span data-ttu-id="34898-114">Чтобы использовать **D3DXMACRO** s в нескольких строках, перед каждым символом новой строки следует ставить обратную косую черту (как \# определено на языке C).</span><span class="sxs-lookup"><span data-stu-id="34898-114">To use **D3DXMACRO** s in more than one line, prefix each new line character with a backslash (like a \#define in the C language).</span></span> <span data-ttu-id="34898-115">Пример:</span><span class="sxs-lookup"><span data-stu-id="34898-115">For example:</span></span>


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



<span data-ttu-id="34898-116">Обратите внимание на три символа обратной косой черты в конце строки.</span><span class="sxs-lookup"><span data-stu-id="34898-116">Notice the 3 backslash characters at the end of the line.</span></span> <span data-ttu-id="34898-117">Первые два необходимы для вывода одного \\ символа "", за которым следует символ новой строки " \\ n".</span><span class="sxs-lookup"><span data-stu-id="34898-117">The first two are required to output a single '\\', followed by the newline character "\\n".</span></span> <span data-ttu-id="34898-118">При необходимости можно также завершить строки, используя " \\ \\ \\ r \\ n".</span><span class="sxs-lookup"><span data-stu-id="34898-118">Optionally, you may also want to terminate your lines using "\\\\\\r\\n".</span></span>

## <a name="requirements"></a><span data-ttu-id="34898-119">Требования</span><span class="sxs-lookup"><span data-stu-id="34898-119">Requirements</span></span>



| <span data-ttu-id="34898-120">Требование</span><span class="sxs-lookup"><span data-stu-id="34898-120">Requirement</span></span> | <span data-ttu-id="34898-121">Значение</span><span class="sxs-lookup"><span data-stu-id="34898-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="34898-122">Header</span><span class="sxs-lookup"><span data-stu-id="34898-122">Header</span></span><br/> | <dl> <span data-ttu-id="34898-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="34898-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34898-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34898-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34898-125">Структуры эффектов</span><span class="sxs-lookup"><span data-stu-id="34898-125">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="34898-126">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="34898-126">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
