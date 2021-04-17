---
description: Блокирует буфер сетки, содержащий данные атрибута сетки, и возвращает указатель на него.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'Метод ID3DXMesh:: Локкаттрибутебуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694114"
---
# <a name="id3dxmeshlockattributebuffer-method"></a><span data-ttu-id="4ad82-103">Метод ID3DXMesh:: Локкаттрибутебуффер</span><span class="sxs-lookup"><span data-stu-id="4ad82-103">ID3DXMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="4ad82-104">Блокирует буфер сетки, содержащий данные атрибута сетки, и возвращает указатель на него.</span><span class="sxs-lookup"><span data-stu-id="4ad82-104">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad82-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ad82-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="4ad82-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ad82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ad82-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ad82-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad82-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ad82-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ad82-109">Сочетание флагов блокировки (ноль или более), описывающих тип выполняемой блокировки.</span><span class="sxs-lookup"><span data-stu-id="4ad82-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="4ad82-110">Для этого метода допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4ad82-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="4ad82-111">D3DLOCK \_ отбросить</span><span class="sxs-lookup"><span data-stu-id="4ad82-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="4ad82-112">D3DLOCK \_ без \_ "грязного" \_ обновления</span><span class="sxs-lookup"><span data-stu-id="4ad82-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="4ad82-113">D3DLOCK \_ носислокк</span><span class="sxs-lookup"><span data-stu-id="4ad82-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="4ad82-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4ad82-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="4ad82-115">Описание флагов см. в разделе [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="4ad82-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad82-116">*ппдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4ad82-116">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad82-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4ad82-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="4ad82-118">Адрес указателя на буфер, содержащий DWORD для каждой грани в сетке.</span><span class="sxs-lookup"><span data-stu-id="4ad82-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ad82-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ad82-119">Return value</span></span>

<span data-ttu-id="4ad82-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ad82-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ad82-121">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4ad82-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4ad82-122">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="4ad82-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ad82-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ad82-123">Remarks</span></span>

<span data-ttu-id="4ad82-124">Если был вызван [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) , в сетке также будет таблица атрибутов, доступ к которой можно получить с помощью метода [**ID3DXBaseMesh:: жетаттрибутетабле**](id3dxbasemesh--getattributetable.md) .</span><span class="sxs-lookup"><span data-stu-id="4ad82-124">If [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) has been called, the mesh will also have an attribute table that can be accessed using the [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ad82-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4ad82-125">Requirements</span></span>



| <span data-ttu-id="4ad82-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4ad82-126">Requirement</span></span> | <span data-ttu-id="4ad82-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4ad82-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad82-128">Header</span><span class="sxs-lookup"><span data-stu-id="4ad82-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4ad82-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ad82-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4ad82-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4ad82-130">Library</span></span><br/> | <dl> <span data-ttu-id="4ad82-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ad82-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4ad82-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ad82-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad82-133">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="4ad82-133">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="4ad82-134">**ID3DXMesh:: Унлоккаттрибутебуффер**</span><span class="sxs-lookup"><span data-stu-id="4ad82-134">**ID3DXMesh::UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="4ad82-135">**ID3DXBaseMesh:: Жетаттрибутетабле**</span><span class="sxs-lookup"><span data-stu-id="4ad82-135">**ID3DXBaseMesh::GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[<span data-ttu-id="4ad82-136">**ID3DXMesh:: Сетаттрибутетабле**</span><span class="sxs-lookup"><span data-stu-id="4ad82-136">**ID3DXMesh::SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
