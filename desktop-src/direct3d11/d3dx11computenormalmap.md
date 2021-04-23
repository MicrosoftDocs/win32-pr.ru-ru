---
title: Функция D3DX11ComputeNormalMap (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Компутенормалмап.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- D3DX11ComputeNormalMap функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273894"
---
# <a name="d3dx11computenormalmap-function"></a><span data-ttu-id="b2aee-105">Функция D3DX11ComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="b2aee-105">D3DX11ComputeNormalMap function</span></span>

> [!Note]  
> <span data-ttu-id="b2aee-106">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="b2aee-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="b2aee-107">Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **компутенормалмап**.</span><span class="sxs-lookup"><span data-stu-id="b2aee-107">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **ComputeNormalMap**.</span></span>

 

<span data-ttu-id="b2aee-108">Преобразует карту высоты в обычную карту.</span><span class="sxs-lookup"><span data-stu-id="b2aee-108">Converts a height map into a normal map.</span></span> <span data-ttu-id="b2aee-109">Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.</span><span class="sxs-lookup"><span data-stu-id="b2aee-109">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2aee-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2aee-110">Syntax</span></span>


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="b2aee-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2aee-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2aee-112">*пконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2aee-112">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2aee-113">Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="b2aee-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="b2aee-114">Указатель на интерфейс [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) , представляющий текстуру исходной карты с высотой.</span><span class="sxs-lookup"><span data-stu-id="b2aee-114">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="b2aee-115">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2aee-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2aee-116">Тип: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="b2aee-116">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="b2aee-117">Указатель на интерфейс [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , представляющий текстуру исходной карты с высотой.</span><span class="sxs-lookup"><span data-stu-id="b2aee-117">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="b2aee-118">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2aee-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2aee-119">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2aee-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b2aee-120">Один или несколько \_ флагов НОРМАЛМАП D3DX, управляющих созданием обычных карт.</span><span class="sxs-lookup"><span data-stu-id="b2aee-120">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="b2aee-121">*Канал* \[ связи окне\]</span><span class="sxs-lookup"><span data-stu-id="b2aee-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2aee-122">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2aee-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b2aee-123">Один \_ флаг канала D3DX, указывающий источник сведений о высоте.</span><span class="sxs-lookup"><span data-stu-id="b2aee-123">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="b2aee-124">*Амплитуда* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2aee-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2aee-125">Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2aee-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b2aee-126">Коэффициент величины постоянного значения, увеличивающий (или уменьшающий) значения в нормальном сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="b2aee-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="b2aee-127">Более высокие значения обычно делают выпуклости более видимыми, а более низкие значения обычно делают невидимыми более выпуклости.</span><span class="sxs-lookup"><span data-stu-id="b2aee-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="b2aee-128">*пдесттекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2aee-128">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2aee-129">Тип: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="b2aee-129">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="b2aee-130">Указатель на интерфейс [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , представляющий текстуру назначения.</span><span class="sxs-lookup"><span data-stu-id="b2aee-130">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2aee-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2aee-131">Return value</span></span>

<span data-ttu-id="b2aee-132">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2aee-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2aee-133">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b2aee-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2aee-134">Если функция завершается ошибкой, возвращаемое значение может иметь следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b2aee-134">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2aee-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2aee-135">Remarks</span></span>

<span data-ttu-id="b2aee-136">Этот метод рассчитывает нормальную работу, используя Центральное различие с размером ядра 3X3.</span><span class="sxs-lookup"><span data-stu-id="b2aee-136">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="b2aee-137">Каналы RGB в назначении содержат смещенные компоненты (x, y, z) нормали.</span><span class="sxs-lookup"><span data-stu-id="b2aee-137">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="b2aee-138">Центральный разностный знаменатель жестко закодирован в 2,0.</span><span class="sxs-lookup"><span data-stu-id="b2aee-138">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2aee-139">Требования</span><span class="sxs-lookup"><span data-stu-id="b2aee-139">Requirements</span></span>



| <span data-ttu-id="b2aee-140">Требование</span><span class="sxs-lookup"><span data-stu-id="b2aee-140">Requirement</span></span> | <span data-ttu-id="b2aee-141">Значение</span><span class="sxs-lookup"><span data-stu-id="b2aee-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2aee-142">Header</span><span class="sxs-lookup"><span data-stu-id="b2aee-142">Header</span></span><br/>  | <dl> <span data-ttu-id="b2aee-143"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2aee-143"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b2aee-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b2aee-144">Library</span></span><br/> | <dl> <span data-ttu-id="b2aee-145"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2aee-145"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b2aee-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2aee-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2aee-147">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="b2aee-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

