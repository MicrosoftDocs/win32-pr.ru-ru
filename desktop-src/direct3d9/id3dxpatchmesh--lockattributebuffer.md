---
description: Блокирует буфер атрибута.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'Метод ID3DXPatchMesh:: Локкаттрибутебуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105665006"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a><span data-ttu-id="ce83b-103">Метод ID3DXPatchMesh:: Локкаттрибутебуффер</span><span class="sxs-lookup"><span data-stu-id="ce83b-103">ID3DXPatchMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="ce83b-104">Блокирует буфер атрибута.</span><span class="sxs-lookup"><span data-stu-id="ce83b-104">Locks the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce83b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce83b-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="ce83b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce83b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce83b-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce83b-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce83b-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce83b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce83b-109">Сочетание флагов блокировки (ноль или более), описывающих тип выполняемой блокировки.</span><span class="sxs-lookup"><span data-stu-id="ce83b-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="ce83b-110">Для этого метода допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ce83b-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="ce83b-111">D3DLOCK \_ отбросить</span><span class="sxs-lookup"><span data-stu-id="ce83b-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="ce83b-112">D3DLOCK \_ без \_ "грязного" \_ обновления</span><span class="sxs-lookup"><span data-stu-id="ce83b-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="ce83b-113">D3DLOCK \_ носислокк</span><span class="sxs-lookup"><span data-stu-id="ce83b-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="ce83b-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ce83b-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="ce83b-115">Описание флагов см. в разделе [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="ce83b-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce83b-116">*ппдата* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ce83b-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ce83b-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ce83b-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="ce83b-118">Адрес указателя на буфер, содержащий DWORD для каждой грани в сетке.</span><span class="sxs-lookup"><span data-stu-id="ce83b-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce83b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce83b-119">Return value</span></span>

<span data-ttu-id="ce83b-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce83b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce83b-121">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ce83b-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ce83b-122">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ce83b-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce83b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce83b-123">Remarks</span></span>

<span data-ttu-id="ce83b-124">Буфер атрибутов обычно блокируется, записывается в, а затем разблокируется для чтения.</span><span class="sxs-lookup"><span data-stu-id="ce83b-124">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce83b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ce83b-125">Requirements</span></span>



| <span data-ttu-id="ce83b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ce83b-126">Requirement</span></span> | <span data-ttu-id="ce83b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ce83b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce83b-128">Header</span><span class="sxs-lookup"><span data-stu-id="ce83b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ce83b-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce83b-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ce83b-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce83b-130">Library</span></span><br/> | <dl> <span data-ttu-id="ce83b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce83b-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ce83b-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce83b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce83b-133">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="ce83b-133">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
