---
description: Получает значение класса шаг текселя, которое указывает класс шаг текселя в соответствии с расположением каждого шаг текселя.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'Метод ID3DXTextureGutterHelper:: Жетгуттермап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647853"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a><span data-ttu-id="a022f-103">Метод ID3DXTextureGutterHelper:: Жетгуттермап</span><span class="sxs-lookup"><span data-stu-id="a022f-103">ID3DXTextureGutterHelper::GetGutterMap method</span></span>

<span data-ttu-id="a022f-104">Получает значение класса шаг текселя, которое указывает класс шаг текселя в соответствии с расположением каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="a022f-104">Receives a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="a022f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a022f-105">Syntax</span></span>


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="a022f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a022f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a022f-107">*пгуттердата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a022f-107">*pGutterData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a022f-108">Тип: **[ **Byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a022f-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a022f-109">Указатель на класс шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="a022f-109">Pointer to the texel class.</span></span> <span data-ttu-id="a022f-110">Возможны следующие классы шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="a022f-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="a022f-111">Отсутствует класс шаг текселя 3.</span><span class="sxs-lookup"><span data-stu-id="a022f-111">There is no texel class 3.</span></span>



| <span data-ttu-id="a022f-112">Класс шаг текселя</span><span class="sxs-lookup"><span data-stu-id="a022f-112">Texel Class</span></span> | <span data-ttu-id="a022f-113">Расположение шаг текселя</span><span class="sxs-lookup"><span data-stu-id="a022f-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a022f-114">0</span><span class="sxs-lookup"><span data-stu-id="a022f-114">0</span></span>           | <span data-ttu-id="a022f-115">Недопустимая точка; шаг текселя не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="a022f-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a022f-116">1</span><span class="sxs-lookup"><span data-stu-id="a022f-116">1</span></span>           | <span data-ttu-id="a022f-117">Внутри треугольника.</span><span class="sxs-lookup"><span data-stu-id="a022f-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a022f-118">2</span><span class="sxs-lookup"><span data-stu-id="a022f-118">2</span></span>           | <span data-ttu-id="a022f-119">Внутренняя часть.</span><span class="sxs-lookup"><span data-stu-id="a022f-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a022f-120">4</span><span class="sxs-lookup"><span data-stu-id="a022f-120">4</span></span>           | <span data-ttu-id="a022f-121">Внутреннее внутреннее поле; шаг текселя будет оцениваться как полный пример в методах [**ID3DXTextureGutterHelper:: апплигуттерсфлоат**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: апплигуттерстекс**](id3dxtexturegutterhelper--applygutterstex.md)или [**ID3DXTextureGutterHelper:: апплигуттерспрт**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="a022f-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a022f-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a022f-122">Return value</span></span>

<span data-ttu-id="a022f-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a022f-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a022f-124">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="a022f-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a022f-125">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="a022f-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="a022f-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a022f-126">Remarks</span></span>

<span data-ttu-id="a022f-127">Приложение должно выделить Пгуттердата и управлять им с размером, определенным:</span><span class="sxs-lookup"><span data-stu-id="a022f-127">The application must allocate and manage pGutterData, with size given by:</span></span>


```
texture width * texture height * sizeof(BYTE)
```



<span data-ttu-id="a022f-128">Ширина и высота текстуры возвращаются [**ID3DXTextureGutterHelper:: полуширинные**](id3dxtexturegutterhelper--getwidth.md) и [**ID3DXTextureGutterHelper:: Height**](id3dxtexturegutterhelper--getheight.md).</span><span class="sxs-lookup"><span data-stu-id="a022f-128">Texture width and height are returned by [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) and [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a022f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a022f-129">Requirements</span></span>



| <span data-ttu-id="a022f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a022f-130">Requirement</span></span> | <span data-ttu-id="a022f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a022f-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a022f-132">Header</span><span class="sxs-lookup"><span data-stu-id="a022f-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a022f-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a022f-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a022f-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a022f-134">Library</span></span><br/> | <dl> <span data-ttu-id="a022f-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a022f-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a022f-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a022f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a022f-137">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="a022f-137">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
