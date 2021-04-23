---
description: Определяет данные памяти.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: Структура D3DXF_FILELOADMEMORY (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000364"
---
# <a name="d3dxf_fileloadmemory-structure"></a><span data-ttu-id="36ec5-103">\_Структура ФИЛЕЛОАДМЕМОРИ D3DXF</span><span class="sxs-lookup"><span data-stu-id="36ec5-103">D3DXF\_FILELOADMEMORY structure</span></span>

<span data-ttu-id="36ec5-104">Определяет данные памяти.</span><span class="sxs-lookup"><span data-stu-id="36ec5-104">Identifies memory data.</span></span>

## <a name="syntax"></a><span data-ttu-id="36ec5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36ec5-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="36ec5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="36ec5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="36ec5-107">**лпмемори**</span><span class="sxs-lookup"><span data-stu-id="36ec5-107">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="36ec5-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36ec5-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="36ec5-109">Указатель на блок памяти для загрузки.</span><span class="sxs-lookup"><span data-stu-id="36ec5-109">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="36ec5-110">**дсизе**</span><span class="sxs-lookup"><span data-stu-id="36ec5-110">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="36ec5-111">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36ec5-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="36ec5-112">Размер блока памяти, который должен быть загружен, в байтах.</span><span class="sxs-lookup"><span data-stu-id="36ec5-112">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36ec5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36ec5-113">Remarks</span></span>

<span data-ttu-id="36ec5-114">Эта структура определяет данные, загружаемые из памяти, когда приложение использует метод [**креатинумобжект**](id3dxfile--createenumobject.md) и ЗАДАЕТ \_ флаг D3DXF филелоад \_ фроммемори.</span><span class="sxs-lookup"><span data-stu-id="36ec5-114">This structure identifies data to be loaded from memory when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the D3DXF\_FILELOAD\_FROMMEMORY flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ec5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="36ec5-115">Requirements</span></span>



| <span data-ttu-id="36ec5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="36ec5-116">Requirement</span></span> | <span data-ttu-id="36ec5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="36ec5-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36ec5-118">Header</span><span class="sxs-lookup"><span data-stu-id="36ec5-118">Header</span></span><br/> | <dl> <span data-ttu-id="36ec5-119"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="36ec5-119"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36ec5-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36ec5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36ec5-121">Структуры файлов D3DX X</span><span class="sxs-lookup"><span data-stu-id="36ec5-121">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
