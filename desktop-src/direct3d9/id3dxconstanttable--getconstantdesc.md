---
description: Возвращает указатель на массив константных описаний в таблице констант.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'Метод ID3DXConstantTable:: Жетконстантдеск (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000384"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a><span data-ttu-id="08e40-103">Метод ID3DXConstantTable:: Жетконстантдеск</span><span class="sxs-lookup"><span data-stu-id="08e40-103">ID3DXConstantTable::GetConstantDesc method</span></span>

<span data-ttu-id="08e40-104">Возвращает указатель на массив константных описаний в таблице констант.</span><span class="sxs-lookup"><span data-stu-id="08e40-104">Gets a pointer to an array of constant descriptions in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08e40-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="08e40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08e40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08e40-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08e40-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08e40-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="08e40-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="08e40-109">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="08e40-109">Unique identifier to a constant.</span></span> <span data-ttu-id="08e40-110">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="08e40-110">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="08e40-111">*пдеск* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="08e40-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08e40-112">Тип: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="08e40-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="08e40-113">Возвращает указатель на массив описаний.</span><span class="sxs-lookup"><span data-stu-id="08e40-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="08e40-114">См. [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="08e40-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="08e40-115">*pCount* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="08e40-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08e40-116">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="08e40-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="08e40-117">Указанный вход должен быть максимальным размером массива.</span><span class="sxs-lookup"><span data-stu-id="08e40-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="08e40-118">Выходные данные — это количество элементов, заполняемых в массиве при возврате функции.</span><span class="sxs-lookup"><span data-stu-id="08e40-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08e40-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08e40-119">Return value</span></span>

<span data-ttu-id="08e40-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08e40-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08e40-121">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="08e40-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="08e40-122">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="08e40-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="08e40-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08e40-123">Remarks</span></span>

<span data-ttu-id="08e40-124">**ID3DXConstantTable:: жетконстантдеск** иногда возвращает [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md) с числом регистров \_ 0.</span><span class="sxs-lookup"><span data-stu-id="08e40-124">**ID3DXConstantTable::GetConstantDesc** will sometimes return a [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md) with a Register\_Count of 0.</span></span> <span data-ttu-id="08e40-125">Это произойдет, когда константа появится в более чем одном \_ наборе регистров, но не содержит место в выделенном наборе регистров.</span><span class="sxs-lookup"><span data-stu-id="08e40-125">This will happen with a constant appears in more than one Register\_Set but does not have space in that register set allocated.</span></span>

<span data-ttu-id="08e40-126">Так как образец может отображаться в таблице констант более одного раза, этот метод может возвращать массив описаний, каждый из которых имеет другой индекс Register.</span><span class="sxs-lookup"><span data-stu-id="08e40-126">Because a sampler can appear more than once in a constant table, this method can return an array of descriptions, each one with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e40-127">Требования</span><span class="sxs-lookup"><span data-stu-id="08e40-127">Requirements</span></span>



| <span data-ttu-id="08e40-128">Требование</span><span class="sxs-lookup"><span data-stu-id="08e40-128">Requirement</span></span> | <span data-ttu-id="08e40-129">Значение</span><span class="sxs-lookup"><span data-stu-id="08e40-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e40-130">Header</span><span class="sxs-lookup"><span data-stu-id="08e40-130">Header</span></span><br/>  | <dl> <span data-ttu-id="08e40-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="08e40-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="08e40-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="08e40-132">Library</span></span><br/> | <dl> <span data-ttu-id="08e40-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08e40-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="08e40-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08e40-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e40-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="08e40-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="08e40-136">**ID3DXConstantTable:: DESC**</span><span class="sxs-lookup"><span data-stu-id="08e40-136">**ID3DXConstantTable::GetDesc**</span></span>](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
