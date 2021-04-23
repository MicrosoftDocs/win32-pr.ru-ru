---
description: Возвращает имя кости из индекса костей.
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'Метод ID3DXSkinInfo:: Жетбоненаме (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0566d423d277dc3f39f36f8c1fda297ec917eb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703629"
---
# <a name="id3dxskininfogetbonename-method"></a><span data-ttu-id="d7c9d-103">Метод ID3DXSkinInfo:: Жетбоненаме</span><span class="sxs-lookup"><span data-stu-id="d7c9d-103">ID3DXSkinInfo::GetBoneName method</span></span>

<span data-ttu-id="d7c9d-104">Возвращает имя кости из индекса костей.</span><span class="sxs-lookup"><span data-stu-id="d7c9d-104">Gets the bone name, from the bone index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c9d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7c9d-105">Syntax</span></span>


```C++
LPCSTR GetBoneName(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="d7c9d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7c9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7c9d-107">*Кость* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7c9d-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7c9d-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7c9d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7c9d-109">Номер кости.</span><span class="sxs-lookup"><span data-stu-id="d7c9d-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7c9d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7c9d-110">Return value</span></span>

<span data-ttu-id="d7c9d-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7c9d-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7c9d-112">Возвращает имя кости.</span><span class="sxs-lookup"><span data-stu-id="d7c9d-112">Returns the bone name.</span></span> <span data-ttu-id="d7c9d-113">Не освобождайте эту строку.</span><span class="sxs-lookup"><span data-stu-id="d7c9d-113">Do not free this string.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c9d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d7c9d-114">Requirements</span></span>



| <span data-ttu-id="d7c9d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d7c9d-115">Requirement</span></span> | <span data-ttu-id="d7c9d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d7c9d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c9d-117">Header</span><span class="sxs-lookup"><span data-stu-id="d7c9d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d7c9d-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7c9d-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d7c9d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d7c9d-119">Library</span></span><br/> | <dl> <span data-ttu-id="d7c9d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7c9d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7c9d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7c9d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c9d-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="d7c9d-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="d7c9d-123">**ID3DXSkinInfo:: Сетбоненаме**</span><span class="sxs-lookup"><span data-stu-id="d7c9d-123">**ID3DXSkinInfo::SetBoneName**</span></span>](id3dxskininfo--setbonename.md)
</dt> <dt>

[<span data-ttu-id="d7c9d-124">**ID3DXSkinInfo:: Жетнумбонес**</span><span class="sxs-lookup"><span data-stu-id="d7c9d-124">**ID3DXSkinInfo::GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
