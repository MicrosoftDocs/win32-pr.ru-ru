---
description: Задает массив логических значений.
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
ms.openlocfilehash: d573a2c44b54809ec259a0ceb5abab02ef37df34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694187"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="ccbad-103">Метод ID3DXConstantTable:: Сетбуларрай</span><span class="sxs-lookup"><span data-stu-id="ccbad-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="ccbad-104">Задает массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="ccbad-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccbad-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccbad-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="ccbad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccbad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccbad-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ccbad-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccbad-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ccbad-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ccbad-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="ccbad-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="ccbad-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ccbad-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccbad-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ccbad-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ccbad-112">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="ccbad-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="ccbad-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ccbad-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccbad-114">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ccbad-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccbad-115">Тип: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ccbad-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccbad-116">Массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="ccbad-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="ccbad-117">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ccbad-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccbad-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccbad-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccbad-119">Число логических значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="ccbad-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccbad-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccbad-120">Return value</span></span>

<span data-ttu-id="ccbad-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccbad-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccbad-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ccbad-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ccbad-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ccbad-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccbad-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ccbad-124">Requirements</span></span>



| <span data-ttu-id="ccbad-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ccbad-125">Requirement</span></span> | <span data-ttu-id="ccbad-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ccbad-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccbad-127">Header</span><span class="sxs-lookup"><span data-stu-id="ccbad-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ccbad-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccbad-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ccbad-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ccbad-129">Library</span></span><br/> | <dl> <span data-ttu-id="ccbad-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccbad-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ccbad-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccbad-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccbad-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="ccbad-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
