---
description: Блокировка буфера индекса.
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: 'Метод ID3DXPatchMesh:: Локкиндексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81dc410262ff21ea972d4c501ac3b5d26a361642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548135"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a><span data-ttu-id="d0135-103">Метод ID3DXPatchMesh:: Локкиндексбуффер</span><span class="sxs-lookup"><span data-stu-id="d0135-103">ID3DXPatchMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="d0135-104">Блокировка буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="d0135-104">Lock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0135-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0135-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="d0135-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0135-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0135-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0135-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0135-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0135-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0135-109">Сочетание флагов блокировки (ноль или более), описывающих тип выполняемой блокировки.</span><span class="sxs-lookup"><span data-stu-id="d0135-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="d0135-110">Для этого метода допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d0135-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="d0135-111">D3DLOCK \_ отбросить</span><span class="sxs-lookup"><span data-stu-id="d0135-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="d0135-112">D3DLOCK \_ без \_ "грязного" \_ обновления</span><span class="sxs-lookup"><span data-stu-id="d0135-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="d0135-113">D3DLOCK \_ носислокк</span><span class="sxs-lookup"><span data-stu-id="d0135-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="d0135-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d0135-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="d0135-115">Описание флагов см. в разделе [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="d0135-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0135-116">*ппдата* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d0135-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d0135-117">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0135-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d0135-118">\*Указатель void на буфер памяти, содержащий возвращенные данные индекса.</span><span class="sxs-lookup"><span data-stu-id="d0135-118">VOID\* pointer to a memory buffer containing the returned index data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0135-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0135-119">Return value</span></span>

<span data-ttu-id="d0135-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0135-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0135-121">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d0135-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d0135-122">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d0135-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0135-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0135-123">Remarks</span></span>

<span data-ttu-id="d0135-124">Буфер индексов обычно блокируется, записывается в, а затем разблокируется для чтения.</span><span class="sxs-lookup"><span data-stu-id="d0135-124">The index buffer is usually locked, written to, and then unlocked for reading.</span></span> <span data-ttu-id="d0135-125">Буферы индекса сети исправлений представляют собой 16-битные буферы.</span><span class="sxs-lookup"><span data-stu-id="d0135-125">Patch mesh index buffers are 16-bit buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0135-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d0135-126">Requirements</span></span>



| <span data-ttu-id="d0135-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d0135-127">Requirement</span></span> | <span data-ttu-id="d0135-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d0135-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0135-129">Header</span><span class="sxs-lookup"><span data-stu-id="d0135-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d0135-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0135-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d0135-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d0135-131">Library</span></span><br/> | <dl> <span data-ttu-id="d0135-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0135-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0135-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0135-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0135-134">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="d0135-134">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="d0135-135">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="d0135-135">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
