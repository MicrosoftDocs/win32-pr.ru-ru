---
description: Задает имя кости.
ms.assetid: 2eecddb8-4efa-41a3-be83-7404047a9857
title: 'Метод ID3DXSkinInfo:: Сетбоненаме (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c9190c12eac21963d116f60d5a7aa09f97db796
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273691"
---
# <a name="id3dxskininfosetbonename-method"></a><span data-ttu-id="190cd-103">Метод ID3DXSkinInfo:: Сетбоненаме</span><span class="sxs-lookup"><span data-stu-id="190cd-103">ID3DXSkinInfo::SetBoneName method</span></span>

<span data-ttu-id="190cd-104">Задает имя кости.</span><span class="sxs-lookup"><span data-stu-id="190cd-104">Sets the bone name.</span></span>

## <a name="syntax"></a><span data-ttu-id="190cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="190cd-105">Syntax</span></span>


```C++
HRESULT SetBoneName(
  [in] DWORD  Bone,
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="190cd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="190cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="190cd-107">*Кость* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190cd-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190cd-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="190cd-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="190cd-109">Номер кости</span><span class="sxs-lookup"><span data-stu-id="190cd-109">Bone number</span></span>

</dd> <dt>

<span data-ttu-id="190cd-110">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="190cd-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="190cd-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="190cd-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="190cd-112">Имя кости</span><span class="sxs-lookup"><span data-stu-id="190cd-112">Bone name</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="190cd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="190cd-113">Return value</span></span>

<span data-ttu-id="190cd-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="190cd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="190cd-115">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="190cd-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="190cd-116">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="190cd-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="190cd-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="190cd-117">Remarks</span></span>

<span data-ttu-id="190cd-118">Имена костей возвращаются функцией [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span><span class="sxs-lookup"><span data-stu-id="190cd-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="190cd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="190cd-119">Requirements</span></span>



| <span data-ttu-id="190cd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="190cd-120">Requirement</span></span> | <span data-ttu-id="190cd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="190cd-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="190cd-122">Header</span><span class="sxs-lookup"><span data-stu-id="190cd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="190cd-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="190cd-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="190cd-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="190cd-124">Library</span></span><br/> | <dl> <span data-ttu-id="190cd-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="190cd-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="190cd-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="190cd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="190cd-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="190cd-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="190cd-128">**ID3DXSkinInfo:: Жетбоненаме**</span><span class="sxs-lookup"><span data-stu-id="190cd-128">**ID3DXSkinInfo::GetBoneName**</span></span>](id3dxskininfo--getbonename.md)
</dt> </dl>

 

 
