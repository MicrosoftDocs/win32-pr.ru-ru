---
description: Определяет данные памяти. Не рекомендуется.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Структура ДКСФИЛЕЛОАДМЕМОРИ (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703880"
---
# <a name="dxfileloadmemory-structure"></a><span data-ttu-id="ef11d-104">Структура ДКСФИЛЕЛОАДМЕМОРИ</span><span class="sxs-lookup"><span data-stu-id="ef11d-104">DXFILELOADMEMORY structure</span></span>

<span data-ttu-id="ef11d-105">Определяет данные памяти.</span><span class="sxs-lookup"><span data-stu-id="ef11d-105">Identifies memory data.</span></span> <span data-ttu-id="ef11d-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ef11d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef11d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef11d-107">Syntax</span></span>


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="ef11d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ef11d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef11d-109">**лпмемори**</span><span class="sxs-lookup"><span data-stu-id="ef11d-109">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="ef11d-110">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef11d-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef11d-111">Указатель на блок памяти для загрузки.</span><span class="sxs-lookup"><span data-stu-id="ef11d-111">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="ef11d-112">**дсизе**</span><span class="sxs-lookup"><span data-stu-id="ef11d-112">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="ef11d-113">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef11d-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef11d-114">Размер блока памяти, который должен быть загружен, в байтах.</span><span class="sxs-lookup"><span data-stu-id="ef11d-114">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef11d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef11d-115">Remarks</span></span>

<span data-ttu-id="ef11d-116">Эта структура определяет ресурс для загрузки, когда приложение использует метод [**креатинумобжект**](idirectxfile--createenumobject.md) и указывает дксфилелоад \_ фроммемори.</span><span class="sxs-lookup"><span data-stu-id="ef11d-116">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef11d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ef11d-117">Requirements</span></span>



| <span data-ttu-id="ef11d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ef11d-118">Requirement</span></span> | <span data-ttu-id="ef11d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ef11d-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ef11d-120">Header</span><span class="sxs-lookup"><span data-stu-id="ef11d-120">Header</span></span><br/> | <dl> <span data-ttu-id="ef11d-121"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef11d-121"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef11d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef11d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef11d-123">Структуры файлов X</span><span class="sxs-lookup"><span data-stu-id="ef11d-123">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="ef11d-124">**креатинумобжект**</span><span class="sxs-lookup"><span data-stu-id="ef11d-124">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="ef11d-125">Константы ДКСФИЛЕ</span><span class="sxs-lookup"><span data-stu-id="ef11d-125">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
