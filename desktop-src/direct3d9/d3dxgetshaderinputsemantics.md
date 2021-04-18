---
description: Возвращает семантику для входных данных шейдера. Используйте этот метод, чтобы определить формат входной вершины.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: Функция D3DXGetShaderInputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713665"
---
# <a name="d3dxgetshaderinputsemantics-function"></a><span data-ttu-id="39bdf-104">Функция D3DXGetShaderInputSemantics</span><span class="sxs-lookup"><span data-stu-id="39bdf-104">D3DXGetShaderInputSemantics function</span></span>

<span data-ttu-id="39bdf-105">Возвращает семантику для входных данных шейдера.</span><span class="sxs-lookup"><span data-stu-id="39bdf-105">Gets the semantics for the shader inputs.</span></span> <span data-ttu-id="39bdf-106">Используйте этот метод, чтобы определить формат входной вершины.</span><span class="sxs-lookup"><span data-stu-id="39bdf-106">Use this method to determine the input vertex format.</span></span>

## <a name="syntax"></a><span data-ttu-id="39bdf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39bdf-107">Syntax</span></span>


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="39bdf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="39bdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39bdf-109">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39bdf-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39bdf-110">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="39bdf-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="39bdf-111">Указатель на поток функции шейдера DWORD.</span><span class="sxs-lookup"><span data-stu-id="39bdf-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="39bdf-112">*псемантикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39bdf-112">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39bdf-113">Тип: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="39bdf-113">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="39bdf-114">Указатель на массив структур [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="39bdf-114">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="39bdf-115">Функция будет заполнять этот массив семантикой для каждого входного элемента, на который ссылается шейдер.</span><span class="sxs-lookup"><span data-stu-id="39bdf-115">The function will fill this array with the semantics for each input element referenced by the shader.</span></span> <span data-ttu-id="39bdf-116">Предполагается, что этот массив содержит по крайней мере элементы MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="39bdf-116">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="39bdf-117">Однако вызов **D3DXGetShaderInputSemantics** с Псемантикс = **null** возвратит количество элементов, необходимых для pCount.</span><span class="sxs-lookup"><span data-stu-id="39bdf-117">However, calling **D3DXGetShaderInputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="39bdf-118">*pCount* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39bdf-118">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39bdf-119">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="39bdf-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="39bdf-120">Возвращает количество элементов в Псемантикс.</span><span class="sxs-lookup"><span data-stu-id="39bdf-120">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39bdf-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39bdf-121">Return value</span></span>

<span data-ttu-id="39bdf-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39bdf-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39bdf-123">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="39bdf-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="39bdf-124">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="39bdf-124">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="39bdf-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39bdf-125">Remarks</span></span>

<span data-ttu-id="39bdf-126">Используйте **D3DXGetShaderInputSemantics** для возврата списка семантики ввода, необходимой шейдеру.</span><span class="sxs-lookup"><span data-stu-id="39bdf-126">Use **D3DXGetShaderInputSemantics** to return a list of input semantics required by the shader.</span></span> <span data-ttu-id="39bdf-127">Это способ узнать, какой формат входной вершины предназначен для шейдера высокого уровня (HLSL).</span><span class="sxs-lookup"><span data-stu-id="39bdf-127">This is the way to find out what the input vertex format is for a high-level shader language (HLSL) shader.</span></span> <span data-ttu-id="39bdf-128">Если у шейдера есть дополнительные входы, которые отсутствуют в объявлении вершины, можно создать дополнительный поток вершин с шагом 0, в котором отсутствуют компоненты со значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39bdf-128">If the shader has additional inputs that your vertex declaration is missing, you could create an extra vertex stream that has a stride of 0 that has the missing components with default values.</span></span> <span data-ttu-id="39bdf-129">Например, этот метод можно использовать для предоставления цвета вершин по умолчанию для моделей, которые не задают его.</span><span class="sxs-lookup"><span data-stu-id="39bdf-129">For instance, this technique could be used to provide default vertex color for models that do not specify it.</span></span>

## <a name="requirements"></a><span data-ttu-id="39bdf-130">Требования</span><span class="sxs-lookup"><span data-stu-id="39bdf-130">Requirements</span></span>



| <span data-ttu-id="39bdf-131">Требование</span><span class="sxs-lookup"><span data-stu-id="39bdf-131">Requirement</span></span> | <span data-ttu-id="39bdf-132">Значение</span><span class="sxs-lookup"><span data-stu-id="39bdf-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="39bdf-133">Header</span><span class="sxs-lookup"><span data-stu-id="39bdf-133">Header</span></span><br/>  | <dl> <span data-ttu-id="39bdf-134"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="39bdf-134"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="39bdf-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="39bdf-135">Library</span></span><br/> | <dl> <span data-ttu-id="39bdf-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39bdf-136"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="39bdf-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39bdf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39bdf-138">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="39bdf-138">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
