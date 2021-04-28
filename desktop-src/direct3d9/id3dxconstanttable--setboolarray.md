---
description: 'Метод ID3DXConstantTable:: Сетбуларрай — задает массив логических значений.'
ms.assetid: 323ad654-81e3-4986-a667-8333dd44a2d1
title: 'Метод ID3DXConstantTable:: Сетбуларрай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c967ffd1a6601144787621628ed1b019e775eddd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115212"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="25133-103">Метод ID3DXConstantTable:: Сетбуларрай</span><span class="sxs-lookup"><span data-stu-id="25133-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="25133-104">Задает массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="25133-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="25133-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25133-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="25133-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25133-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25133-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25133-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25133-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="25133-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="25133-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="25133-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="25133-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25133-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25133-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="25133-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="25133-112">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="25133-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="25133-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="25133-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="25133-114">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25133-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25133-115">Тип: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="25133-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25133-116">Массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="25133-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="25133-117">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25133-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25133-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25133-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25133-119">Число логических значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="25133-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25133-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25133-120">Return value</span></span>

<span data-ttu-id="25133-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25133-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25133-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="25133-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25133-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="25133-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="25133-124">Требования</span><span class="sxs-lookup"><span data-stu-id="25133-124">Requirements</span></span>



| <span data-ttu-id="25133-125">Требование</span><span class="sxs-lookup"><span data-stu-id="25133-125">Requirement</span></span> | <span data-ttu-id="25133-126">Значение</span><span class="sxs-lookup"><span data-stu-id="25133-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25133-127">Header</span><span class="sxs-lookup"><span data-stu-id="25133-127">Header</span></span><br/>  | <dl> <span data-ttu-id="25133-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="25133-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="25133-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="25133-129">Library</span></span><br/> | <dl> <span data-ttu-id="25133-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25133-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="25133-131">См. также</span><span class="sxs-lookup"><span data-stu-id="25133-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25133-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="25133-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
