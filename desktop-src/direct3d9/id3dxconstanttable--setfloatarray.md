---
description: Задает массив чисел с плавающей запятой.
ms.assetid: 7a622dd5-47ed-4166-a6df-f484b03e0b5a
title: 'Метод ID3DXConstantTable:: Сетфлоатаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d75d4171ab51859e4095acbe5d3e86d704b1f437
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273813"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a><span data-ttu-id="e50ee-103">Метод ID3DXConstantTable:: Сетфлоатаррай</span><span class="sxs-lookup"><span data-stu-id="e50ee-103">ID3DXConstantTable::SetFloatArray method</span></span>

<span data-ttu-id="e50ee-104">Задает массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e50ee-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e50ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e50ee-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="e50ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e50ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e50ee-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e50ee-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50ee-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e50ee-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e50ee-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="e50ee-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="e50ee-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e50ee-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50ee-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e50ee-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e50ee-112">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="e50ee-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="e50ee-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e50ee-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50ee-114">*Общая папка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e50ee-114">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50ee-115">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e50ee-115">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e50ee-116">Массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e50ee-116">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="e50ee-117">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e50ee-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50ee-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e50ee-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e50ee-119">Число значений с плавающей запятой в массиве.</span><span class="sxs-lookup"><span data-stu-id="e50ee-119">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e50ee-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e50ee-120">Return value</span></span>

<span data-ttu-id="e50ee-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e50ee-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e50ee-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e50ee-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e50ee-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e50ee-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e50ee-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e50ee-124">Requirements</span></span>



| <span data-ttu-id="e50ee-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e50ee-125">Requirement</span></span> | <span data-ttu-id="e50ee-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e50ee-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e50ee-127">Header</span><span class="sxs-lookup"><span data-stu-id="e50ee-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e50ee-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e50ee-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e50ee-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e50ee-129">Library</span></span><br/> | <dl> <span data-ttu-id="e50ee-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e50ee-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e50ee-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e50ee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e50ee-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="e50ee-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
