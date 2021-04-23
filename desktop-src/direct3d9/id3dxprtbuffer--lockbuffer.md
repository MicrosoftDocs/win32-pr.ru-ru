---
description: Блокирует диапазон демонстрационных данных вершин или шаг текселя и получает указатель на расположение в буферной памяти.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'Метод ID3DXPRTBuffer:: Локкбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2da8cb5a6a2e036fb7b495a129a5ef29d9ff749
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694217"
---
# <a name="id3dxprtbufferlockbuffer-method"></a><span data-ttu-id="cb5e6-103">Метод ID3DXPRTBuffer:: Локкбуффер</span><span class="sxs-lookup"><span data-stu-id="cb5e6-103">ID3DXPRTBuffer::LockBuffer method</span></span>

<span data-ttu-id="cb5e6-104">Блокирует диапазон демонстрационных данных вершин или шаг текселя и получает указатель на расположение в буферной памяти.</span><span class="sxs-lookup"><span data-stu-id="cb5e6-104">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb5e6-105">Syntax</span></span>


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="cb5e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb5e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb5e6-107">*Запуск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb5e6-107">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5e6-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb5e6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb5e6-109">Индекс образца данных вершины или шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="cb5e6-109">Index of the sample of vertex or texel data.</span></span>

</dd> <dt>

<span data-ttu-id="cb5e6-110">*Нумсамплес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb5e6-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5e6-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb5e6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb5e6-112">Количество вершин (или пикселей текстуры) с выборкой.</span><span class="sxs-lookup"><span data-stu-id="cb5e6-112">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="cb5e6-113">*ппдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb5e6-113">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5e6-114">Тип: **[ **float**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cb5e6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="cb5e6-115">Указатель на расположение в памяти, где начинается начальная выборка.</span><span class="sxs-lookup"><span data-stu-id="cb5e6-115">Pointer to the location in memory where the Start sample begins.</span></span> <span data-ttu-id="cb5e6-116">Макет памяти данных буфера:</span><span class="sxs-lookup"><span data-stu-id="cb5e6-116">The memory layout of the buffer data is:</span></span>


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb5e6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb5e6-117">Return value</span></span>

<span data-ttu-id="cb5e6-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb5e6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb5e6-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="cb5e6-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cb5e6-120">Если метод завершается с ошибкой, будет возвращено следующее значение:</span><span class="sxs-lookup"><span data-stu-id="cb5e6-120">If the method fails, the following value will be returned:</span></span>

## <a name="remarks"></a><span data-ttu-id="cb5e6-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="cb5e6-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cb5e6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="cb5e6-122">Requirements</span></span>



| <span data-ttu-id="cb5e6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="cb5e6-123">Requirement</span></span> | <span data-ttu-id="cb5e6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cb5e6-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5e6-125">Header</span><span class="sxs-lookup"><span data-stu-id="cb5e6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cb5e6-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb5e6-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cb5e6-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb5e6-127">Library</span></span><br/> | <dl> <span data-ttu-id="cb5e6-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb5e6-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cb5e6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb5e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5e6-130">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="cb5e6-130">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="cb5e6-131">**ID3DXPRTBuffer:: Жетнумчаннелс**</span><span class="sxs-lookup"><span data-stu-id="cb5e6-131">**ID3DXPRTBuffer::GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[<span data-ttu-id="cb5e6-132">**ID3DXPRTBuffer:: Жетнумкоеффс**</span><span class="sxs-lookup"><span data-stu-id="cb5e6-132">**ID3DXPRTBuffer::GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[<span data-ttu-id="cb5e6-133">**ID3DXPRTBuffer:: Жетнумсамплес**</span><span class="sxs-lookup"><span data-stu-id="cb5e6-133">**ID3DXPRTBuffer::GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
