---
description: Запрашивает выделение объекта контейнера сетки.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'Метод ID3DXAllocateHierarchy:: Креатемешконтаинер (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694086"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a><span data-ttu-id="2c122-103">Метод ID3DXAllocateHierarchy:: Креатемешконтаинер</span><span class="sxs-lookup"><span data-stu-id="2c122-103">ID3DXAllocateHierarchy::CreateMeshContainer method</span></span>

<span data-ttu-id="2c122-104">Запрашивает выделение объекта контейнера сетки.</span><span class="sxs-lookup"><span data-stu-id="2c122-104">Requests allocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c122-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c122-105">Syntax</span></span>


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a><span data-ttu-id="2c122-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c122-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c122-107">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c122-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c122-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c122-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c122-109">Имя сетки.</span><span class="sxs-lookup"><span data-stu-id="2c122-109">Name of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2c122-110">*пмешдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c122-110">*pMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c122-111">Тип: **const [**D3DXMESHDATA**](d3dxmeshdata.md) \***</span><span class="sxs-lookup"><span data-stu-id="2c122-111">Type: **const [**D3DXMESHDATA**](d3dxmeshdata.md)\***</span></span>

<span data-ttu-id="2c122-112">Указатель на структуру данных сетки.</span><span class="sxs-lookup"><span data-stu-id="2c122-112">Pointer to the mesh data structure.</span></span> <span data-ttu-id="2c122-113">См. [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="2c122-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c122-114">*пматериалс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c122-114">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c122-115">Тип: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="2c122-115">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="2c122-116">Массив материалов, используемых в сетке.</span><span class="sxs-lookup"><span data-stu-id="2c122-116">Array of materials used in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2c122-117">*пеффектинстанцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c122-117">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c122-118">Тип: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="2c122-118">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="2c122-119">Массив экземпляров эффектов, используемых в сетке.</span><span class="sxs-lookup"><span data-stu-id="2c122-119">Array of effect instances used in the mesh.</span></span> <span data-ttu-id="2c122-120">См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="2c122-120">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c122-121">*Нумматериалс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c122-121">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c122-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c122-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c122-123">Количество материалов в массиве материалов.</span><span class="sxs-lookup"><span data-stu-id="2c122-123">Number of materials in the materials array.</span></span>

</dd> <dt>

<span data-ttu-id="2c122-124">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c122-124">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c122-125">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2c122-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2c122-126">Массив соседей для сетки.</span><span class="sxs-lookup"><span data-stu-id="2c122-126">Adjacency array for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2c122-127">*пскининфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c122-127">*pSkinInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c122-128">Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="2c122-128">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

<span data-ttu-id="2c122-129">Указатель на объект сетки обложки, если обнаружены данные обложки.</span><span class="sxs-lookup"><span data-stu-id="2c122-129">Pointer to the skin mesh object if skin data is found.</span></span> <span data-ttu-id="2c122-130">См. [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="2c122-130">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c122-131">*ппневмешконтаинер* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2c122-131">*ppNewMeshContainer* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2c122-132">Тип: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c122-132">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="2c122-133">Возвращает созданный контейнер сетки.</span><span class="sxs-lookup"><span data-stu-id="2c122-133">Returns the created mesh container.</span></span> <span data-ttu-id="2c122-134">См. [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="2c122-134">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c122-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c122-135">Return value</span></span>

<span data-ttu-id="2c122-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c122-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c122-137">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="2c122-137">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="2c122-138">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2c122-138">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="2c122-139">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от D3DERR или D3DXERR, так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="2c122-139">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c122-140">Требования</span><span class="sxs-lookup"><span data-stu-id="2c122-140">Requirements</span></span>



| <span data-ttu-id="2c122-141">Требование</span><span class="sxs-lookup"><span data-stu-id="2c122-141">Requirement</span></span> | <span data-ttu-id="2c122-142">Значение</span><span class="sxs-lookup"><span data-stu-id="2c122-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c122-143">Header</span><span class="sxs-lookup"><span data-stu-id="2c122-143">Header</span></span><br/>  | <dl> <span data-ttu-id="2c122-144"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c122-144"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2c122-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c122-145">Library</span></span><br/> | <dl> <span data-ttu-id="2c122-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c122-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2c122-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c122-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c122-148">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="2c122-148">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
