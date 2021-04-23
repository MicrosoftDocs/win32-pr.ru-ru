---
description: Возвращает устройство, создавшее сетку.
ms.assetid: b03dadda-ca54-4a55-a0a5-cf5ccdb55a72
title: Метод ID3DXPatchMesh::-Device (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a026398b719bf3ba9a9c02082105cbc7dd299013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000498"
---
# <a name="id3dxpatchmeshgetdevice-method"></a><span data-ttu-id="ab75e-103">Метод ID3DXPatchMesh:: of Device</span><span class="sxs-lookup"><span data-stu-id="ab75e-103">ID3DXPatchMesh::GetDevice method</span></span>

<span data-ttu-id="ab75e-104">Возвращает устройство, создавшее сетку.</span><span class="sxs-lookup"><span data-stu-id="ab75e-104">Gets the device that created the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab75e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab75e-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ab75e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab75e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab75e-107">*ппдевице* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ab75e-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab75e-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="ab75e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="ab75e-109">Указатель на устройство.</span><span class="sxs-lookup"><span data-stu-id="ab75e-109">Pointer to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab75e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab75e-110">Return value</span></span>

<span data-ttu-id="ab75e-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab75e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab75e-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ab75e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ab75e-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ab75e-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab75e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ab75e-114">Requirements</span></span>



| <span data-ttu-id="ab75e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ab75e-115">Requirement</span></span> | <span data-ttu-id="ab75e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ab75e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab75e-117">Header</span><span class="sxs-lookup"><span data-stu-id="ab75e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ab75e-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab75e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ab75e-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ab75e-119">Library</span></span><br/> | <dl> <span data-ttu-id="ab75e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab75e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab75e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab75e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab75e-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="ab75e-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
