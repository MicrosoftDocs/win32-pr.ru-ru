---
description: Статистика ресурсов, собираемая \_ RESOURCEMANAGER D3DDEVINFO при использовании механизма асинхронных запросов.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: Структура D3DRESOURCESTATS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713538"
---
# <a name="d3dresourcestats-structure"></a><span data-ttu-id="d7b48-103">Структура D3DRESOURCESTATS</span><span class="sxs-lookup"><span data-stu-id="d7b48-103">D3DRESOURCESTATS structure</span></span>

<span data-ttu-id="d7b48-104">Статистика ресурсов, собираемая [**\_ ResourceManager D3DDEVINFO**](d3ddevinfo-resourcemanager.md) при использовании механизма асинхронных запросов.</span><span class="sxs-lookup"><span data-stu-id="d7b48-104">Resource statistics gathered by the [**D3DDEVINFO\_ResourceManager**](d3ddevinfo-resourcemanager.md) when using the asynchronous query mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b48-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7b48-105">Syntax</span></span>


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a><span data-ttu-id="d7b48-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d7b48-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7b48-107">**бсрашинг**</span><span class="sxs-lookup"><span data-stu-id="d7b48-107">**bThrashing**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-108">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-109">Указывает, происходит ли пробуксовка.</span><span class="sxs-lookup"><span data-stu-id="d7b48-109">Indicates if thrashing is occurring.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-110">**аппроксбитесдовнлоадед**</span><span class="sxs-lookup"><span data-stu-id="d7b48-110">**ApproxBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-112">Приблизительное число байтов, скачанных диспетчером ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7b48-112">Approximate number of bytes downloaded by the resource manager.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-113">**нумевиктс**</span><span class="sxs-lookup"><span data-stu-id="d7b48-113">**NumEvicts**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-115">Число исключенных объектов.</span><span class="sxs-lookup"><span data-stu-id="d7b48-115">Number of objects evicted.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-116">**нумвидкреатес**</span><span class="sxs-lookup"><span data-stu-id="d7b48-116">**NumVidCreates**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-118">Количество объектов, созданных в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="d7b48-118">Number of objects created in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-119">**ластпри**</span><span class="sxs-lookup"><span data-stu-id="d7b48-119">**LastPri**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-120">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-121">Приоритет последнего исключенного объекта.</span><span class="sxs-lookup"><span data-stu-id="d7b48-121">Priority of last object evicted.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-122">**нумусед**</span><span class="sxs-lookup"><span data-stu-id="d7b48-122">**NumUsed**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-124">Число объектов, заданное для устройства.</span><span class="sxs-lookup"><span data-stu-id="d7b48-124">Number of objects set to the device.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-125">**нумусединвидмем**</span><span class="sxs-lookup"><span data-stu-id="d7b48-125">**NumUsedInVidMem**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-126">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-127">Число объектов, заданных на устройстве, которые уже находятся в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="d7b48-127">Number of objects set to the device, which are already in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-128">**WorkingSet**</span><span class="sxs-lookup"><span data-stu-id="d7b48-128">**WorkingSet**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-129">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-129">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-130">Количество объектов в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="d7b48-130">Number of objects in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-131">**воркингсетбитес**</span><span class="sxs-lookup"><span data-stu-id="d7b48-131">**WorkingSetBytes**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-132">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-133">Число байтов в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="d7b48-133">Number of bytes in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-134">**тоталманажед**</span><span class="sxs-lookup"><span data-stu-id="d7b48-134">**TotalManaged**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-135">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-135">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-136">Общее число управляемых объектов.</span><span class="sxs-lookup"><span data-stu-id="d7b48-136">Total number of managed objects.</span></span>

</dd> <dt>

<span data-ttu-id="d7b48-137">**TotalBytes**</span><span class="sxs-lookup"><span data-stu-id="d7b48-137">**TotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="d7b48-138">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7b48-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7b48-139">Общее число байтов управляемых объектов.</span><span class="sxs-lookup"><span data-stu-id="d7b48-139">Total number of bytes of managed objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7b48-140">Требования</span><span class="sxs-lookup"><span data-stu-id="d7b48-140">Requirements</span></span>



| <span data-ttu-id="d7b48-141">Требование</span><span class="sxs-lookup"><span data-stu-id="d7b48-141">Requirement</span></span> | <span data-ttu-id="d7b48-142">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b48-142">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b48-143">Header</span><span class="sxs-lookup"><span data-stu-id="d7b48-143">Header</span></span><br/> | <dl> <span data-ttu-id="d7b48-144"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7b48-144"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7b48-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7b48-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b48-146">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="d7b48-146">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d7b48-147">Асинхронное уведомление (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d7b48-147">Asynchronous Notification (Direct3D 9)</span></span>](asynchronous-notification.md)
</dt> </dl>

 

 
