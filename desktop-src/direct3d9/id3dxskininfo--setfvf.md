---
description: Задает тип гибкого формата вершин (ФВФ).
ms.assetid: e581dcd4-7e17-4c36-aac9-c2942924cf51
title: 'Метод ID3DXSkinInfo:: Сетфвф (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 010385597442ba1546c20122f6551fca0cfcf81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703625"
---
# <a name="id3dxskininfosetfvf-method"></a><span data-ttu-id="fa828-103">Метод ID3DXSkinInfo:: Сетфвф</span><span class="sxs-lookup"><span data-stu-id="fa828-103">ID3DXSkinInfo::SetFVF method</span></span>

<span data-ttu-id="fa828-104">Задает тип гибкого формата вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="fa828-104">Sets the flexible vertex format (FVF) type.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa828-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa828-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="fa828-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa828-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa828-107">*Фвф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa828-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa828-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa828-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa828-109">Гибкий формат вершин.</span><span class="sxs-lookup"><span data-stu-id="fa828-109">Flexible vertex format.</span></span> <span data-ttu-id="fa828-110">См. [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="fa828-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa828-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa828-111">Return value</span></span>

<span data-ttu-id="fa828-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa828-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa828-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fa828-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fa828-114">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="fa828-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa828-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fa828-115">Requirements</span></span>



| <span data-ttu-id="fa828-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fa828-116">Requirement</span></span> | <span data-ttu-id="fa828-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fa828-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa828-118">Header</span><span class="sxs-lookup"><span data-stu-id="fa828-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fa828-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa828-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fa828-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa828-120">Library</span></span><br/> | <dl> <span data-ttu-id="fa828-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa828-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa828-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa828-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa828-123">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="fa828-123">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
