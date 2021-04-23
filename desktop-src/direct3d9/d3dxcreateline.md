---
description: Использует левую систему координат для создания линии.
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: Функция D3DXCreateLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cf7d75ca63d64be39733b36a1b7d7a1b464238e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694124"
---
# <a name="d3dxcreateline-function"></a><span data-ttu-id="17004-103">Функция D3DXCreateLine</span><span class="sxs-lookup"><span data-stu-id="17004-103">D3DXCreateLine function</span></span>

<span data-ttu-id="17004-104">Использует левую систему координат для создания линии.</span><span class="sxs-lookup"><span data-stu-id="17004-104">Uses a left-handed coordinate system to create a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="17004-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17004-105">Syntax</span></span>


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a><span data-ttu-id="17004-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17004-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17004-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17004-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17004-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="17004-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="17004-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с сеткой созданных Box.</span><span class="sxs-lookup"><span data-stu-id="17004-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="17004-110">*пплине* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17004-110">*ppLine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17004-111">Тип: **[ **LPD3DXLINE**](id3dxline.md)\***</span><span class="sxs-lookup"><span data-stu-id="17004-111">Type: **[**LPD3DXLINE**](id3dxline.md)\***</span></span>

<span data-ttu-id="17004-112">Указатель на интерфейс [**ID3DXLine**](id3dxline.md) .</span><span class="sxs-lookup"><span data-stu-id="17004-112">Pointer to an [**ID3DXLine**](id3dxline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17004-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17004-113">Return value</span></span>

<span data-ttu-id="17004-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17004-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17004-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="17004-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="17004-116">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="17004-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="17004-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17004-117">Remarks</span></span>

<span data-ttu-id="17004-118">Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).</span><span class="sxs-lookup"><span data-stu-id="17004-118">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) Flexible Vertex Format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="17004-119">Требования</span><span class="sxs-lookup"><span data-stu-id="17004-119">Requirements</span></span>



| <span data-ttu-id="17004-120">Требование</span><span class="sxs-lookup"><span data-stu-id="17004-120">Requirement</span></span> | <span data-ttu-id="17004-121">Значение</span><span class="sxs-lookup"><span data-stu-id="17004-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17004-122">Header</span><span class="sxs-lookup"><span data-stu-id="17004-122">Header</span></span><br/>  | <dl> <span data-ttu-id="17004-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="17004-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="17004-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="17004-124">Library</span></span><br/> | <dl> <span data-ttu-id="17004-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17004-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17004-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17004-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17004-127">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="17004-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
