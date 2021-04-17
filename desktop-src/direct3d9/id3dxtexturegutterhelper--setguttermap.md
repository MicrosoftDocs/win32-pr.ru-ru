---
description: Задает значение класса шаг текселя, указывающее класс шаг текселя в соответствии с расположением каждого шаг текселя.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'Метод ID3DXTextureGutterHelper:: Сетгуттермап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703941"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a><span data-ttu-id="8edc2-103">Метод ID3DXTextureGutterHelper:: Сетгуттермап</span><span class="sxs-lookup"><span data-stu-id="8edc2-103">ID3DXTextureGutterHelper::SetGutterMap method</span></span>

<span data-ttu-id="8edc2-104">Задает значение класса шаг текселя, указывающее класс шаг текселя в соответствии с расположением каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="8edc2-104">Sets a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="8edc2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8edc2-105">Syntax</span></span>


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="8edc2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8edc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8edc2-107">*пгуттердата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8edc2-107">*pGutterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8edc2-108">Тип: **[ **Byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8edc2-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8edc2-109">Указатель на класс шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="8edc2-109">Pointer to the texel class.</span></span> <span data-ttu-id="8edc2-110">Возможны следующие классы шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="8edc2-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="8edc2-111">Отсутствует класс шаг текселя 3.</span><span class="sxs-lookup"><span data-stu-id="8edc2-111">There is no texel class 3.</span></span>



| <span data-ttu-id="8edc2-112">Класс шаг текселя</span><span class="sxs-lookup"><span data-stu-id="8edc2-112">Texel Class</span></span> | <span data-ttu-id="8edc2-113">Расположение шаг текселя</span><span class="sxs-lookup"><span data-stu-id="8edc2-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8edc2-114">0</span><span class="sxs-lookup"><span data-stu-id="8edc2-114">0</span></span>           | <span data-ttu-id="8edc2-115">Недопустимая точка; шаг текселя не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="8edc2-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8edc2-116">1</span><span class="sxs-lookup"><span data-stu-id="8edc2-116">1</span></span>           | <span data-ttu-id="8edc2-117">Внутри треугольника.</span><span class="sxs-lookup"><span data-stu-id="8edc2-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8edc2-118">2</span><span class="sxs-lookup"><span data-stu-id="8edc2-118">2</span></span>           | <span data-ttu-id="8edc2-119">Внутренняя часть.</span><span class="sxs-lookup"><span data-stu-id="8edc2-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8edc2-120">4</span><span class="sxs-lookup"><span data-stu-id="8edc2-120">4</span></span>           | <span data-ttu-id="8edc2-121">Внутреннее внутреннее поле; шаг текселя будет оцениваться как полный пример в методах [**ID3DXTextureGutterHelper:: апплигуттерсфлоат**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: апплигуттерстекс**](id3dxtexturegutterhelper--applygutterstex.md)или [**ID3DXTextureGutterHelper:: апплигуттерспрт**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="8edc2-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8edc2-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8edc2-122">Return value</span></span>

<span data-ttu-id="8edc2-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8edc2-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8edc2-124">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="8edc2-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8edc2-125">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="8edc2-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="8edc2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8edc2-126">Requirements</span></span>



| <span data-ttu-id="8edc2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8edc2-127">Requirement</span></span> | <span data-ttu-id="8edc2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8edc2-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8edc2-129">Header</span><span class="sxs-lookup"><span data-stu-id="8edc2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8edc2-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8edc2-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8edc2-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8edc2-131">Library</span></span><br/> | <dl> <span data-ttu-id="8edc2-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8edc2-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8edc2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8edc2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8edc2-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="8edc2-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
