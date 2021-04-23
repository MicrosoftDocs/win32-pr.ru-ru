---
description: Возвращает максимальное влияние на грань в сетке треугольников с указанным буфером индекса.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'Метод ID3DXSkinInfo:: Жетмаксфацеинфлуенцес (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424314"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a><span data-ttu-id="8e3a6-103">Метод ID3DXSkinInfo:: Жетмаксфацеинфлуенцес</span><span class="sxs-lookup"><span data-stu-id="8e3a6-103">ID3DXSkinInfo::GetMaxFaceInfluences method</span></span>

<span data-ttu-id="8e3a6-104">Возвращает максимальное влияние на грань в сетке треугольников с указанным буфером индекса.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-104">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e3a6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e3a6-105">Syntax</span></span>


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="8e3a6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e3a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e3a6-107">*ПИБ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e3a6-107">*pIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e3a6-108">Тип: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="8e3a6-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span></span>

<span data-ttu-id="8e3a6-109">Указатель на индексный буфер, содержащий данные индекса сетки.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-109">Pointer to the index buffer that contains the mesh index data.</span></span>

</dd> <dt>

<span data-ttu-id="8e3a6-110">*Нумфацес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e3a6-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e3a6-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e3a6-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e3a6-112">Число лиц в сетке.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-112">Number of faces in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8e3a6-113">*максфацеинфлуенцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e3a6-113">*maxFaceInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e3a6-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e3a6-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8e3a6-115">Указатель на максимальное влияние на лицо.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-115">Pointer to the maximum face influences.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e3a6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e3a6-116">Return value</span></span>

<span data-ttu-id="8e3a6-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e3a6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e3a6-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8e3a6-119">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e3a6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8e3a6-120">Requirements</span></span>



| <span data-ttu-id="8e3a6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8e3a6-121">Requirement</span></span> | <span data-ttu-id="8e3a6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8e3a6-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3a6-123">Header</span><span class="sxs-lookup"><span data-stu-id="8e3a6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8e3a6-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e3a6-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8e3a6-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e3a6-125">Library</span></span><br/> | <dl> <span data-ttu-id="8e3a6-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e3a6-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8e3a6-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e3a6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e3a6-128">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="8e3a6-128">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
