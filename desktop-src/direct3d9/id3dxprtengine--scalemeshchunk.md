---
description: Масштабирует все выборки, связанные с заданной подсетью. Метод полезен для вычисления рассеивания подповерхности.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'Метод ID3DXPRTEngine:: Скалемешчунк (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703953"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a><span data-ttu-id="f2245-104">Метод ID3DXPRTEngine:: Скалемешчунк</span><span class="sxs-lookup"><span data-stu-id="f2245-104">ID3DXPRTEngine::ScaleMeshChunk method</span></span>

<span data-ttu-id="f2245-105">Масштабирует все выборки, связанные с заданной подсетью.</span><span class="sxs-lookup"><span data-stu-id="f2245-105">Scales all the samples associated with a given submesh.</span></span> <span data-ttu-id="f2245-106">Метод полезен для вычисления рассеивания подповерхности.</span><span class="sxs-lookup"><span data-stu-id="f2245-106">The method is useful for computing subsurface scattering.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2245-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2245-107">Syntax</span></span>


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="f2245-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2245-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2245-109">*умешчунк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2245-109">*uMeshChunk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2245-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2245-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2245-111">Расположение в сетке, с которого начинается масштабирование выборок.</span><span class="sxs-lookup"><span data-stu-id="f2245-111">Location in the mesh at which to start scaling samples.</span></span>

</dd> <dt>

<span data-ttu-id="f2245-112">*фскале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2245-112">*fScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2245-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2245-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2245-114">Значение, на которое умножается каждый вектор в подсети.</span><span class="sxs-lookup"><span data-stu-id="f2245-114">Value by which to multiply each vector in the submesh.</span></span>

</dd> <dt>

<span data-ttu-id="f2245-115">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f2245-115">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2245-116">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f2245-116">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f2245-117">Указатель на объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) для получения масштабируемых образцов во вложенной сетке.</span><span class="sxs-lookup"><span data-stu-id="f2245-117">Pointer to a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object to receive rescaled samples in the submesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2245-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2245-118">Return value</span></span>

<span data-ttu-id="f2245-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2245-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2245-120">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="f2245-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f2245-121">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f2245-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2245-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f2245-122">Requirements</span></span>



| <span data-ttu-id="f2245-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f2245-123">Requirement</span></span> | <span data-ttu-id="f2245-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f2245-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2245-125">Header</span><span class="sxs-lookup"><span data-stu-id="f2245-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f2245-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2245-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f2245-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2245-127">Library</span></span><br/> | <dl> <span data-ttu-id="f2245-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2245-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2245-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2245-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2245-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="f2245-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
