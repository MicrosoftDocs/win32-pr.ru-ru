---
description: Задает массив целых чисел.
ms.assetid: 15add9df-966d-45aa-b29c-d4bed2a125f4
title: 'Метод ID3DXConstantTable:: Сетинтаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f89de7d784ce355570d369606bfa67ddd6f5acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713731"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="e382c-103">Метод ID3DXConstantTable:: Сетинтаррай</span><span class="sxs-lookup"><span data-stu-id="e382c-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="e382c-104">Задает массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="e382c-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e382c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e382c-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="e382c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e382c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e382c-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e382c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e382c-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e382c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e382c-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="e382c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="e382c-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e382c-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e382c-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e382c-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e382c-112">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="e382c-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="e382c-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e382c-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e382c-114">*PN* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e382c-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e382c-115">Тип: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e382c-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e382c-116">Массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="e382c-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="e382c-117">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e382c-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e382c-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e382c-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e382c-119">Число целочисленных значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="e382c-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e382c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e382c-120">Return value</span></span>

<span data-ttu-id="e382c-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e382c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e382c-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e382c-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e382c-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e382c-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e382c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e382c-124">Requirements</span></span>



| <span data-ttu-id="e382c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e382c-125">Requirement</span></span> | <span data-ttu-id="e382c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e382c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e382c-127">Header</span><span class="sxs-lookup"><span data-stu-id="e382c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e382c-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e382c-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e382c-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e382c-129">Library</span></span><br/> | <dl> <span data-ttu-id="e382c-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e382c-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e382c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e382c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e382c-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="e382c-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
