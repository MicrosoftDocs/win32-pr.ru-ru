---
title: Функция D3DX11SHProjectCubeMap (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать математическую библиотеку "сферические гармонические колебания", Шпрожекткубемап.
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- D3DX11SHProjectCubeMap функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998495"
---
# <a name="d3dx11shprojectcubemap-function"></a><span data-ttu-id="ee642-105">Функция D3DX11SHProjectCubeMap</span><span class="sxs-lookup"><span data-stu-id="ee642-105">D3DX11SHProjectCubeMap function</span></span>

> [!Note]  
> <span data-ttu-id="ee642-106">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="ee642-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="ee642-107">Вместо использования этой функции рекомендуется использовать [математическую библиотеку "сферические гармонические колебания](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) ", **шпрожекткубемап**.</span><span class="sxs-lookup"><span data-stu-id="ee642-107">Instead of using this function, we recommend that you use the [Spherical Harmonics Math](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) library, **SHProjectCubeMap**.</span></span>

 

<span data-ttu-id="ee642-108">Проецирует функцию, представленную в сопоставлении кубов, в сферические гармонические колебания.</span><span class="sxs-lookup"><span data-stu-id="ee642-108">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee642-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee642-109">Syntax</span></span>


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="ee642-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee642-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee642-111">*pContext*</span><span class="sxs-lookup"><span data-stu-id="ee642-111">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="ee642-112">Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="ee642-112">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="ee642-113">Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="ee642-113">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="ee642-114">*Заказ*</span><span class="sxs-lookup"><span data-stu-id="ee642-114">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="ee642-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ee642-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ee642-116">В порядке вычисления SH формирует коэффициенты в заказе ^ 2, степень которых — Order-1.</span><span class="sxs-lookup"><span data-stu-id="ee642-116">Order of the SH evaluation, generates Order^2 coefficients whose degree is Order-1.</span></span> <span data-ttu-id="ee642-117">Допустимый диапазон: от 2 до 6.</span><span class="sxs-lookup"><span data-stu-id="ee642-117">Valid range is between 2 and 6.</span></span>

</dd> <dt>

<span data-ttu-id="ee642-118">*пкубемап*</span><span class="sxs-lookup"><span data-stu-id="ee642-118">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="ee642-119">Тип: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="ee642-119">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="ee642-120">Указатель на [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , представляющий кубической карты, который планируется спроецировать на сферические гармонические колебания.</span><span class="sxs-lookup"><span data-stu-id="ee642-120">A pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) that represents a cubemap that is going to be projected into spherical harmonics.</span></span>

</dd> <dt>

<span data-ttu-id="ee642-121">*праут*</span><span class="sxs-lookup"><span data-stu-id="ee642-121">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="ee642-122">Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="ee642-122">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="ee642-123">Выходной вектор SH для Red.</span><span class="sxs-lookup"><span data-stu-id="ee642-123">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="ee642-124">*пгаут*</span><span class="sxs-lookup"><span data-stu-id="ee642-124">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="ee642-125">Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="ee642-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="ee642-126">Выходной вектор SH для зеленого цвета.</span><span class="sxs-lookup"><span data-stu-id="ee642-126">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="ee642-127">*пбаут*</span><span class="sxs-lookup"><span data-stu-id="ee642-127">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="ee642-128">Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="ee642-128">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="ee642-129">Выходной вектор SH для синего.</span><span class="sxs-lookup"><span data-stu-id="ee642-129">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee642-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee642-130">Return value</span></span>

<span data-ttu-id="ee642-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee642-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee642-132">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ee642-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee642-133">Требования</span><span class="sxs-lookup"><span data-stu-id="ee642-133">Requirements</span></span>



| <span data-ttu-id="ee642-134">Требование</span><span class="sxs-lookup"><span data-stu-id="ee642-134">Requirement</span></span> | <span data-ttu-id="ee642-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ee642-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee642-136">Header</span><span class="sxs-lookup"><span data-stu-id="ee642-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ee642-137"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee642-137"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ee642-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee642-138">Library</span></span><br/> | <dl> <span data-ttu-id="ee642-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee642-139"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ee642-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee642-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee642-141">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="ee642-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

