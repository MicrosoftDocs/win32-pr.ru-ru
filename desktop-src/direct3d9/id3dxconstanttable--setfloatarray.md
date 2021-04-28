---
description: 'Метод ID3DXConstantTable:: Сетфлоатаррай — задает массив чисел с плавающей запятой.'
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
ms.openlocfilehash: 23c96cb2bfc8113fd167c8b57a21a46285b691a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115172"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a><span data-ttu-id="b588c-103">Метод ID3DXConstantTable:: Сетфлоатаррай</span><span class="sxs-lookup"><span data-stu-id="b588c-103">ID3DXConstantTable::SetFloatArray method</span></span>

<span data-ttu-id="b588c-104">Задает массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b588c-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b588c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b588c-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="b588c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b588c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b588c-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b588c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b588c-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b588c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b588c-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="b588c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="b588c-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b588c-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b588c-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b588c-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b588c-112">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="b588c-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="b588c-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b588c-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b588c-114">*Общая папка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b588c-114">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b588c-115">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b588c-115">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b588c-116">Массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b588c-116">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="b588c-117">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b588c-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b588c-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b588c-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b588c-119">Число значений с плавающей запятой в массиве.</span><span class="sxs-lookup"><span data-stu-id="b588c-119">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b588c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b588c-120">Return value</span></span>

<span data-ttu-id="b588c-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b588c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b588c-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b588c-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b588c-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b588c-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b588c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b588c-124">Requirements</span></span>



| <span data-ttu-id="b588c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b588c-125">Requirement</span></span> | <span data-ttu-id="b588c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b588c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b588c-127">Header</span><span class="sxs-lookup"><span data-stu-id="b588c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b588c-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b588c-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b588c-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b588c-129">Library</span></span><br/> | <dl> <span data-ttu-id="b588c-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b588c-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b588c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b588c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b588c-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b588c-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
