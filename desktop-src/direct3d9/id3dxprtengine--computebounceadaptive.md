---
description: Выполняет вычисление исходного радианцеа, полученного на основе одного отскока с переходом на использование адаптивной выборки.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'Метод ID3DXPRTEngine:: Компутебаунцеадаптиве (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 787dee9719e0450dd39ebb19f4c06ee76013cb07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703970"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a><span data-ttu-id="095dc-103">Метод ID3DXPRTEngine:: Компутебаунцеадаптиве</span><span class="sxs-lookup"><span data-stu-id="095dc-103">ID3DXPRTEngine::ComputeBounceAdaptive method</span></span>

<span data-ttu-id="095dc-104">Выполняет вычисление исходного радианцеа, полученного на основе одного отскока с переходом на использование адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="095dc-104">Computes the source radiance resulting from a single bounce of interreflected light, using adaptive sampling.</span></span> <span data-ttu-id="095dc-105">Этот метод создает новые вершины и грани в сети для более точного приближения к предварительно вычисленному сигналу передачи радианце (PRT).</span><span class="sxs-lookup"><span data-stu-id="095dc-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="095dc-106">Этот метод можно использовать для любой освещенной сцены, включая модель PRT на основе сферического гармонического (SH).</span><span class="sxs-lookup"><span data-stu-id="095dc-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based PRT model.</span></span>

## <a name="syntax"></a><span data-ttu-id="095dc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="095dc-107">Syntax</span></span>


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="095dc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="095dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="095dc-109">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="095dc-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095dc-110">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="095dc-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="095dc-111">Указатель на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , представляющий трехмерный объект из предыдущего освещения.</span><span class="sxs-lookup"><span data-stu-id="095dc-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="095dc-112">Этот входной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.</span><span class="sxs-lookup"><span data-stu-id="095dc-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="095dc-113">*Адаптивесреш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="095dc-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095dc-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="095dc-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="095dc-115">Пороговое значение для вектора PRT, используемого для подразделения вершин сетки и граней.</span><span class="sxs-lookup"><span data-stu-id="095dc-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="095dc-116">Если значение параметра меньше 1E-6F, то указывается по умолчанию параметр 1E-6f.</span><span class="sxs-lookup"><span data-stu-id="095dc-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="095dc-117">*Минеджеленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="095dc-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095dc-118">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="095dc-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="095dc-119">Минимальная длина грани, которая будет создана при адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="095dc-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="095dc-120">Если метод определяет, что значение слишком мало, задается зависящее от модели значение.</span><span class="sxs-lookup"><span data-stu-id="095dc-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="095dc-121">При нулевом значении указывается значение по умолчанию 4.</span><span class="sxs-lookup"><span data-stu-id="095dc-121">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="095dc-122">*Макссубдив* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="095dc-122">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095dc-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="095dc-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="095dc-124">Максимальный уровень подраздела лица, который будет использоваться в адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="095dc-124">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="095dc-125">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="095dc-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="095dc-126">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="095dc-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="095dc-127">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="095dc-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="095dc-128">Этот выходной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.</span><span class="sxs-lookup"><span data-stu-id="095dc-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="095dc-129">*пдататотал* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="095dc-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="095dc-130">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="095dc-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="095dc-131">Указатель на необязательный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , сохраняющий сумму pData с каждым светло-возвратным вычислением.</span><span class="sxs-lookup"><span data-stu-id="095dc-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that keeps a running sum of pDataOut with each light bounce computation.</span></span> <span data-ttu-id="095dc-132">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="095dc-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="095dc-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="095dc-133">Return value</span></span>

<span data-ttu-id="095dc-134">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="095dc-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="095dc-135">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="095dc-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="095dc-136">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="095dc-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="095dc-137">Требования</span><span class="sxs-lookup"><span data-stu-id="095dc-137">Requirements</span></span>



| <span data-ttu-id="095dc-138">Требование</span><span class="sxs-lookup"><span data-stu-id="095dc-138">Requirement</span></span> | <span data-ttu-id="095dc-139">Значение</span><span class="sxs-lookup"><span data-stu-id="095dc-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="095dc-140">Header</span><span class="sxs-lookup"><span data-stu-id="095dc-140">Header</span></span><br/>  | <dl> <span data-ttu-id="095dc-141"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="095dc-141"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="095dc-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="095dc-142">Library</span></span><br/> | <dl> <span data-ttu-id="095dc-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="095dc-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="095dc-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="095dc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095dc-145">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="095dc-145">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="095dc-146">**ID3DXPRTEngine:: Робустмешрефине**</span><span class="sxs-lookup"><span data-stu-id="095dc-146">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
