---
description: Блокировка буфера вершин.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'Метод ID3DXPatchMesh:: Локквертексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914768"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a><span data-ttu-id="fc77f-103">Метод ID3DXPatchMesh:: Локквертексбуффер</span><span class="sxs-lookup"><span data-stu-id="fc77f-103">ID3DXPatchMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="fc77f-104">Блокировка буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="fc77f-104">Lock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc77f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc77f-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="fc77f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc77f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc77f-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc77f-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc77f-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc77f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc77f-109">Сочетание флагов блокировки (ноль или более), описывающих тип выполняемой блокировки.</span><span class="sxs-lookup"><span data-stu-id="fc77f-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="fc77f-110">Для этого метода допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="fc77f-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="fc77f-111">D3DLOCK \_ отбросить</span><span class="sxs-lookup"><span data-stu-id="fc77f-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="fc77f-112">D3DLOCK \_ без \_ "грязного" \_ обновления</span><span class="sxs-lookup"><span data-stu-id="fc77f-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="fc77f-113">D3DLOCK \_ носислокк</span><span class="sxs-lookup"><span data-stu-id="fc77f-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="fc77f-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fc77f-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="fc77f-115">D3DLOCK \_ нуверврите</span><span class="sxs-lookup"><span data-stu-id="fc77f-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="fc77f-116">Описание флагов см. в разделе [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="fc77f-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc77f-117">*ппдата* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fc77f-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fc77f-118">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc77f-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fc77f-119">\*Указатель void на буфер памяти, содержащий возвращенные данные вершин.</span><span class="sxs-lookup"><span data-stu-id="fc77f-119">VOID\* pointer to a memory buffer containing the returned vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc77f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc77f-120">Return value</span></span>

<span data-ttu-id="fc77f-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc77f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc77f-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fc77f-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fc77f-123">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fc77f-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc77f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc77f-124">Remarks</span></span>

<span data-ttu-id="fc77f-125">Буфер вершин обычно блокируется, записывается в, а затем разблокируется для чтения.</span><span class="sxs-lookup"><span data-stu-id="fc77f-125">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

<span data-ttu-id="fc77f-126">В сетчатых обновлениях используются 16-битные буферы индексов.</span><span class="sxs-lookup"><span data-stu-id="fc77f-126">Patch meshes use 16-bit index buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc77f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="fc77f-127">Requirements</span></span>



| <span data-ttu-id="fc77f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="fc77f-128">Requirement</span></span> | <span data-ttu-id="fc77f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="fc77f-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc77f-130">Header</span><span class="sxs-lookup"><span data-stu-id="fc77f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="fc77f-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc77f-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fc77f-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc77f-132">Library</span></span><br/> | <dl> <span data-ttu-id="fc77f-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc77f-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc77f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc77f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc77f-135">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="fc77f-135">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
