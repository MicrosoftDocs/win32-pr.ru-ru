---
description: Задает стандартный вектор для каждого шаг текселя в объекте текстуры. Этот метод используется для хранения векторов нормали вершин из сетки (или интерполяции нормалей вершин, если выполняется вычисление предварительно вычисленных радианце передаваемых данных (PRT) на основе пикселя).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'Метод ID3DXPRTEngine:: Сетпертекселнормал (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424433"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a><span data-ttu-id="d0acd-104">Метод ID3DXPRTEngine:: Сетпертекселнормал</span><span class="sxs-lookup"><span data-stu-id="d0acd-104">ID3DXPRTEngine::SetPerTexelNormal method</span></span>

<span data-ttu-id="d0acd-105">Задает стандартный вектор для каждого шаг текселя в объекте текстуры.</span><span class="sxs-lookup"><span data-stu-id="d0acd-105">Sets a normal vector for each texel in a texture object.</span></span> <span data-ttu-id="d0acd-106">Этот метод используется для хранения векторов нормали вершин из сетки (или интерполяции нормалей вершин, если выполняется вычисление предварительно вычисленных радианце передаваемых данных (PRT) на основе пикселя).</span><span class="sxs-lookup"><span data-stu-id="d0acd-106">This method is used to store vertex normal vectors from a mesh (or interpolated vertex normals if pixel-based precomputed radiance transfer (PRT) is being computed).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0acd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0acd-107">Syntax</span></span>


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a><span data-ttu-id="d0acd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0acd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0acd-109">*пнормалтекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0acd-109">*pNormalTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0acd-110">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="d0acd-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="d0acd-111">Указатель на объект текстуры [**IDirect3DTexture9**](/windows/desktop/api) , который служит в качестве стандартной схемы пространства объектов для хранения обычных векторов.</span><span class="sxs-lookup"><span data-stu-id="d0acd-111">Pointer to an [**IDirect3DTexture9**](/windows/desktop/api) texture object that serves as an object space normal map in which to store normal vectors.</span></span> <span data-ttu-id="d0acd-112">Текстура должна иметь те же размеры, что и [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , и должна иметь возможность хранить подписанные форматы текстуры.</span><span class="sxs-lookup"><span data-stu-id="d0acd-112">The texture must have the same dimensions as [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and must be able to store signed texture formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0acd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0acd-113">Return value</span></span>

<span data-ttu-id="d0acd-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0acd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0acd-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="d0acd-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d0acd-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d0acd-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0acd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d0acd-117">Requirements</span></span>



| <span data-ttu-id="d0acd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d0acd-118">Requirement</span></span> | <span data-ttu-id="d0acd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d0acd-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0acd-120">Header</span><span class="sxs-lookup"><span data-stu-id="d0acd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d0acd-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0acd-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d0acd-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d0acd-122">Library</span></span><br/> | <dl> <span data-ttu-id="d0acd-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0acd-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0acd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0acd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0acd-125">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="d0acd-125">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
