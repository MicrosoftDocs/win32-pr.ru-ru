---
description: Интерфейс ID3DXPRTCompBuffer хранит сжатую версию буфера ID3DXPRTBuffer для использования с анализом основных компонентов (PCA).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Интерфейс ID3DXPRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703972"
---
# <a name="id3dxprtcompbuffer-interface"></a><span data-ttu-id="7fa68-103">Интерфейс ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="7fa68-103">ID3DXPRTCompBuffer interface</span></span>

<span data-ttu-id="7fa68-104">Интерфейс **ID3DXPRTCompBuffer** хранит сжатую версию буфера [**ID3DXPRTBuffer**](id3dxprtbuffer.md) для использования с анализом основных компонентов (PCA).</span><span class="sxs-lookup"><span data-stu-id="7fa68-104">The **ID3DXPRTCompBuffer** interface stores a compressed version of a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer, for use with principal component analysis (PCA).</span></span>

## <a name="members"></a><span data-ttu-id="7fa68-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="7fa68-105">Members</span></span>

<span data-ttu-id="7fa68-106">Интерфейс **ID3DXPRTCompBuffer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7fa68-106">The **ID3DXPRTCompBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7fa68-107">**ID3DXPRTCompBuffer** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7fa68-107">**ID3DXPRTCompBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="7fa68-108">Методы</span><span class="sxs-lookup"><span data-stu-id="7fa68-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7fa68-109">Методы</span><span class="sxs-lookup"><span data-stu-id="7fa68-109">Methods</span></span>

<span data-ttu-id="7fa68-110">Интерфейс **ID3DXPRTCompBuffer** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7fa68-110">The **ID3DXPRTCompBuffer** interface has these methods.</span></span>



