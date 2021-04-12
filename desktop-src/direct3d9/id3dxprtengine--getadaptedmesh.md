---
description: Возвращает сетку с изменениями, полученными из адаптивной пространственной выборки. Возвращаемая сетка содержит только позиции, нормали и координаты текстуры (если они определены).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'Метод ID3DXPRTEngine:: Жетадаптедмеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d012344a5dfbc1bc17780cb4ab9a53820fe34f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355693"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a><span data-ttu-id="aeda3-104">Метод ID3DXPRTEngine:: Жетадаптедмеш</span><span class="sxs-lookup"><span data-stu-id="aeda3-104">ID3DXPRTEngine::GetAdaptedMesh method</span></span>

<span data-ttu-id="aeda3-105">Возвращает сетку с изменениями, полученными из адаптивной пространственной выборки.</span><span class="sxs-lookup"><span data-stu-id="aeda3-105">Returns a mesh with modifications resulting from adaptive spatial sampling.</span></span> <span data-ttu-id="aeda3-106">Возвращаемая сетка содержит только позиции, нормали и координаты текстуры (если они определены).</span><span class="sxs-lookup"><span data-stu-id="aeda3-106">The returned mesh contains only positions, normals, and texture coordinates (if defined).</span></span>

## <a name="syntax"></a><span data-ttu-id="aeda3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aeda3-107">Syntax</span></span>


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="aeda3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aeda3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeda3-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aeda3-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeda3-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="aeda3-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="aeda3-111">Указатель на устройство [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , которое используется для создания выходной сетки.</span><span class="sxs-lookup"><span data-stu-id="aeda3-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="aeda3-112">*пфацеремап* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="aeda3-112">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeda3-113">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="aeda3-113">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aeda3-114">Указатель на исходную сетчатую линию, разделенную для создания текущего лица.</span><span class="sxs-lookup"><span data-stu-id="aeda3-114">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> <dt>

<span data-ttu-id="aeda3-115">*пвертремап* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="aeda3-115">*pVertRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeda3-116">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="aeda3-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aeda3-117">Указатель на массив назначения, содержащий три исходные вершины сетки, являющиеся родителями текущей вершины.</span><span class="sxs-lookup"><span data-stu-id="aeda3-117">Pointer to a destination array containing the three original mesh vertices that are the parents of the current vertex.</span></span>

</dd> <dt>

<span data-ttu-id="aeda3-118">*пфвертвеигхтс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="aeda3-118">*pfVertWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeda3-119">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="aeda3-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aeda3-120">Указатель на массив назначения, содержащий коэффициенты смешения для вершин Пвертремап.</span><span class="sxs-lookup"><span data-stu-id="aeda3-120">Pointer to a destination array containing blending factors for the pVertRemap vertices.</span></span>

</dd> <dt>

<span data-ttu-id="aeda3-121">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aeda3-121">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeda3-122">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="aeda3-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="aeda3-123">Указатель на выходной объект сетки [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="aeda3-123">Pointer to the output [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeda3-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aeda3-124">Return value</span></span>

<span data-ttu-id="aeda3-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aeda3-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aeda3-126">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="aeda3-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="aeda3-127">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="aeda3-127">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="aeda3-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aeda3-128">Remarks</span></span>

<span data-ttu-id="aeda3-129">Пвертремап и Пфвертвеигхтс можно использовать для интерполяции любого значения на вершину по сети.</span><span class="sxs-lookup"><span data-stu-id="aeda3-129">pVertRemap and pfVertWeights can be used to interpolate any per-vertex value over the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeda3-130">Требования</span><span class="sxs-lookup"><span data-stu-id="aeda3-130">Requirements</span></span>



| <span data-ttu-id="aeda3-131">Требование</span><span class="sxs-lookup"><span data-stu-id="aeda3-131">Requirement</span></span> | <span data-ttu-id="aeda3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="aeda3-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeda3-133">Header</span><span class="sxs-lookup"><span data-stu-id="aeda3-133">Header</span></span><br/>  | <dl> <span data-ttu-id="aeda3-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeda3-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="aeda3-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aeda3-135">Library</span></span><br/> | <dl> <span data-ttu-id="aeda3-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aeda3-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aeda3-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aeda3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeda3-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="aeda3-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
