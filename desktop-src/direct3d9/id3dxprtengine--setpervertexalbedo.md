---
description: Задает значение албедо для каждой вершины сетки, перезаписывая предыдущие значения албедо.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'Метод ID3DXPRTEngine:: Сетпервертексалбедо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647855"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a><span data-ttu-id="b4552-103">Метод ID3DXPRTEngine:: Сетпервертексалбедо</span><span class="sxs-lookup"><span data-stu-id="b4552-103">ID3DXPRTEngine::SetPerVertexAlbedo method</span></span>

<span data-ttu-id="b4552-104">Задает значение албедо для каждой вершины сетки, перезаписывая предыдущие значения албедо.</span><span class="sxs-lookup"><span data-stu-id="b4552-104">Sets an albedo value for each mesh vertex, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4552-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4552-105">Syntax</span></span>


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a><span data-ttu-id="b4552-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4552-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4552-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4552-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4552-108">Тип: **константа \* void**</span><span class="sxs-lookup"><span data-stu-id="b4552-108">Type: **const VOID\***</span></span>

<span data-ttu-id="b4552-109">Указатель на данные типа FLOAT албедо первого образца.</span><span class="sxs-lookup"><span data-stu-id="b4552-109">Pointer to FLOAT albedo data of the first sample.</span></span>

</dd> <dt>

<span data-ttu-id="b4552-110">*Нумчаннелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4552-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4552-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4552-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4552-112">Число устанавливаемых цветовых каналов.</span><span class="sxs-lookup"><span data-stu-id="b4552-112">Number of color channels to set.</span></span> <span data-ttu-id="b4552-113">Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные.</span><span class="sxs-lookup"><span data-stu-id="b4552-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="b4552-114">*Шаг с шагом* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4552-114">*Stride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4552-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4552-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4552-116">Шаг в байтах, необходимый для перехода к значению албедо следующей выборки.</span><span class="sxs-lookup"><span data-stu-id="b4552-116">Stride in bytes needed to get to next sample's albedo value.</span></span> <span data-ttu-id="b4552-117">См. раздел [Ширина и шаг (Direct3D 9)](width-vs--pitch.md).</span><span class="sxs-lookup"><span data-stu-id="b4552-117">See [Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4552-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4552-118">Return value</span></span>

<span data-ttu-id="b4552-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4552-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4552-120">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="b4552-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b4552-121">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b4552-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4552-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b4552-122">Requirements</span></span>



| <span data-ttu-id="b4552-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b4552-123">Requirement</span></span> | <span data-ttu-id="b4552-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b4552-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4552-125">Header</span><span class="sxs-lookup"><span data-stu-id="b4552-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b4552-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4552-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b4552-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4552-127">Library</span></span><br/> | <dl> <span data-ttu-id="b4552-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4552-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b4552-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4552-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4552-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b4552-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