| <span data-ttu-id="7fa68-111">Метод</span><span class="sxs-lookup"><span data-stu-id="7fa68-111">Method</span></span>                                                             | <span data-ttu-id="7fa68-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7fa68-112">Description</span></span>                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fa68-113">**екстрактбасис**</span><span class="sxs-lookup"><span data-stu-id="7fa68-113">**ExtractBasis**</span></span>](id3dxprtcompbuffer--extractbasis.md)           | <span data-ttu-id="7fa68-114">Извлекает средние и абстрактные векторы для заданного кластера из сжатого буфера данных **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="7fa68-114">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                       |
| [<span data-ttu-id="7fa68-115">**екстрактклустеридс**</span><span class="sxs-lookup"><span data-stu-id="7fa68-115">**ExtractClusterIDs**</span></span>](id3dxprtcompbuffer--extractclusterids.md) | <span data-ttu-id="7fa68-116">Извлекает идентификаторы кластеров по образцу из сжатого буфера данных **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="7fa68-116">Extracts the per-sample cluster IDs from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="7fa68-117">**екстрактпка**</span><span class="sxs-lookup"><span data-stu-id="7fa68-117">**ExtractPCA**</span></span>](id3dxprtcompbuffer--extractpca.md)               | <span data-ttu-id="7fa68-118">Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="7fa68-118">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                               |
| [<span data-ttu-id="7fa68-119">**екстракттекстуре**</span><span class="sxs-lookup"><span data-stu-id="7fa68-119">**ExtractTexture**</span></span>](id3dxprtcompbuffer--extracttexture.md)       | <span data-ttu-id="7fa68-120">Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных **ID3DXPRTCompBuffer** и добавляет их в объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="7fa68-120">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="7fa68-121">**екстракттомеш**</span><span class="sxs-lookup"><span data-stu-id="7fa68-121">**ExtractToMesh**</span></span>](id3dxprtcompbuffer--extracttomesh.md)         | <span data-ttu-id="7fa68-122">Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных **ID3DXPRTCompBuffer** и добавляет их в объект [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="7fa68-122">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                 |
| [<span data-ttu-id="7fa68-123">**Высота**</span><span class="sxs-lookup"><span data-stu-id="7fa68-123">**GetHeight**</span></span>](id3dxprtcompbuffer--getheight.md)                 | <span data-ttu-id="7fa68-124">Получает высоту текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7fa68-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="7fa68-125">**жетнумчаннелс**</span><span class="sxs-lookup"><span data-stu-id="7fa68-125">**GetNumChannels**</span></span>](id3dxprtcompbuffer--getnumchannels.md)       | <span data-ttu-id="7fa68-126">Возвращает количество цветовых каналов, используемых в памяти для хранения образцов.</span><span class="sxs-lookup"><span data-stu-id="7fa68-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="7fa68-127">**жетнумклустерс**</span><span class="sxs-lookup"><span data-stu-id="7fa68-127">**GetNumClusters**</span></span>](id3dxprtcompbuffer--getnumclusters.md)       | <span data-ttu-id="7fa68-128">Извлекает количество кластеров, используемых для сжатия.</span><span class="sxs-lookup"><span data-stu-id="7fa68-128">Retrieves the number of clusters to use for compression.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="7fa68-129">**жетнумкоеффс**</span><span class="sxs-lookup"><span data-stu-id="7fa68-129">**GetNumCoeffs**</span></span>](id3dxprtcompbuffer--getnumcoeffs.md)           | <span data-ttu-id="7fa68-130">Возвращает число скаляров на цветовой канал, используемый в памяти для хранения выборок.</span><span class="sxs-lookup"><span data-stu-id="7fa68-130">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="7fa68-131">**жетнумпка**</span><span class="sxs-lookup"><span data-stu-id="7fa68-131">**GetNumPCA**</span></span>](id3dxprtcompbuffer--getnumpca.md)                 | <span data-ttu-id="7fa68-132">Извлекает количество основных векторов анализа компонентов (PCA) для использования в каждом кластере.</span><span class="sxs-lookup"><span data-stu-id="7fa68-132">Retrieves the number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="7fa68-133">**жетнумсамплес**</span><span class="sxs-lookup"><span data-stu-id="7fa68-133">**GetNumSamples**</span></span>](id3dxprtcompbuffer--getnumsamples.md)         | <span data-ttu-id="7fa68-134">Возвращает число вершин (или пикселей текстуры) выборки.</span><span class="sxs-lookup"><span data-stu-id="7fa68-134">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="7fa68-135">**Полуширинные**</span><span class="sxs-lookup"><span data-stu-id="7fa68-135">**GetWidth**</span></span>](id3dxprtcompbuffer--getwidth.md)                   | <span data-ttu-id="7fa68-136">Получает ширину текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7fa68-136">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="7fa68-137">**«Текстурирование»**</span><span class="sxs-lookup"><span data-stu-id="7fa68-137">**IsTexture**</span></span>](id3dxprtcompbuffer--istexture.md)                 | <span data-ttu-id="7fa68-138">Указывает, содержит ли буфер текстуру.</span><span class="sxs-lookup"><span data-stu-id="7fa68-138">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="7fa68-139">**нормализедата**</span><span class="sxs-lookup"><span data-stu-id="7fa68-139">**NormalizeData**</span></span>](id3dxprtcompbuffer--normalizedata.md)         | <span data-ttu-id="7fa68-140">Нормализует все весовые коэффициенты для анализа основных компонентов (PCA), чтобы они были в диапазоне от-1 до 1.</span><span class="sxs-lookup"><span data-stu-id="7fa68-140">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="7fa68-141">Векторы базиса изменяются для отражения этой нормализации.</span><span class="sxs-lookup"><span data-stu-id="7fa68-141">Basis vectors are modified to reflect this normalization.</span></span><br/>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="7fa68-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fa68-142">Remarks</span></span>

<span data-ttu-id="7fa68-143">Интерфейс **ID3DXPRTCompBuffer** получается путем вызова функции [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7fa68-143">The **ID3DXPRTCompBuffer** interface is obtained by calling the [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) function.</span></span>

<span data-ttu-id="7fa68-144">Тип LPD3DXPRTCOMPBUFFER определяется как указатель на интерфейс **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="7fa68-144">The LPD3DXPRTCOMPBUFFER type is defined as a pointer to the **ID3DXPRTCompBuffer** interface.</span></span>


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="7fa68-145">Требования</span><span class="sxs-lookup"><span data-stu-id="7fa68-145">Requirements</span></span>



| <span data-ttu-id="7fa68-146">Требование</span><span class="sxs-lookup"><span data-stu-id="7fa68-146">Requirement</span></span> | <span data-ttu-id="7fa68-147">Значение</span><span class="sxs-lookup"><span data-stu-id="7fa68-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa68-148">Header</span><span class="sxs-lookup"><span data-stu-id="7fa68-148">Header</span></span><br/>  | <dl> <span data-ttu-id="7fa68-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fa68-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7fa68-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7fa68-150">Library</span></span><br/> | <dl> <span data-ttu-id="7fa68-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fa68-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7fa68-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fa68-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa68-153">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="7fa68-153">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7fa68-154">**D3DXCreatePRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="7fa68-154">**D3DXCreatePRTCompBuffer**</span></span>](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="7fa68-155">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="7fa68-155">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
