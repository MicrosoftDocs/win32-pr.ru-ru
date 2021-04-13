---
description: Выполняет вычисление исходного радианцеа, полученного на основе одного отскока с переходом. Этот метод можно использовать для любой освещенной сцены, включая модель предварительно вычисленных радианце (PRT) на основе сферического гармонического (SH).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'Метод ID3DXPRTEngine:: Компутебаунце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355703"
---
# <a name="id3dxprtenginecomputebounce-method"></a><span data-ttu-id="8cfe6-104">Метод ID3DXPRTEngine:: Компутебаунце</span><span class="sxs-lookup"><span data-stu-id="8cfe6-104">ID3DXPRTEngine::ComputeBounce method</span></span>

<span data-ttu-id="8cfe6-105">Выполняет вычисление исходного радианцеа, полученного на основе одного отскока с переходом.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-105">Computes the source radiance resulting from a single bounce of interreflected light.</span></span> <span data-ttu-id="8cfe6-106">Этот метод можно использовать для любой освещенной сцены, включая модель предварительно вычисленных радианце (PRT) на основе сферического гармонического (SH).</span><span class="sxs-lookup"><span data-stu-id="8cfe6-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based precomputed radiance transfer (PRT) model.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cfe6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cfe6-107">Syntax</span></span>


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="8cfe6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cfe6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cfe6-109">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cfe6-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfe6-110">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="8cfe6-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="8cfe6-111">Указатель на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , представляющий трехмерный объект из предыдущего освещения.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="8cfe6-112">Этот входной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="8cfe6-113">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8cfe6-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfe6-114">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="8cfe6-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="8cfe6-115">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , моделирующий один элемент отскока на перенаправленном свете.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the interreflected light.</span></span> <span data-ttu-id="8cfe6-116">Этот выходной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="8cfe6-117">*пдататотал* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8cfe6-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfe6-118">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="8cfe6-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="8cfe6-119">Указатель на необязательный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который является выполняющейся суммой всех предыдущих выходов pData.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="8cfe6-120">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cfe6-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cfe6-121">Return value</span></span>

<span data-ttu-id="8cfe6-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cfe6-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cfe6-123">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8cfe6-124">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cfe6-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cfe6-125">Remarks</span></span>

<span data-ttu-id="8cfe6-126">Используйте следующую последовательность вызова, чтобы смоделировать несколько световых отскоков с прямым освещением.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-126">Use the following calling sequence to model multiple light bounces with direct lighting.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



<span data-ttu-id="8cfe6-127">Используйте следующую последовательность вызова, чтобы смоделировать несколько источников падения яркости с помощью геоточечной подповерхности.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-127">Use the following calling sequence to model multiple light bounces with subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



<span data-ttu-id="8cfe6-128">Выходные данные этого метода не включают албедо, и в симуляторе встроена только входящая лампочка.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="8cfe6-129">Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="8cfe6-130">Вызовите метод [**ID3DXPRTEngine:: мултиплялбедо**](id3dxprtengine--multiplyalbedo.md) , чтобы умножить каждый вектор PRT на албедо.</span><span class="sxs-lookup"><span data-stu-id="8cfe6-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfe6-131">Требования</span><span class="sxs-lookup"><span data-stu-id="8cfe6-131">Requirements</span></span>



| <span data-ttu-id="8cfe6-132">Требование</span><span class="sxs-lookup"><span data-stu-id="8cfe6-132">Requirement</span></span> | <span data-ttu-id="8cfe6-133">Значение</span><span class="sxs-lookup"><span data-stu-id="8cfe6-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfe6-134">Header</span><span class="sxs-lookup"><span data-stu-id="8cfe6-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8cfe6-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cfe6-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8cfe6-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8cfe6-136">Library</span></span><br/> | <dl> <span data-ttu-id="8cfe6-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cfe6-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8cfe6-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cfe6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cfe6-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="8cfe6-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="8cfe6-140">**ID3DXPRTEngine:: COMPUTE**</span><span class="sxs-lookup"><span data-stu-id="8cfe6-140">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 




