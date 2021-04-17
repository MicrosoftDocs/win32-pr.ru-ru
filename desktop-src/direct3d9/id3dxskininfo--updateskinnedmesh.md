---
description: Применяет обложки программного обеспечения к целевым вершинам на основе текущих матриц.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'Метод ID3DXSkinInfo:: Упдатескиннедмеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713445"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a><span data-ttu-id="c1f59-103">Метод ID3DXSkinInfo:: Упдатескиннедмеш</span><span class="sxs-lookup"><span data-stu-id="c1f59-103">ID3DXSkinInfo::UpdateSkinnedMesh method</span></span>

<span data-ttu-id="c1f59-104">Применяет обложки программного обеспечения к целевым вершинам на основе текущих матриц.</span><span class="sxs-lookup"><span data-stu-id="c1f59-104">Applies software skinning to the target vertices based on the current matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1f59-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1f59-105">Syntax</span></span>


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a><span data-ttu-id="c1f59-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1f59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1f59-107">*пбонетрансформс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1f59-107">*pBoneTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1f59-108">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1f59-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c1f59-109">Матрица преобразования костей.</span><span class="sxs-lookup"><span data-stu-id="c1f59-109">Bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="c1f59-110">*пбонеинвтранспосетрансформс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1f59-110">*pBoneInvTransposeTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1f59-111">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1f59-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c1f59-112">Обратная трансформация матрицы преобразования костей.</span><span class="sxs-lookup"><span data-stu-id="c1f59-112">Inverse transpose of the bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="c1f59-113">*пвертицессрк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1f59-113">*pVerticesSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1f59-114">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f59-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1f59-115">Указатель на буфер, содержащий исходные вершины.</span><span class="sxs-lookup"><span data-stu-id="c1f59-115">Pointer to the buffer containing the source vertices.</span></span>

</dd> <dt>

<span data-ttu-id="c1f59-116">*пвертицесдст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1f59-116">*pVerticesDst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1f59-117">Тип: **[ **PVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f59-117">Type: **[**PVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1f59-118">Указатель на буфер, содержащий целевые вершины.</span><span class="sxs-lookup"><span data-stu-id="c1f59-118">Pointer to the buffer containing the destination vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1f59-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1f59-119">Return value</span></span>

<span data-ttu-id="c1f59-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1f59-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1f59-121">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c1f59-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c1f59-122">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c1f59-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1f59-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1f59-123">Remarks</span></span>

<span data-ttu-id="c1f59-124">При использовании для обложки вершин с двумя элементами позиционирования этот метод обрисовывает второй элемент расположения с обратной стороны кости, а не саму кость.</span><span class="sxs-lookup"><span data-stu-id="c1f59-124">When used to skin vertices with two position elements, this method skins the second position element with the inverse of the bone instead of the bone itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1f59-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c1f59-125">Requirements</span></span>



| <span data-ttu-id="c1f59-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c1f59-126">Requirement</span></span> | <span data-ttu-id="c1f59-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c1f59-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f59-128">Header</span><span class="sxs-lookup"><span data-stu-id="c1f59-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c1f59-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1f59-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c1f59-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1f59-130">Library</span></span><br/> | <dl> <span data-ttu-id="c1f59-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1f59-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1f59-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1f59-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f59-133">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="c1f59-133">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
