---
description: Параметры, применяемые по умолчанию.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: Структура D3DXEFFECTDEFAULT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694160"
---
# <a name="d3dxeffectdefault-structure"></a><span data-ttu-id="8bf0f-103">Структура D3DXEFFECTDEFAULT</span><span class="sxs-lookup"><span data-stu-id="8bf0f-103">D3DXEFFECTDEFAULT structure</span></span>

<span data-ttu-id="8bf0f-104">Параметры, применяемые по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8bf0f-104">Effect default parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf0f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bf0f-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a><span data-ttu-id="8bf0f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="8bf0f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8bf0f-107">**ппарамнаме**</span><span class="sxs-lookup"><span data-stu-id="8bf0f-107">**pParamName**</span></span>
</dt> <dd>

<span data-ttu-id="8bf0f-108">Тип: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="8bf0f-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="8bf0f-109">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="8bf0f-109">Parameter name.</span></span>

</dd> <dt>

<span data-ttu-id="8bf0f-110">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8bf0f-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="8bf0f-111">Тип: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span><span class="sxs-lookup"><span data-stu-id="8bf0f-111">Type: **[**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8bf0f-112">Тип данных в pValue.</span><span class="sxs-lookup"><span data-stu-id="8bf0f-112">Data type in pValue.</span></span> <span data-ttu-id="8bf0f-113">Дополнительные сведения см. в разделе [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span><span class="sxs-lookup"><span data-stu-id="8bf0f-113">For more information, see [**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span></span>

</dd> <dt>

<span data-ttu-id="8bf0f-114">**нумбитес**</span><span class="sxs-lookup"><span data-stu-id="8bf0f-114">**NumBytes**</span></span>
</dt> <dd>

<span data-ttu-id="8bf0f-115">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8bf0f-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8bf0f-116">Размер (в байтах) данных, на которые указывает pValue.</span><span class="sxs-lookup"><span data-stu-id="8bf0f-116">Size, in bytes, of the data pointed to by pValue.</span></span>

</dd> <dt>

<span data-ttu-id="8bf0f-117">**pValue**</span><span class="sxs-lookup"><span data-stu-id="8bf0f-117">**pValue**</span></span>
</dt> <dd>

<span data-ttu-id="8bf0f-118">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8bf0f-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8bf0f-119">Указатель на место в памяти, содержащее данные.</span><span class="sxs-lookup"><span data-stu-id="8bf0f-119">Pointer to the memory location that contains the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bf0f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8bf0f-120">Requirements</span></span>



| <span data-ttu-id="8bf0f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8bf0f-121">Requirement</span></span> | <span data-ttu-id="8bf0f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf0f-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf0f-123">Header</span><span class="sxs-lookup"><span data-stu-id="8bf0f-123">Header</span></span><br/> | <dl> <span data-ttu-id="8bf0f-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf0f-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf0f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bf0f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf0f-126">Структуры эффектов</span><span class="sxs-lookup"><span data-stu-id="8bf0f-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
