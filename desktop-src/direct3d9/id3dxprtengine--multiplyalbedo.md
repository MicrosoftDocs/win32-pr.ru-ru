---
description: Умножает каждый предварительно вычисленный вектор радианценой пересылки (PRT) на вершину албедо.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'Метод ID3DXPRTEngine:: Мултиплялбедо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703955"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a><span data-ttu-id="a6056-103">Метод ID3DXPRTEngine:: Мултиплялбедо</span><span class="sxs-lookup"><span data-stu-id="a6056-103">ID3DXPRTEngine::MultiplyAlbedo method</span></span>

<span data-ttu-id="a6056-104">Умножает каждый предварительно вычисленный вектор радианценой пересылки (PRT) на вершину албедо.</span><span class="sxs-lookup"><span data-stu-id="a6056-104">Multiplies each precomputed radiance transfer (PRT) vector by the per-vertex albedo.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6056-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6056-105">Syntax</span></span>


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="a6056-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6056-107">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a6056-107">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6056-108">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a6056-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a6056-109">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который будет содержать ВЕКТОРы PRT, умноженные на албедо вершины.</span><span class="sxs-lookup"><span data-stu-id="a6056-109">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will contain PRT vectors multiplied by the per-vertex albedo.</span></span> <span data-ttu-id="a6056-110">Если этот выходной буфер является объектом текстуры, необходимо соблюдать осторожность, чтобы сохранить албедо текстуры в том же разрешении, что и буфер имитации.</span><span class="sxs-lookup"><span data-stu-id="a6056-110">If this output buffer is a texture object, then care must be taken to store the albedo of the texture at the same resolution as the simulation buffer.</span></span> <span data-ttu-id="a6056-111">Вы можете задать правильное разрешение для албедо с [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), применяя области для переплета текстур, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="a6056-111">You can set the proper resolution on the albedo with [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), applying texture gutter regions if appropriate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6056-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6056-112">Return value</span></span>

<span data-ttu-id="a6056-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6056-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6056-114">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="a6056-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a6056-115">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a6056-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6056-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6056-116">Remarks</span></span>

<span data-ttu-id="a6056-117">Методы ID3DXPRTEngine:: Компутекскскс вычисляют выходные буферы, в которых сигнал освещения не умножается на албедо.</span><span class="sxs-lookup"><span data-stu-id="a6056-117">The ID3DXPRTEngine::Computexxx methods compute output buffers in which the light signal has not been multiplied by albedo.</span></span> <span data-ttu-id="a6056-118">Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.</span><span class="sxs-lookup"><span data-stu-id="a6056-118">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="a6056-119">Чтобы включить албедо в модель, подготовленную к просмотру, вызовите этот метод после одного из методов Компутекскскс.</span><span class="sxs-lookup"><span data-stu-id="a6056-119">To include albedo in the rendered-light model, call this method after one of the Computexxx methods.</span></span>

<span data-ttu-id="a6056-120">Перед вызовом этого метода необходимо вызвать [**ID3DXPRTEngine:: сетмешматериалс**](id3dxprtengine--setmeshmaterials.md) .</span><span class="sxs-lookup"><span data-stu-id="a6056-120">[**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) should be called before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6056-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a6056-121">Requirements</span></span>



| <span data-ttu-id="a6056-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a6056-122">Requirement</span></span> | <span data-ttu-id="a6056-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a6056-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6056-124">Header</span><span class="sxs-lookup"><span data-stu-id="a6056-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a6056-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6056-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a6056-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a6056-126">Library</span></span><br/> | <dl> <span data-ttu-id="a6056-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6056-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a6056-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6056-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6056-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a6056-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="a6056-130">**ID3DXPRTEngine:: Компутедиректлигхтингш**</span><span class="sxs-lookup"><span data-stu-id="a6056-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




