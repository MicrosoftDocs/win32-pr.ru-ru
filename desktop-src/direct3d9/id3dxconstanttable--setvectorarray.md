---
description: Задает массив векторов 4D.
ms.assetid: bd453384-4f38-4017-a9a5-cac605919940
title: 'Метод ID3DXConstantTable:: Сетвектораррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6c68621a3f97251cdd88836792bf55980f28311
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703807"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="6b497-103">Метод ID3DXConstantTable:: Сетвектораррай</span><span class="sxs-lookup"><span data-stu-id="6b497-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="6b497-104">Задает массив векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="6b497-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b497-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b497-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="6b497-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b497-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b497-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b497-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b497-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6b497-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6b497-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="6b497-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="6b497-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b497-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b497-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6b497-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6b497-112">Уникальный идентификатор массива констант Vector.</span><span class="sxs-lookup"><span data-stu-id="6b497-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="6b497-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6b497-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b497-114">*пвектор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b497-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b497-115">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b497-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6b497-116">Массив векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="6b497-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="6b497-117">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b497-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b497-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b497-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b497-119">Количество векторов в массиве.</span><span class="sxs-lookup"><span data-stu-id="6b497-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b497-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b497-120">Return value</span></span>

<span data-ttu-id="6b497-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b497-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b497-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6b497-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6b497-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="6b497-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b497-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6b497-124">Requirements</span></span>



| <span data-ttu-id="6b497-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6b497-125">Requirement</span></span> | <span data-ttu-id="6b497-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6b497-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b497-127">Header</span><span class="sxs-lookup"><span data-stu-id="6b497-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6b497-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b497-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6b497-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b497-129">Library</span></span><br/> | <dl> <span data-ttu-id="6b497-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b497-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6b497-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b497-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b497-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="6b497-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
