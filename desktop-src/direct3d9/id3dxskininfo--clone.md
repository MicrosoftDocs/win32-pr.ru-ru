---
description: Создает точную копию объекта сведений об обложке.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'Метод ID3DXSkinInfo:: Clone (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edd9776b75d027a32b32b58c59fc82daaebfa3ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273747"
---
# <a name="id3dxskininfoclone-method"></a><span data-ttu-id="c2771-103">Метод ID3DXSkinInfo:: Clone</span><span class="sxs-lookup"><span data-stu-id="c2771-103">ID3DXSkinInfo::Clone method</span></span>

<span data-ttu-id="c2771-104">Создает точную копию объекта сведений об обложке.</span><span class="sxs-lookup"><span data-stu-id="c2771-104">Clones a skin info object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2771-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2771-105">Syntax</span></span>


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c2771-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2771-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2771-107">*ппскининфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c2771-107">*ppSkinInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2771-108">Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2771-108">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="c2771-109">Адрес указателя на объект [**ID3DXSkinInfo**](id3dxskininfo.md) , который будет содержать клонированный объект, если метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c2771-109">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) object, which will contain the cloned object if the method is successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2771-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2771-110">Return value</span></span>

<span data-ttu-id="c2771-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2771-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2771-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c2771-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c2771-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c2771-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2771-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c2771-114">Requirements</span></span>



| <span data-ttu-id="c2771-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c2771-115">Requirement</span></span> | <span data-ttu-id="c2771-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c2771-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2771-117">Header</span><span class="sxs-lookup"><span data-stu-id="c2771-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c2771-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2771-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c2771-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2771-119">Library</span></span><br/> | <dl> <span data-ttu-id="c2771-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2771-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2771-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2771-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2771-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="c2771-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 




