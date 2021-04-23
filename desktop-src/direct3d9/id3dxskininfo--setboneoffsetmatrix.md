---
description: Задает матрицу смещения кости.
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'Метод ID3DXSkinInfo:: Сетбонеоффсетматрикс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 283d36bb68e33cfa0e2349bab304b0cdde7ef77e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820916"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a><span data-ttu-id="74eeb-103">Метод ID3DXSkinInfo:: Сетбонеоффсетматрикс</span><span class="sxs-lookup"><span data-stu-id="74eeb-103">ID3DXSkinInfo::SetBoneOffsetMatrix method</span></span>

<span data-ttu-id="74eeb-104">Задает матрицу смещения кости.</span><span class="sxs-lookup"><span data-stu-id="74eeb-104">Sets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="74eeb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74eeb-105">Syntax</span></span>


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a><span data-ttu-id="74eeb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74eeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74eeb-107">*Кость* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74eeb-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74eeb-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74eeb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74eeb-109">Номер кости.</span><span class="sxs-lookup"><span data-stu-id="74eeb-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="74eeb-110">*пбонетрансформ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74eeb-110">*pBoneTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74eeb-111">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="74eeb-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="74eeb-112">Указатель на матрицу смещения кости.</span><span class="sxs-lookup"><span data-stu-id="74eeb-112">Pointer to the bone offset matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74eeb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74eeb-113">Return value</span></span>

<span data-ttu-id="74eeb-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74eeb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74eeb-115">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="74eeb-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74eeb-116">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="74eeb-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="74eeb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74eeb-117">Remarks</span></span>

<span data-ttu-id="74eeb-118">Имена костей возвращаются функцией [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span><span class="sxs-lookup"><span data-stu-id="74eeb-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74eeb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="74eeb-119">Requirements</span></span>



| <span data-ttu-id="74eeb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="74eeb-120">Requirement</span></span> | <span data-ttu-id="74eeb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="74eeb-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74eeb-122">Header</span><span class="sxs-lookup"><span data-stu-id="74eeb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="74eeb-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="74eeb-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="74eeb-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74eeb-124">Library</span></span><br/> | <dl> <span data-ttu-id="74eeb-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74eeb-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74eeb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74eeb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74eeb-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="74eeb-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="74eeb-128">**ID3DXSkinInfo:: Жетбонеоффсетматрикс**</span><span class="sxs-lookup"><span data-stu-id="74eeb-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 
