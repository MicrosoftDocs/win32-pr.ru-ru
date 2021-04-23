---
description: Возвращает матрицу смещения кости.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'Метод ID3DXSkinInfo:: Жетбонеоффсетматрикс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354093"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a><span data-ttu-id="46a9f-103">Метод ID3DXSkinInfo:: Жетбонеоффсетматрикс</span><span class="sxs-lookup"><span data-stu-id="46a9f-103">ID3DXSkinInfo::GetBoneOffsetMatrix method</span></span>

<span data-ttu-id="46a9f-104">Возвращает матрицу смещения кости.</span><span class="sxs-lookup"><span data-stu-id="46a9f-104">Gets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="46a9f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46a9f-105">Syntax</span></span>


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="46a9f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="46a9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46a9f-107">*Кость* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46a9f-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46a9f-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46a9f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46a9f-109">Номер кости.</span><span class="sxs-lookup"><span data-stu-id="46a9f-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46a9f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46a9f-110">Return value</span></span>

<span data-ttu-id="46a9f-111">Тип: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="46a9f-111">Type: **[**LPD3DXMATRIX**](d3dxmatrix.md)**</span></span>

<span data-ttu-id="46a9f-112">Возвращает указатель на матрицу смещения кости.</span><span class="sxs-lookup"><span data-stu-id="46a9f-112">Returns a pointer to the bone offset matrix.</span></span> <span data-ttu-id="46a9f-113">Не освобождайте этот указатель.</span><span class="sxs-lookup"><span data-stu-id="46a9f-113">Do not free this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="46a9f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="46a9f-114">Requirements</span></span>



| <span data-ttu-id="46a9f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="46a9f-115">Requirement</span></span> | <span data-ttu-id="46a9f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="46a9f-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46a9f-117">Header</span><span class="sxs-lookup"><span data-stu-id="46a9f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="46a9f-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="46a9f-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="46a9f-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46a9f-119">Library</span></span><br/> | <dl> <span data-ttu-id="46a9f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46a9f-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46a9f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46a9f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a9f-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="46a9f-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="46a9f-123">**сетбонеоффсетматрикс**</span><span class="sxs-lookup"><span data-stu-id="46a9f-123">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[<span data-ttu-id="46a9f-124">**жетнумбонес**</span><span class="sxs-lookup"><span data-stu-id="46a9f-124">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
